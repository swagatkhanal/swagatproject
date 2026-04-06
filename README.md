# Full-Stack Deployment with CI/CD & Monitoring

This project demonstrates a professional DevOps workflow featuring a containerized MERN-stack application, automated deployment via GitHub Actions, and real-time infrastructure monitoring.

## 🚀 Features
- **Containerization:** Entire stack (Frontend, Backend, MongoDB) managed via Docker Compose.
- **CI/CD Pipeline:** Automated deployment to an Azure VM using GitHub Actions.
- **Monitoring:** Real-time metrics collection using Prometheus and Node Exporter.
- **Observability:** Custom Grafana dashboards for CPU and RAM utilization.
- **Persistence:** Docker volumes configured for Grafana to ensure data retention.

## 🛠️ Tech Stack
- **Frontend:** Nginx / React (or your specific framework)
- **Backend:** Node.js / Express
- **Database:** MongoDB
- **DevOps:** Docker, GitHub Actions, Azure VM
- **Monitoring:** Prometheus, Grafana, Node Exporter

## 📊 Monitoring Setup
The monitoring stack is accessible at:
- **Grafana:** `http://<VM-IP>:3001`
- **Prometheus:** `http://<VM-IP>:9090`
- **Metrics:** `http://<VM-IP>:9100/metrics`

## ⚙️ How to Deploy
1. Update the code locally.
2. Commit and push to the `main` branch.
3. GitHub Actions will automatically SSH into the Azure VM and run:
   ```bash
   sudo docker compose up --build -d
