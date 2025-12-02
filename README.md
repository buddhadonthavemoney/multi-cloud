# Multi-Cloud TicTacToe + Kubernetes Infrastructure

This repository combines a **realtime multiplayer TicTacToe application** and a **production-ready multi-cloud Kubernetes infrastructure**. The goal is to demonstrate a full, cloud-agnostic deployment pipeline—from app to cluster—using reusable Terraform modules for AWS and GCP.

## What’s Inside

### 🎮 **Multiplayer TicTacToe Application**

Located in the `multicloud-tictactoe/` submodule.

* FastAPI backend with WebSockets
* Redis-backed shared game state
* Responsive Jinja2 UI
* Dockerfile + Kubernetes manifests (Deployments, Services, Ingress)

This application can be deployed to any Kubernetes cluster created by the infrastructure layer.

---

### ☁️ **Multi-Cloud Kubernetes Infrastructure**

Located in the `multicloud-terraform/` submodule.

* Terraform modules for **AWS EKS** and **GCP GKE**
* Reusable VPC/networking modules for both clouds
* Environment-based workflows (`environments/aws/production`, `environments/gcp/production`)
* Supports local or remote Terraform state backends

This layer provisions the clusters where the TicTacToe app can run.

---

## Repository Structure

```
/
├── multicloud-tictactoe/        # FastAPI + Redis multiplayer game + K8s manifests
└── multicloud-terraform/        # Multi-cloud infra: AWS EKS + GCP GKE modules + envs
```

---

## Purpose

This repo serves as an end-to-end example of:

* Building a realtime web app
* Packaging it for Kubernetes
* Deploying it consistently across **multiple cloud providers** using Terraform

Ideal for demos, learning, or as a foundation for multi-cloud projects.
