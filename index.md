# Helpful commands

## Kubernetes

### Pods

```bash
kubectl get pods --field-selector=status.phase=Running --sort-by=.metadata.creationTimestamp # display running pods sorted by creation
kubectl logs my-pod # display logs
kubectl logs -f my-pod # tail logs
```
