
### Quick Order Simulation with Kafka

#### credit-check + availability + fraud-detection

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
