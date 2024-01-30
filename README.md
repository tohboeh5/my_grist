# Outline

## develop

```bash
kubectl create secret generic nocodb-secret -n nocodb --dry-run=client --from-env-file=.env --output=yaml > kubefiles/secret.yaml
kubectl create secret generic postgres-secret -n nocodb --dry-run=client --from-env-file=postgres.env --output=yaml > kubefiles/postgres-secret.yaml
```

```bash
kubectl apply -f init
kubectl apply -f kubefiles
```