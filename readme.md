# Project Title: AWS Infrastructure as Code (IaC) with Terraform

## Overview
This project demonstrates how to use Terraform to provision AWS infrastructure (VPC, EC2, RDS, S3, etc.)

## Tech Stack
- Terraform
- AWS (Amazon Web Services)
- Github Actions

## Architecture

![Architecture Diagram](./diagrams/diagram.png)

---

## Features


---

## Folder Structure

```
.
├── .github/workflows/s        # CI/CD pipeline definitions
├── k8s/                      # K8s manifests or Helm charts
├── infra/                    # IaC for infra setup
├── dashboards/               # Monitoring dashboards (JSON/screenshots)
├── diagrams/                 # Architecture visuals
└── README.md
```

---

## Getting Started

### Prerequisites
- AWS Account
- 
- Terraform (if infra is included)

### Setup Steps
```bash
# Clone the repo
git clone https://github.com/Rbilli51614/aws-infra-terraform.git
cd repo-name

# Deploy infrastructure (if applicable)
cd infra/
terraform init && terraform apply

# Deploy app to Kubernetes
cd ../k8s/
kubectl apply -f .

# Monitor app
kubectl port-forward svc/grafana 3000:3000
```

---

## CI/CD Pipeline

- **Trigger**: On push to `main`
- **Stages**:
  1. Lint and test code
  2. Build Docker image and push to DockerHub
  3. Deploy to Kubernetes using Helm

_Workflows are located in `.github/workflows/`._

---

## Screenshots

| Grafana Dashboard|                               | ArgoCD Sync |
|--------------------------------------||-----------------------------------|
| ![grafana](./dashboards/grafana.png) | ![argocd](./diagrams/diagram.png) |

---

## Lessons Learned
- 
- 

---

## TODO
- 

---

## License
MIT
