# Cost Model (Budget Lab)

## Strategy
This environment is designed to be used in short lab sessions and removed immediately afterward.

## Guardrails
- Single node pool
- Minimal add-ons by default
- Delete the resource group after validation to avoid ongoing compute/LB costs

## Shutdown
The preferred shutdown is full teardown:
`az group delete -n rg-aks-lab --yes --no-wait`