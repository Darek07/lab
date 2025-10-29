# Homarr

[Homarr repo](https://github.com/homarr-labs/charts/tree/dev/charts/homarr)

# Installation

```bash
helm repo add homarr-labs https://homarr-labs.github.io/charts/
helm repo update
helm install homarr homarr-labs/homarr --namespace homarr --create-namespace

kubectl create secret generic db-encryption --from-literal=db-encryption-key=$(openssl rand -hex 32) --namespace homarr
```
