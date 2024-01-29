# Here is the commands fot starting the docker for kafka

## Start ZooKeeper on Docker

docker run -p 2181:2181 zookeeper

## Start Kafka Client with Zookeeper

docker run -p 9092:9092 -e KAFKA_ZOOKEEPER_CONNECT=192.168.137.1:2181 -e KAFKA_ADVERTISED_LISTENERS=PLAINTEXT://192.168.137.1:9092 -e KAFKA_OFFSETS_TOPIC_REPLICATION_FACTOR=1 confluentinc/cp-kafka
