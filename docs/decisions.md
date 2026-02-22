# Design Decisions

## Why AKS
AKS provides a managed Kubernetes control plane suitable for enterprise deployments and aligns with Azure-first cloud environments.

## Why NGINX Ingress
Ingress provides L7 routing and an external entry point without exposing services individually.

## Why managed identity
Removes the need to manage long-lived credentials and supports least-privilege patterns.

## What would change for production
- Private cluster + private endpoints
- Key Vault CSI driver for secrets
- Network policies + egress control
- Full observability (Container Insights, alerts, dashboards)
- Multi-node pools and upgrade strategy