# spinkube-demo-charts
Get up and running with SpinKube quickly with helm charts

# Pre-requisites

1. containerd and containerd-shim-spin installed on each node
Your nodes may already have this for example if you are using the k3d image from the quickstart docs or if you are using [AKS WASI nodepools](https://learn.microsoft.com/en-us/azure/aks/use-wasi-node-pools). If you are not, check out the [runtime class manager](https://github.com/spinkube/runtime-class-manager) project for shim installation guidance.

2. cert-manager   
If you don't already have cert-manager installed, the following command installs it using Helm (taken from cert-manager docs):
```console
helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --create-namespace \
  --version v1.14.5 \
  --set installCRDs=true
```

# Install Guide

```console
helm install spinkube-cluster-resources spinkube-cluster-resources
helm install spin-operator spin-operator
```
