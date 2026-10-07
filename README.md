# 🚀 Node.js Docker & Ansible Deployment

A simple DevOps project demonstrating how to containerize a Node.js application with Docker and automate the deployment process using Ansible.

## 🛠️ Technologies

* Node.js
* Docker
* Docker Hub
* Ansible
* Ubuntu / WSL
* Git & GitHub

## 📌 Project Architecture

```text
Developer
    │
    ▼
 GitHub Repository
    │
    ▼
 Ansible
    │
    ├── Build Docker Image
    ├── Tag Image
    ├── Login to Docker Hub
    ├── Push Image
    │
    ▼
 Docker Hub
    │
    ▼
 Docker Container
    │
    ▼
 Node.js Application
```

## ⚙️ Prerequisites

Make sure you have installed:

* Node.js
* Docker
* Ansible
* Git

## 🚀 Run the Project

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/ansible-nodejs-docker.git
cd ansible-nodejs-docker
```

Install dependencies:

```bash
npm install
```

Run the application:

```bash
npm start
```

## 🐳 Build Docker Image

```bash
docker build -t ansible-nodejs-img .
```

Run the container:

```bash
docker run -d \
  -p 3000:3000 \
  --name ansible-nodejs-container \
  ansible-nodejs-img
```

The application will be available at:

```text
http://localhost:3000
```

## 🤖 Ansible Deployment

Run:

```bash
ansible-playbook ansible-playbook.yaml
```

The playbook automates:

1. Docker image build
2. Image tagging
3. Docker Hub authentication
4. Image push
5. Container deployment

## 🔐 Environment Variables

Never store passwords or Docker Hub tokens directly inside the repository.

Example:

```bash
export DOCKER_PASSWORD="YOUR_DOCKER_HUB_TOKEN"
```

Then run:

```bash
ansible-playbook ansible-playbook.yaml
```

## 📚 What I Learned

* Docker image creation
* Docker container management
* Docker Hub image publishing
* Ansible automation
* Environment variable management
* Linux / WSL development
* DevOps deployment workflow
  

## 👨‍💻 Author

**Mohammed Hamada**

This project was created as part of my DevOps learning journey.


    
