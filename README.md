# Kubernetes Backend Platform

## Project Overview
This project demonstrates a local Kubernetes-based backend platform using `kind`. It includes:

- **api-gateway**: External entry point for the services.
- **orders-service**: Internal service with dummy endpoints.
- **Health checks**: `/health` endpoint for liveness and readiness.
- **Scaling & Availability**: Horizontal Pod Autoscaler (HPA) and Pod Disruption Budgets (PDB) configured.
- **Identity & Access**: ServiceAccounts and RBAC roles for each service.
- **Ingress**: API gateway routing.
- **CI/CD**: GitHub Actions pipeline to build Docker images and deploy to Kubernetes.

---

## Prerequisites

- Docker
- Kind (Kubernetes in Docker)
- kubectl
- Git

---

## Local Setup

1. Clone repository:

```bash
git clone https://github.com/Nidhi8901/k8s-backend-platform.git
cd k8s-backend-platform
