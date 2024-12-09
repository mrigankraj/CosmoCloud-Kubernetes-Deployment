# CosmoCloud Kubernetes Deployment

## Project Overview
Helm chart deploying microservices stack with:
- Backend Service
- Frontend Service
- Redis Database

## Deployment Instructions
```bash
helm install testapp cosmocloud-deploy --atomic --timeout 30s


## Service Configuration

Backend: ClusterIP, port 8000
Frontend: NodePort, port 5175
Redis: ClusterIP, port 6379

## Prerequisites

Kubernetes Cluster
Helm 3.x
