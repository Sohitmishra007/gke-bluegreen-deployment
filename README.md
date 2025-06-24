# Blue-Green Deployment on GKE 🌍

This project demonstrates a **Blue-Green Deployment** strategy on **Google Kubernetes Engine (GKE)** using NGINX containers and ConfigMaps.

## 💡 What is Blue-Green Deployment?
Blue-green deployment is a release strategy that reduces downtime and risk. Two environments (blue and green) run in parallel; traffic is switched between them safely.

## 🧱 Architecture
- `blue-deployment.yaml`: Blue version of app
- `green-deployment.yaml`: Green version of app
- `configmaps.yaml`: Injects version-specific HTML
- `service.yaml`: Common service to switch traffic

## 🚀 Usage

```bash
kubectl apply -f configmaps.yaml
kubectl apply -f blue-deployment.yaml
kubectl apply -f green-deployment.yaml
kubectl apply -f service.yaml
