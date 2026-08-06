# 🚀 End-to-End DevSecOps Three-Tier Application Deployment on AWS EKS

![AWS](https://img.shields.io/badge/AWS-EKS-orange?logo=amazonaws)
![Terraform](https://img.shields.io/badge/Terraform-623CE4?logo=terraform)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-2088FF?logo=githubactions)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?logo=argo)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?logo=prometheus)
![Grafana](https://img.shields.io/badge/Grafana-F46800?logo=grafana)
![License](https://img.shields.io/badge/License-MIT-green)

## 📖 Project Overview

This project demonstrates a complete **Enterprise DevSecOps CI/CD pipeline** for deploying a **Three-Tier Web Application** on **Amazon EKS** using modern cloud-native technologies.

The application consists of:

* 🎨 Frontend – ReactJS
* ⚙️ Backend – NodeJS (Express)
* 🗄️ Database – MongoDB

The infrastructure is provisioned using **Terraform**, containerized with **Docker**, deployed to **Amazon EKS**, managed through **GitOps with ArgoCD**, and monitored using **Prometheus** and **Grafana**.

---

# 🏗️ Architecture

```
Developer
      │
      ▼
GitHub Repository
      │
      ▼
GitHub Actions CI Pipeline
      │
      ├── Checkout Source
      ├── Build Application
      ├── Unit Tests
      ├── SonarQube Analysis
      ├── Quality Gate
      ├── OWASP Dependency Check
      ├── Trivy File Scan
      ├── Docker Build
      ├── Trivy Image Scan
      ├── Push Image to Amazon ECR
      ▼
Update Kubernetes Manifests
      │
      ▼
GitHub (GitOps Repository)
      │
      ▼
ArgoCD
      │
      ▼
Amazon EKS Cluster
      │
      ▼
Frontend → Backend → MongoDB
      │
      ▼
Prometheus + Grafana Monitoring
```

---

# ☁️ AWS Services Used

* Amazon EKS
* Amazon ECR
* EC2
* IAM
* VPC
* Security Groups
* CloudWatch
* Load Balancer
* Route Tables
* Internet Gateway

---

# 🛠️ Technologies Used

| Category           | Tools                                    |
| ------------------ | ---------------------------------------- |
| Cloud              | AWS                                      |
| Infrastructure     | Terraform                                |
| CI/CD              | GitHub Actions                           |
| Containerization   | Docker                                   |
| Container Registry | Amazon ECR                               |
| Orchestration      | Kubernetes (EKS)                         |
| GitOps             | ArgoCD                                   |
| Package Manager    | Helm                                     |
| Monitoring         | Prometheus                               |
| Visualization      | Grafana                                  |
| Security           | Trivy, OWASP Dependency Check, SonarQube |
| Backend            | NodeJS                                   |
| Frontend           | ReactJS                                  |
| Database           | MongoDB                                  |

---

# 📁 Repository Structure

```
DevOps-End-to-End-Kubernetes-Three-Tier-Project
│
├── Application-Code
│   ├── frontend
│   ├── backend
│   └── database
│
├── Terraform
│   ├── VPC
│   ├── EKS
│   ├── IAM
│   └── Networking
│
├── GitHub-Actions
│   └── workflow.yml
│
├── Kubernetes-Manifests
│   ├── frontend
│   ├── backend
│   ├── mongodb
│   ├── ingress
│   ├── configmap
│   └── secrets
│
├── Helm
│
├── Monitoring
│   ├── Prometheus
│   └── Grafana
│
├── ArgoCD
│
└── README.md
```

---

# ⚙️ CI/CD Pipeline

The GitHub Actions workflow automates the complete software delivery lifecycle.

### Pipeline Stages

* Checkout Source Code
* Setup Java
* Restore Maven Cache
* Build Application
* Execute Unit Tests
* SonarQube Code Analysis
* Sonar Quality Gate
* OWASP Dependency Check
* Trivy Filesystem Scan
* Docker Image Build
* Trivy Image Scan
* Authenticate with Amazon ECR
* Push Docker Image
* Update Kubernetes Manifest
* Commit Image Tag
* ArgoCD Auto Sync
* Deploy to Amazon EKS

---

# 🔐 DevSecOps Implementation

The pipeline integrates security checks at multiple stages.

✔ SonarQube Static Code Analysis

✔ Sonar Quality Gate

✔ OWASP Dependency Check

✔ Trivy Filesystem Scan

✔ Trivy Docker Image Scan

✔ Secure Image Storage in Amazon ECR

---

# 🚀 Infrastructure Provisioning

Infrastructure is created using reusable Terraform modules.

Resources Provisioned

* VPC
* Public & Private Subnets
* Internet Gateway
* NAT Gateway
* Route Tables
* IAM Roles
* Security Groups
* Amazon EKS Cluster
* Managed Node Groups

---

# ☸️ Kubernetes Deployment

Application components deployed:

* Frontend Deployment
* Backend Deployment
* MongoDB StatefulSet
* Services
* Ingress
* ConfigMaps
* Secrets
* Persistent Volume Claims

---

# 🔄 GitOps Workflow

```
Developer

     │

Git Push

     │

GitHub Actions

     │

Build + Test + Scan

     │

Docker Build

     │

Push to Amazon ECR

     │

Update Kubernetes YAML

     │

Push Changes

     │

ArgoCD Detects Change

     │

Automatic Sync

     │

Amazon EKS Deployment
```

---

# 📊 Monitoring & Observability

Monitoring stack includes:

* Prometheus for Metrics Collection
* Grafana Dashboards
* Kubernetes Cluster Monitoring
* Node Exporter
* kube-state-metrics
* Application Health Monitoring

Metrics monitored include:

* CPU Usage
* Memory Usage
* Disk Usage
* Pod Status
* Node Status
* Network Traffic
* Container Restarts

---

# 📸 Project Screenshots

Add screenshots here.

```
images/

├── architecture.png

├── github-actions.png

├── argocd.png

├── grafana-dashboard.png

├── prometheus.png

├── eks-nodes.png

└── application.png
```

---

# 🎯 Learning Outcomes

This project demonstrates practical experience with:

* Infrastructure as Code (Terraform)
* GitHub Actions CI/CD
* Docker Image Management
* Amazon EKS
* Kubernetes Workloads
* GitOps using ArgoCD
* DevSecOps Best Practices
* Container Security
* Monitoring & Observability
* Cloud Infrastructure Automation

---

# 📌 Future Enhancements

* Blue/Green Deployment
* Canary Deployment
* Horizontal Pod Autoscaler
* Cluster Autoscaler
* AWS Load Balancer Controller
* External Secrets Operator
* OpenTelemetry
* Loki & Tempo Integration
* KEDA Event-Driven Autoscaling

---

# 👨‍💻 Author

**Darshan T**

Associate DevOps Engineer

**Tech Stack:** AWS | Kubernetes | Docker | Terraform | GitHub Actions | ArgoCD | Helm | Prometheus | Grafana | Linux | DevSecOps

If you found this project useful, consider giving it a ⭐ on GitHub.
