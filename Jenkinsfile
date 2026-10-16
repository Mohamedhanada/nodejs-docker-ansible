pipeline {
    agent any

    environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerhub')
	}
    stages {
        stage('Docker Login') {
            steps {
                // Add --password-stdin to run docker login command non-interactively
                withCredentials([usernamePassword(
                    credentialsId: 'dockerhub',
                     usernameVariable: 'DOCKER_USERNAME',
                      passwordVariable: 'DOCKER_PASSWORD')]) {
                    bat "echo %DOCKER_PASSWORD% | docker login -u %DOCKER_USERNAME% --password-stdin"
                }
            }
        }
        stage('Build & push Dockerfile') {
            steps {
                bat """
                cd node_js/
                ansible-playbook ansible-playbook.yml
                """
            }
        }
    } 
}
