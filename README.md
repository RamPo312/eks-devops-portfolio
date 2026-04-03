#  End-to-End DevOps Deployment on AWS EKS

## Project Overview

This project demonstrates a complete DevOps workflow by deploying a containerized Python Flask application on AWS EKS using Terraform, Docker, Kubernetes, and GitHub Actions.

It covers the full lifecycle from application development to automated deployment in a cloud-native environment.

---

## Architecture

- Application developed using Python Flask
- Docker used for containerization
- Terraform used for infrastructure provisioning
- AWS EKS used for Kubernetes cluster
- GitHub Actions used for CI/CD automation
- Kubernetes LoadBalancer used to expose the application

---

## Tech Stack

- AWS EKS
- Terraform
- Docker
- Kubernetes
- GitHub Actions
- Python Flask

---

## Screenshots

## Screenshots

### 🔹 Application Running
![App](https://raw.githubusercontent.com/RamPo312/eks-devops-portfolio/main/screenshots/app-running.png)

### 🔹 Kubernetes Pods
![Pods](Screenshots/pods.png)

### 🔹 Kubernetes Service (LoadBalancer)
![Service](screenshots/service.png)

### 🔹 GitHub Actions CI/CD Pipeline
![CI/CD](screenshots/github-actions.png)

### 🔹 Docker Hub Image
![Docker](screenshots/dockerhub.png)

### 🔹 AWS EKS Cluster
![EKS](screenshots/eks.png)



---

## Setup Instructions

### Clone Repository
```bash
git clone https://github.com/RamPo312/eks-devops-portfolio.git
cd eks-devops-portfolio

---

## Commands Used

# =========================
#  Git & GitHub Commands
# =========================
git clone https://github.com/RamPo312/eks-devops-portfolio.git
cd eks-devops-portfolio
git status
git add .
git commit -m "updated project"
git push origin main


# =========================
#  Docker Commands
# =========================
docker build -t <dockerhub-username>/eks-devops-app:v1 ./app
docker login
docker push <dockerhub-username>/eks-devops-app:v1
docker images
docker run -p 5000:5000 <dockerhub-username>/eks-devops-app:v1


# =========================
#  Terraform Commands
# =========================
terraform init
terraform validate
terraform plan
terraform apply
terraform destroy


# =========================
#  Kubernetes (EKS) Commands
# =========================
aws eks update-kubeconfig --region us-east-1 --name eks-devops-cluster
kubectl get nodes
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
kubectl get pods
kubectl get svc
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl delete -f k8s/deployment.yaml
kubectl delete -f k8s/service.yaml
