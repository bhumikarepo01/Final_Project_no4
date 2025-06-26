
# CI/CD Pipeline with GitHub Actions & Docker (Local Deployment)

---

## 🟣 Project Overview

This project demonstrates a complete CI/CD pipeline using:
- Docker to build and containerize the app
- Docker Hub to store and share Docker images
- GitHub Actions to automate build/test/push pipeline
- Minikube to deploy the app locally on Kubernetes

---

## 🟣 Tools and Technology

- GitHub (version control & CI)
- GitHub Actions (automation)
- Docker & Docker Hub
- Minikube (Kubernetes)
- Node.js
- YAML

---

## 🟣 Project Structure

```
my-cicd-project/
├── .github/
│   └── workflows/
│       └── ci-cd.yaml
├── Dockerfile
├── package.json
├── server.js
├── service.yaml
├── deployment.yaml
├── screenshots/
│   ├── ci_pipeline.png
│   ├── dockerhub.png
│   ├── pod_output.png
│   └── server.png
├── README.md
```

---

## 🟣 How to Run This Project (Step-by-Step)

### 1. Pre-requisites
- Git & GitHub account
- Docker Desktop
- Minikube
- Node.js & npm
- Docker Hub account

### 2. Fork or Clone the Repository
```bash
git clone https://github.com/bhumikarepo01/Final_Project_no4.git
cd my-cicd-project
```

### 3. Set Up GitHub Secrets
Go to GitHub repo > Settings > Secrets > Actions and add:
- `DOCKER_USERNAME`
- `DOCKER_PASSWORD`

### 4. Trigger the CI/CD Workflow
```bash
git add .
git commit -m "Trigger CI/CD"
git push origin main
```

### 5. Start Minikube
```bash
minikube start
```

### 6. Deploy to Kubernetes
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 7. Port Forwarding
```bash
kubectl port-forward service/my-cicd-app 3000:80
```

### 8. View the App
Visit: [http://localhost:3000](http://localhost:3000)

---

## 🟣 Screenshots

- `ci_pipeline.png` – GitHub Actions pipeline success
- `dockerhub.png` – Docker Hub image
- `pod_output.png` – Pod running
- `server.png` – App response

---

## 🟣 Summary

This pipeline runs fully locally. It automates testing, image creation, and deployment.  
Great for learning DevOps without cloud platforms.
