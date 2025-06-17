# CI/CD Pipeline with GitHub Actions & Docker (Local Deployment)

---

## 🟣 Project Overview

This project demonstrates a **complete CI/CD pipeline** using:

✅ **Docker:** To build and containerize the application.  
✅ **Docker Hub:** To store and distribute the Docker image.  
✅ **GitHub Actions:** To automate testing, building, and pushing the image.  
✅ **Minikube:** To deploy and run the Docker image in a local Kubernetes environment.

---

## 🟣 Tools and Technology

- **Docker**
- **Docker Hub**
- **GitHub Actions**
- **Minikube**
- **YAML configuration files**

---

## 🟣 Project Structure
my-cicd-project/
├── .github/
│ └─ workflows/
│ └─ ci-cd.yaml
├── Dockerfile
├── package.json
├── server.js
├── service.yaml
├── deployment.yaml
├── screenshots/
│ ├─ ci_pipeline.png
│ ├─ dockerhub.png
│ ├─ pod_output.png
│ └─ server.png
├── README.md

## 🟣 CI Flow (Workflow)

1️⃣ Push code to **main branch** on GitHub.  
2️⃣ GitHub Actions pipeline starts automatically.  
3️⃣ Tests are run first.  
4️⃣ Docker image is built and pushed to **Docker Hub**.  

---

## 🟣 Deployment Flow (Local)

1️⃣ Start **Minikube**:

```shell```
minikube start

2️⃣ Apply Deployment and Service to the Cluster:

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

3️⃣ Forward port to view the application:

kubectl port-forward service/my-service 3000:3000

4️⃣ Access the application at:

http://localhost:3000

🟣 Screenshots
The screenshots/ directory contains:

Screenshot_CI_pipeline.png: GitHub Actions pipeline successfully finished.

Screenshot_Dockerhub.png: Docker Hub shows the pushed image.

Screenshot_pod_output.png: The pod is up and running in Minikube.

Screenshot_Server.png: The application is serving requests at http://localhost:3000.

🟣 Summary
This pipeline lets you:
  Push code and immediately deploy it to your local Kubernetes environment.
  Automate testing, building, and delivery.
  Integrate CI and CD practices without needing a huge production stack.


