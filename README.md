# GitOps Repository - Heno

ArgoCD-managed infrastructure and applications for Heno Kubernetes cluster.

## Structure

```
gitops-heno/
├── argocd/
│   └── applications/     # ArgoCD Application definitions
├── infrastructure/       # Infrastructure components
│   ├── traefik/         # Traefik Ingress Controller
│   └── metrics-server/  # Kubernetes Metrics Server
└── apps/                # Application workloads (add your apps here)
```

## Current Applications

### Infrastructure
- **Traefik** - Ingress Controller (NodePort)
- **Metrics Server** - Kubernetes metrics API

### Applications
_Add your applications in the `apps/` directory_

## How to Use

1. Add new applications in `apps/` directory
2. Create ArgoCD Application manifests in `argocd/applications/`
3. Commit and push changes
4. ArgoCD will automatically sync the changes

## ArgoCD Configuration

All applications are configured with:
- Automated sync enabled
- Self-heal enabled
- Prune enabled

## Cluster Info

- **K8s Master**: 192.168.2.139
- **K8s Worker**: 192.168.2.140
- **MariaDB**: 192.168.2.141
- **Redis**: 192.168.2.142
