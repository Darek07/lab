# Prometheus stack

Prometheus with Grafana for local cluster. [Prometheus stack repo](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack).

# Installation

```bash
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install prometheus-stack prometheus-community/kube-prometheus-stack --namespace=monitoring --create-namespace
```

# Grafana login

Admin user: get from default values or from secrets.
Admin password: get from secrets or change in values to `adminPassword` (dev only).

```bash
k get secret -n monitoring prometheus-stack-grafana -o jsonpath='{.data.admin-password}' | base64 -d; echo
```
