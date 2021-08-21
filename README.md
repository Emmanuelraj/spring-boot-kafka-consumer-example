This Project covers how to use Spring Boot with Spring Kafka to Publish JSON/String message to a Kafka topic

Below are the command for Linux/Mac and Windows
# Start Zookeeper
          Linux:  bin/zookeeper-server-start.sh config/zookeeper.properties
          Windows:  .\bin\windows\zookeeper-server-start.bat config\zookeeper.properties
# Start Kafka Server
          Linux : bin/kafka-server-start.sh config/server.properties
          Windows : .\bin\windows\kafka-server-start.bat config\server.properties
# Create Kafka Topic
        Linux : bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic # #   Kafka_Example
         Windows : .\bin\windows\kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic NewTopic
# Consume from the Kafka Topic via Console
      Linux : bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic Kafka_Example --from-beginning
       Windows :.\bin\windows\kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic NewTopic --from-beginning
