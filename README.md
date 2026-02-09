# Kubernetes Production-Style Deployment Demo

A production-oriented Kubernetes project demonstrating deployment of a web application and MongoDB database with best practices such as resource management, health checks, autoscaling, and secure configuration.

---

## 📌 Project Overview

This project simulates a real-world Kubernetes deployment environment by implementing:

- Web application deployment using Nginx  
- MongoDB database deployment  
- Secure credential management using Secrets  
- Configuration management using ConfigMaps  
- Namespace isolation  
- Health monitoring via liveness & readiness probes  
- Resource requests and limits  
- Horizontal Pod Autoscaling (HPA)  

---

## Tech Stack

- Kubernetes  
- Minikube  
- Docker  
- MongoDB  
- Nginx  

---

## Architecture

User → NodePort Service → Nginx Pods → MongoDB Service → MongoDB Pod

---

## Key Enhancements Implemented

### ✅ Namespace Isolation
All resources are deployed in a dedicated namespace to ensure environment separation and better organization.

### ✅ Resource Management
Configured CPU and memory requests/limits to optimize cluster utilization and prevent resource starvation.

### ✅ Liveness & Readiness Probes
Implemented health checks to ensure application reliability and enable zero-downtime deployments.

### ✅ Horizontal Pod Autoscaler (HPA)
Enabled automatic scaling of pods based on CPU utilization to handle varying workloads.

### ✅ Secure Secrets Handling
MongoDB credentials managed securely using Kubernetes Secrets instead of hardcoding sensitive data.

### ✅ ConfigMap Usage
Database connection details externalized using ConfigMaps for flexible configuration management.

---

## 🚀 How to Run

### Start Minikube
```bash
minikube start
```

### Create Namespace
```bash
kubectl apply -f namespace.yaml
```

### Deploy MongoDB
```bash
kubectl apply -f mongo/
```

### Deploy Web App
```bash
kubectl apply -f webapp/
```

### Access Application
```bash
minikube service webapp-service -n demo-app
```

---

## Learning Outcomes

- Hands-on Kubernetes production practices  
- Debugging and troubleshooting pods  
- Managing secure application configurations  
- Implementing scalability and reliability patterns  
- Understanding container orchestration concepts  

