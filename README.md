<div style="font-family: 'Times New Roman', Times, serif;">

# Midas Core

Midas Core is a backend system built using Spring Boot that processes financial transactions.  
The main idea of this project is to show how real-world backend systems work using Kafka, databases, APIs, and REST endpoints.

---

## Overview

This system receives transactions, validates them, processes them, and stores the results.  
It also allows users to check their account balance.

Flow of the system:

Frontend → Kafka → Midas Core → Database → Incentive API → REST API

---

## Features

- Uses Kafka to handle transactions asynchronously  
- Validates transactions before processing  
- Stores data using H2 database and JPA  
- Connects to an external Incentive API  
- Provides a REST API to check user balance  

---

## How it works

1. A transaction is sent to Kafka  
2. Midas Core reads the transaction  
3. It checks if the sender and receiver exist  
4. It verifies that the sender has enough balance  
5. It calls the Incentive API  
6. The recipient receives the amount + incentive  
7. The transaction is saved in the database  

---

## Technologies used

- Java 17  
- Spring Boot  
- Apache Kafka  
- H2 Database  
- Spring Data JPA  
- REST APIs  

---

## API Endpoint

GET /balance?userId={id}

Example response:

{
  "balance": 500.0
}

If the user does not exist, the balance returned is 0.

---

## Key concepts

- Kafka is used to separate frontend and backend  
- JPA helps in handling database operations easily  
- REST API is used for communication between systems  
- The system is designed to be scalable and easy to modify  

---

## Final thoughts

This project helped me understand how backend systems handle real-world problems like transaction processing, validation, and system integration.

---

Developed by Deven Borse

</div>
