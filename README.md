# K8s Backend Platform – CI/CD Pipeline

## 📌 Project Overview
This project demonstrates a complete CI/CD pipeline for a microservices-based backend platform using:
- GitHub Actions for automation
- Docker for containerization
- Docker Hub for image registry
- Kubernetes for deployment

The pipeline automatically builds and pushes Docker images whenever code is pushed to the main branch.

---

## 🧱 Tech Stack
- GitHub Actions
- Docker & Docker Hub
- Kubernetes
- YAML
- Linux
- Git & GitHub

---
## Project Stucture
k8s-backend-platform/
├── services/
│ ├── api-gateway/
│ └── orders-service/
├── k8s/
│ ├── api-gateway-deployment.yaml
│ ├── orders-service-deployment.yaml
│ └── services.yaml
├── .github/workflows/
│ └── ci-cd.yml
└── README.md


---

## 🚀 CI/CD Workflow

### 🔄 Trigger
- Runs automatically on every push to the `main` branch.

### 🛠️ Steps
1. Checkout code from GitHub
2. Log in to Docker Hub using GitHub Secrets
3. Build Docker images for:
   - API Gateway
   - Orders Service
4. Push images to Docker Hub

---

## 🔐 Secrets Used
Stored securely in GitHub:
- `DOCKERHUB_USERNAME`
- `DOCKERHUB_PASSWORD` (Docker Hub Personal Access Token)

---

## 🐳 Docker Images
Images are pushed to:
- `docker.io/nidhi8901/api-gateway`
- `docker.io/nidhi8901/orders-service`

---

## ☸️ Kubernetes Deployment
After images are pushed, they can be deployed using:
```bash
kubectl apply -f k8s/

