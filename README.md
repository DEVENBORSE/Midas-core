<div style="font-family: 'Times New Roman', Times, serif;">

# 💰 Midas Core

Midas Core is a backend system built using Spring Boot that processes financial transactions.  
This project was developed as part of the **JPMorgan Chase Virtual Internship (Forage)** and demonstrates how real-world backend systems work using Kafka, databases, APIs, and REST endpoints.

---

## 📌 Overview

This system receives transactions, validates them, processes them, and stores the results.  
It also allows users to check their account balance.

🔁 Flow of the system:

Frontend → Kafka → Midas Core → Database → Incentive API → REST API

---

## 🚀 Features

- 🔁 Kafka-based asynchronous transaction processing  
- ✅ Transaction validation before processing  
- 💾 Data storage using H2 database and JPA  
- 🎯 Integration with external Incentive API  
- 🌐 REST API to check user balance  

---

## ⚙️ How it works

1. 📥 A transaction is sent to Kafka  
2. 📡 Midas Core reads the transaction  
3. 🔍 It checks if sender and receiver exist  
4. 💰 It verifies sender has enough balance  
5. 🌐 Calls the Incentive API  
6. ➕ Recipient gets amount + incentive  
7. 🗄️ Transaction is saved in database  

---

## 🧰 Technologies used

- ☕ Java 17  
- 🌱 Spring Boot  
- 📨 Apache Kafka  
- 🗄️ H2 Database  
- 🔗 Spring Data JPA  
- 🌍 REST APIs  

---

## 🌐 API Endpoint

GET /balance?userId={id}

📥 Example response:

{
  "balance": 500.0
}

👉 If the user does not exist, the balance returned is 0.

---

## 🧠 Key concepts

- 🔄 Kafka helps decouple frontend and backend  
- 🧩 JPA simplifies database operations  
- 🌐 REST APIs enable communication between services  
- 📈 System is scalable and easy to extend  

---

## 🎯 Final thoughts

This project helped me understand how backend systems handle real-world problems like transaction processing, validation, and system integration.

---

👨‍💻 Author

Developed by Deven Borse  
🎓 JPMorgan Chase Virtual Internship (Forage)

</div>
