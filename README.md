i# Docker + Kubernetes CI/CD Pipeline Project

This project demonstrates end-to-end deployment of a Flask application using Docker, Kubernetes (Minikube), and GitHub Actions CI/CD pipeline.

## Tech Stack
- Python (Flask)
- Docker
- Kubernetes (Minikube)
- GitHub Actions

## Architecture Flow

GitHub → GitHub Actions → Docker Build → Kubernetes Deployment (Minikube)

## Run Locally

### 1. Clone repo
git clone <repo-url>
cd docker-kubernetes-demo

### 2. Build Docker image
docker build -t myapp .

### 3. Run container
docker run -p 5000:5000 myapp

## Kubernetes Deployment

### Apply deployment
kubectl apply -f deployment.yaml

### Check pods
kubectl get pods

### Expose service
minikube service myapp


## CI/CD Pipeline

On every push to `main` branch:
- Builds Docker image
- Runs container test

Workflow file:
.github/workflows/deploy.yml

## Project Structure

.github/workflows/   → CI/CD pipeline  
app.py               → Flask app  
Dockerfile           → Docker image  
deployment.yaml      → Kubernetes config  
README.md            → Documentation  


## Author
Rajeev Ranjan  
SRE / DevOps Enthusiast


## Key Learnings
- Docker containerization
- Kubernetes deployment using Minikube
- CI/CD automation using GitHub Actions
- Basic DevOps workflow design

