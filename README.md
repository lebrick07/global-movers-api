# Global Movers Application

Auto-generated application managed by OpenLuffy.

## Stack
- **Language**: Python
- **Framework**: FastAPI
- **Container Registry**: GitHub Container Registry (GHCR)

## Environments
- **Development**: `global-movers-dev` namespace
- **Pre-production**: `global-movers-preprod` namespace  
- **Production**: `global-movers-prod` namespace

## Local Development

### ```bash
pip install -r requirements.txt
python main.py
```

Visit: http://localhost:8000

## CI/CD Pipeline
GitHub Actions automatically builds and deploys on push:
- `develop` branch → DEV + PREPROD environments
- `main` branch → PRODUCTION environment (manual approval required)

## Deployment
Managed by ArgoCD - syncs automatically when new images are pushed.

## Health Check
All environments expose `/healthz` endpoint for liveness/readiness probes.

---
*Managed by OpenLuffy* 🏴‍☠️
