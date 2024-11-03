Starts kafka + zookeper containers:
docker-compose up -d

check up containers:
docker-compose ps

Enter in kafka container:
docker exec -it kafka bash

Creates kafka topic:
if container doesn't find kafka topic then execute "whereis kafka-topics"
so the terminal will returns /opt/kafka_2.13-2.8.1/bin/kafka-topics.sh.

/opt/kafka_2.13-2.8.1/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3 --topic user

