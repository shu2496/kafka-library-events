## Kafka Spring Boot producer consumer application using H2 in-memory database
**Two applications, one for library-event-producer and another for library-event-consumer.**

##Details
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
     1. broker.id=1
     2. listeners=PLAINTEXT://localhost:9092
     3. log.dirs=/tmp/kafka-logs-1
     4. auto.create.topics.enable=false
  #### first copy poste the server.properties file. There should be 3 server files naming server.properties,server-1.properties and server-2.properties
