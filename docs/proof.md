## Runtime Validation

### Cluster Health
- AKS node pool operational
- Kubernetes version: v1.33.6
- Container runtime: containerd
- Node status: Ready

### Workload Status
- hello deployment running (1/1 ready)
- Service exposed via ClusterIP
- NGINX ingress controller provisioned
- Public endpoint reachable

### External Endpoint
- Ingress IP: 135.233.20.48
- Port: 80

### Nodes

| Name | Status | Version | Internal IP | OS |
|------|--------|---------|------------|----|
| aks-nodepool1-74457834-vmss000000 | Ready | v1.33.6 | 10.224.0.4 | Ubuntu 22.04 |

### Pods

| Name | Ready | Status | Node |
|------|-------|--------|------|
| hello-6f5dcb7d8-lt97r | 1/1 | Running | aks-nodepool1-74457834-vmss000000 |

### Services

| Name | Type | External IP | Ports |
|------|------|------------|-------|
| ingress-nginx-controller | LoadBalancer | 135.233.20.48 | 80,443 |

### Ingress

| Name | Class | Address | Port |
|------|------|---------|------|
| hello-ingress | nginx | 135.233.20.48 | 80 |

<details>
<summary>Raw kubectl output</summary>

```text
NAME STATUS ROLES AGE VERSION INTERNAL-IP EXTERNAL-IP OS-IMAGE KERNEL-VERSION CONTAINER-RUNTIME aks-nodepool1-74457834-vmss000000 Ready <none> 3m18s v1.33.6 10.224.0.4 <none> Ubuntu 22.04.5 LTS 5.15.0-1102-azure containerd://1.7.30-1 NAME READY STATUS RESTARTS AGE IP NODE NOMINATED NODE READINESS GATES hello-6f5dcb7d8-lt97r 1/1 Running 0 2m7s 10.244.0.64 aks-nodepool1-74457834-vmss000000 <none> <none> NAME TYPE CLUSTER-IP EXTERNAL-IP PORT(S) AGE ingress-nginx-controller LoadBalancer 10.0.6.196 135.233.20.48 80:30582/TCP,443:31284/TCP 103s ingress-nginx-controller-admission ClusterIP 10.0.201.178 <none> 443/TCP 103s NAME CLASS HOSTS ADDRESS PORTS AGE hello-ingress nginx * 135.233.20.48 80 66s