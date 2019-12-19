# Helpful commands

## Kubernetes

### Pods

```bash
# display running pods sorted by creation, phase can be Running|Failed|Pending|Unknown|Succeeded
kubectl get pods --field-selector=status.phase=Running --sort-by=.metadata.creationTimestamp
# display logs
kubectl logs my-pod
# tail logs
kubectl logs -f my-pod
# delete pods
kubectl delete pods my-pod
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

## Linux

### Vi

```
# go to beginning of files
gg
# delete al lines after cursor
dG
```

## MongoDB

### Command examples

```
db.getCollectionNames()
db.{collection}.findOne()
```

## Kafka

### Command examples

```bash
# list topics
bin/kafka-topics.sh --zookeeper localhost:2181 --list
# get the latest offset of a topic
bin/kafka-run-class.sh kafka.tools.GetOffsetShell --broker-list {brokers} --topic {topic} --time -1
```
