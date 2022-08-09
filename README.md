# Kafka-Order-Email-Stock-Services

#Commands for Kafka Windows

zookeeper-server-start.bat ..\..\config\zookeeper.properties

kafka-server-start.bat ..\..\config\server.properties

kafka-topics.bat --create --topic my-topic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 3

kafka-console-producer.bat --broker-list localhost:9092 --topic my-topic

kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic my-topic --from-beginning

Event-driven architecture is often referred to as “asynchronous” communication. This means that the sender and recipient don’t have to wait for each other to move on to their next task. Systems are not dependent on that one message. For instance, a telephone call is considered synchronous or more along the lines of the traditional “request/response” architecture. Someone calls you and asks you to do something, the requestor waits while the responder completes the task, and then both parties hang up. An asynchronous example would be text messaging. You send a message and in some cases, you don't even know who you are sending it to or if anyone’s listening, but you are not waiting for a response.
Event-driven apps can be created in any programming language because event-driven is a programming approach, not a language. An event-driven architecture is loosely coupled


STEPS
1.Open the application.properties file of the order-service project and configure Kafka producer.
spring.kafka.producer.bootstrap-servers: localhost:9092
spring.kafka.producer.key-serializer: org.apache.kafka.common.serialization.StringSerializer
spring.kafka.producer.value-serializer: org.springframework.kafka.support.serializer.JsonSerializer
spring.kafka.topic.name=order_topics

2.Configure Kafka Topic in OrderService Microservice

3.Create Kafka Producer in OrderService Microservice
4.Create REST API to Send Order and Test Kafka Producer in OrderService Microservice
5.Configure Kafka Consumer in StockService Microservice
6.Create Kafka Consumer in StockService Microservice
7.Configure and Create Kafka Consumer in EmailService Microservice

8.Run 3 Microservices Together and Have a Demo

Let's run all the below 3 Spring boot microservices projects:
order-service
stock-service
email-service
