## Start docker-compose
```shell
docker-compose up
```

## Connect to kafka container
```shell
docker exec -it kafka bin/bash
```

## Change directory
```shell
cd /opt/kafka_<version>/bin
```

## Create topic
```shell
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic <topic_name>
```

## Show topics list
```shell
kafka-topics.sh --list --zookeeper zookeeper:2181
```
