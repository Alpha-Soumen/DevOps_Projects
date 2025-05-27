# 🚀 React App with Docker and Kubernetes

A simple React application, containerized with Docker, pushed to Docker Hub, and deployed to a local Kubernetes cluster using Minikube.

---

## 🏗️ Project Overview

This project demonstrates how to:

✅ Create a React app  
✅ Containerize it with Docker  
✅ Push it to Docker Hub  
✅ Deploy it to Kubernetes (Minikube)  
✅ Access the app locally

---

## 📦 Prerequisites

Make sure you have these installed:

- [Node.js](https://nodejs.org/)  
- [Docker](https://www.docker.com/)  
- [kubectl](https://kubernetes.io/docs/tasks/tools/)  
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)

---

## 🛠️ Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Alpha-Soumen/DevOps_Projects.git
cd DevOps_Projects/React-docker-k8s-app/testapp

```
### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Run the App Locally

```bash
npm start
```

Visit [http://localhost:3000](http://localhost:3000).

---

## 🐳 Docker: Build and Push

### Build Docker Image

```bash
docker build -t soumenbhunia/react-k8s-app:latest .
```

### Push to Docker Hub

```bash
docker login
docker push soumenbhunia/react-k8s-app:latest
```

---

## ☸️ Kubernetes: Deploy with Minikube

### Start Minikube

```bash
minikube start
```

### Create Deployment

```bash
kubectl create deployment react-k8s-app --image=soumenbhunia/react-k8s-app:latest
```

### Expose Deployment

```bash
kubectl expose deployment react-k8s-app --type=NodePort --port=3000
```

### Access the App

```bash
minikube service react-k8s-app
```

This will open your app in the browser!

---

## 🔎 Kubernetes Management

### Check Pods, Deployments, and Services

```bash
kubectl get pods
kubectl get deployments
kubectl get services
```

### Clean Up

```bash
kubectl delete service react-k8s-app
kubectl delete deployment react-k8s-app
minikube stop
```

---

## 🧩 Project Structure

```
testapp/
├── Dockerfile
├── README.md
├── package.json
├── public/
│   └── index.html
└── src/
    ├── App.js
    ├── index.js
    └── ...
```

---

## ⚙️ Additional Notes

* If you face any issues with Minikube, restart it:

  ```bash
  minikube delete
  minikube start
  ```
* You can also **build and test locally** without Docker/Kubernetes by using:

  ```bash
  npm start
  ```

---

## 👨‍💻 Developed by

* **Soumen Bhunia**
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin)](https://www.linkedin.com/in/soumen-bhunia/)
 

---

