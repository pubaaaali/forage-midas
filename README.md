# JP Morgan Chase - Advanced Software Engineering Virtual Experience

## Overview
Completed the JP Morgan Chase Advanced Software Engineering Virtual Experience Program on Forage. Built a backend transaction processing system using Spring Boot, Kafka, H2 Database, and REST APIs.

## Tasks Completed

### Task 1: Project Setup
- Configured a Spring Boot project with Maven
- Added dependencies for Spring Data JPA, Kafka, H2, and Testcontainers

### Task 2: Kafka Integration
- Implemented a Kafka listener to consume transaction messages
- Configured JSON deserialization for incoming transaction data

### Task 3: H2 Database Integration
- Integrated an H2 in-memory database using Spring Data JPA
- Implemented transaction validation (valid sender/recipient, sufficient balance)
- Created TransactionRecord entity with many-to-one relationships
- Persisted valid transactions and updated user balances

### Task 4: Incentive API Integration
- Integrated an external REST API for transaction incentives
- Used RestTemplate to communicate with the Incentive API
- Applied incentive amounts to recipient balances

### Task 5: Balance REST API
- Built a REST controller exposing a GET /balance endpoint
- Returns user balance by userId in JSON format

## Tech Stack
- **Java 17**
- **Spring Boot 3.2.5**
- **Apache Kafka** (message queue)
- **H2 Database** (in-memory SQL)
- **Spring Data JPA** (database abstraction)
- **REST APIs** (Spring Web)
- **Maven** (build tool)
- **Testcontainers** (integration testing)

## How to Run
```bash
# Build the project
mvn clean install

# Start the incentive API
java -jar services/transaction-incentive-api.jar

# Run the application
mvn spring-boot:run
```

