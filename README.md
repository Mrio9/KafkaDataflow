Start Zoo-keeper
---------------------------------------------------------
bin/zookeeper-server-start.sh config/zookeeper.properties

Start Kafka-server
---------------------------------------------------------
bin/kafka-server-start.sh config/server.properties

create a topic
---------------------------------------------------------
bin/kafka-topics.sh --create --topic topicname --bootstrap-server {Put the Public IP of your EC2 Instance:9092} --replication-factor 1 --partitions 1

Start Producer
---------------------------------------------------------
bin/kafka-console-producer.sh --topic topicname --bootstrap-server {Put the Public IP of your EC2 Instance:9092}

Start Consumer
---------------------------------------------------------
bin/kafka-console-consumer.sh --topic demo_testing2 --bootstrap-server {Put the Public IP of your EC2 Instance:9092}
