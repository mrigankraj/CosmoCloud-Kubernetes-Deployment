# CosmoCloud Kubernetes Deployment

## Project Overview
Helm chart for deploying a complete application stack with:
- Backend Service
- Frontend Service
- Redis Database

## Deployment Specifications
- Backend: `shreybatra/sample-backend`
  - Environment: REDIS_URI=redis://redis-svc:6379
- Frontend: `shreybatra/sample-frontend`
  - Environment: BACKEND_URL=http://backend-svc:8000
- Redis: Official `redis` image

## Service Configuration
- Backend Service
  - Type: ClusterIP
  - Port: 8000
- Frontend Service
  - Type: NodePort
  - Port: 5175
  - NodePort: 31000
- Redis Service
  - Type: ClusterIP
  - Port: 6379

## Deployment Command
```bash
helm install testapp cosmocloud-deploy --atomic --timeout 30s
