## Run docker compose
```shell script
docker-compose up -d
````

## Create topic
```shell script
docker exec -it kafka_container kafka-topics.sh --create --topic mytopic --bootstrap-server kafka:9092
```

## Describe
```shell script
docker exec -it kafka_container kafka-topics.sh --describe --topic mytopic --bootstrap-server kafka:9092
```

## Produce
```shell script
docker exec -it kafka_container kafka-console-producer.sh --topic mytopic --bootstrap-server localhost:9092
```

## Consumer
```shell script
docker exec -it kafka_container kafka-console-consumer.sh --topic mytopic --bootstrap-server kafka:9092 --from-beginning
```