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

## Prerequisites
* Need to install metamask browser extension and create an account.
* Once account is ready, you need to add some ether balance using Rinkeby Authenticated Faucet.
* Node - v10.x.x (preferrably v10.15.0 for long term support)
* npm - v6.x.x (preferrably v6.6.0)

## Tools used:
1. kafka: 
   * Solidity: Ethereum's smart contract programming language.
   * Remix: IDE, used for smart contract development.
   * Metamask: MetaMask is a software cryptocurrency wallet used to interact with the Ethereum blockchain
1. Frontend: 
   * Web3.js: Javascript library used to interact with the Ethereum blockchain
   * React.js: Javascript library for frontend development.
## To Run
* *num run server*
* Go to browser at address http://localhost:3000 to access the web page.
