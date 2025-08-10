Starts kafka + zookeper containers:<br/>

url: https://github.com/confluentinc/cp-docker-images/blob/5.3.3-post/examples/kafka-cluster/docker-compose.yml
docker-compose up -d

check up containers:
docker-compose ps

Enter in kafka container:<br/>
docker exec -it kafka bash

Creates kafka topic:<br/>
if container doesn't find kafka topic then execute "whereis kafka-topics"
so the terminal will returns /opt/kafka_2.13-2.8.1/bin/kafka-topics.sh.

/opt/kafka_2.13-2.8.1/bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3 --topic user

