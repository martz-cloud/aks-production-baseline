# AKS Production Baseline (Budget Lab)

## Overview
Production-style Azure Kubernetes Service deployment built with cost guardrails.

## Key Features
- AKS with managed identity
- Azure Container Registry integration
- NGINX ingress
- Cost-controlled lab pattern (deploy → validate → destroy)

## Architecture
[insert diagram later]

## Cost Strategy
Cluster is deployed only during lab sessions and fully removed afterward to minimize spend.