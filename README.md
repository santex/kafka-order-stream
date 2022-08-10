
### How it could look order simulation with kafka 

#### credit-check + availability + fraud-detection

---



```
export TRANSACTIONS_TOPIC=orders
export TRANSACTIONS_PER_SECOND=2
export KAFKA_BROKER_URL=http://localhost:9092
```


---

```
docker network create orders-network

docker-compose -f docker-compose.kafka.yml up -d

docker-compose -f docker-compose.kafka.yml logs -f broker | grep "started" &

docker-compose up -d

docker-compose -f docker-compose.kafka.yml exec broker kafka-console-consumer --bootstrap-server localhost:9092 --topic T

#docker-compose down

#docker-compose -f docker-compose.kafka.yml stop

#docker network rm orders-network

```


#### missing aspects payment & order state persistancy etc...
