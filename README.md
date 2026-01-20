# GitOps Deployment (Using ArgoCD)

This repository contains the GitOps configuration for deploying a 3-tier application (database, backend, frontend) to Kubernetes using ArgoCD.

It defines the desired cluster state and deployment order. Application code is maintained in a separate repository [click here](https://github.com/sumitNITS/3-tier-app)

## What This Repo Does

- Uses ArgoCD for continuous delivery
- Bootstraps the stack using the App of Apps pattern
- Enforces deployment order with Sync Waves
- Keeps Git as the single source of truth
- Enables automatic self-healing

## Repo Structure

bootstrap/
 - app-of-apps.yaml

apps/
 - namespace/
 - database/
 - migration/
 - backend/
 - frontend/

Each directory under `apps/` contains an ArgoCD `Application`.

## How to Deploy the application

Use the below command to get started

```bash
kubectl apply -f bootstrap/app-of-apps.yaml
```
