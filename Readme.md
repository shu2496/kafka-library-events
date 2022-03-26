## Kafka Spring Boot producer consumer application using H2 in-memory database
**Two applications, one for library-event-producer and another for library-event-consumer.**

## Details
1. there are 3 broker 
  * on ports 9092, 9093, 9094
2. library-event-Consumer port: 8081


Usage
1. To make POST request
                {
                    "libraryEventId":null,
                    "book":
                    {
                        "bookId":101,
                        "bookName":"MyKafka",
                        "bookAuthor":"Shubham"
                    }
                }
2. Run the post request. 
3. Check the changes in the database: http://localhost:8081/h2
4. Type jdbc:h2:mem:testdb  into JDBC URL
5. Type org.h2.Driver into Driver Class
6. Then connect

## Prerequisites
* Java 11
* Lombok
* Gradle
* kafka
* spring boot

## Installation & running
### Create 3 kafka brokers
   
   #### Add/change these properties in server.properties file
     1. broker.id=0
     2. listeners=PLAINTEXT://localhost:9092
     3. log.dirs=/tmp/kafka-logs
     4. auto.create.topics.enable=false
  ### copy poste the server.properties file. There should be 3 server files naming server.properties,server-1.properties and server-2.properties
  1. change broker id to 1 and 2 respectively
  2. change localhost to 9093 and 9094 
  3. change the log to 1 or 2 (log.dirs=/tmp/kafka-logs-1) (log.dirs=/tmp/kafka-logs-2)

### Start zookeeper and kafka server
#### zookeeper
1. C:\kafka_2.13-3.1.0>zookeeper-server-start.bat config\zookeeper.properties
#### kafka server
1. C:\kafka_2.13-3.1.0>kafka-server-start.bat config\server.properties
#### kafka server-1
1. C:\kafka_2.13-3.1.0>kafka-server-start.bat config\server-1.properties
#### kafka server-2
1. C:\kafka_2.13-3.1.0>kafka-server-start.bat config\server-2.properties
#### Connect with consumer without key
1. C:\kafka_2.13-3.1.0>kafka-console-consumer --bootstrap-server localhost:9092 --topic library-events



