# Helpful commands

## Kubernetes

### Pods

```bash
# display running pods sorted by creation, phase can be Running|Failed|Pending|Unknown|Succeeded
kubectl get pods --field-selector=status.phase=Running --sort-by=.metadata.creationTimestamp
# filter pods by label
kubectl get pods -l app=my_app,version=1.0
# display logs
kubectl logs my-pod
# tail logs
kubectl logs -f my-pod
# delete pods
kubectl delete pods my-pod
# Attach to pod
kubectl exec -it my-pod -- /bin/bash
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

## HDFS

# Copy to remote
```bash
# To S3
hadoop distcp -Dfs.s3a.access.key="..." -Dfs.s3a.secret.key="..." /hdfs-folder/ s3a://s3-folder/
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

## Bash

### Test
```bash
# Test syntax
if [ cond ]
then
  echo "true"
else
  echo "false"
fi
# Test if variable empty
[ -z "$VAR" ] && echo "It's empty"
```

## Unix

### SSH
```bash
# Redirect local port 3308 to port 3306 of target.com using jump server jum.com
ssh -L 3308:target.com:3306 jump.com
```
