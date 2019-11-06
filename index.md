# Helpful commands

## Kubernetes

### Pods

```bash
kubectl get pods --field-selector=status.phase=Running --sort-by=.metadata.creationTimestamp # display running pods sorted by creation
kubectl logs my-pod # display logs
kubectl logs -f my-pod # tail logs
```

## Docker

### Connect to running container

```bash
docker exec -ti {container} /bin/bash
```

## Hive

### Connect with Beeline

```bash
beeline -u jdbc:hive2://localhost:10000/default -n {user}
```
