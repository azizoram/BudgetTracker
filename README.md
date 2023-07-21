# Budget Tracker Manager
Budget Tracker Manager is a comprehensive web application developed using Java 17, Spring Boot, and React.js. The primary goal of the application is to help users manage their finances efficiently, track transactions, and maintain budget limits. It provides a user-friendly interface for handling financial data and receiving notifications when budget limits are exceeded.

## Technologies Used
### Backend

* Java 17.
* Spring Boot.
* PostgreSQL (Relational Database for Transactions, User, Category, Wallet).
* MongoDB (NoSQL Database for Notifications).
* Hazelcast (Used for caching transactions and categories).
* Docker (Application settings are defined in docker-compose.yml with 2 servers and 2 databases).
* Axios (Used for making HTTP requests between Frontend and Backend).
* Hazelcast used for Transactions and Category. 

### Frontend

* React.js

### Cache
* Hazelcast (Used for caching transactions and categories).

### Docker
* All application settings are defined in docker-compose.yml.
* 2 servers and 2 databases (PostgreSQL and MongoDB) and Dispatcher are presented as containers and images, all located in one Docker network.

### Messaging
* Apache Kafka (Message broker used for sending budget limit exceeded emails through Mailgun).

### ElasticSearch
* Used for searching transactions by description.

### Authorization
* Basic Authorization is used for user authentication.

### Interceptors
* Requests information is logged in the console using interceptors.

### Paterns Used
* DTO (Data Transfer Objects) for Responses
* Builder Pattern for Transaction creation
* MVC (Model-View-Controller) pattern for the architecture
* DAO (Data Access Object) pattern for data retrieval
* Proxy Pattern for the Dispatcher

### REST API

* Application uses REST API endpoints in Controllers for communication between the user and the Dispatcher and servers.

## Project Setup

### Backend
1) Start PostgreSQL and MongoDB:

       docker-compose up postgres mongo
2) Start the Dispatcher, servers, Zookeeper, and Kafka:
   
       docker-compose up dispatcher server server-2 zookeeper kafka

### Frontend
1) Change directory to the frontend:
   
       cd fe

2) Start the React.js application:

       npm start


## Team
The project was completed in collaboration with the following team members:

- Arlan Nurkhozhin
- Azizov Ramir
- Lezhnev Evgenii
- Sadyraliyev Dastan
- Tsay Vyacheslav 
