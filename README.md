# 🏋️ Fitness App Microservices

🚀 A scalable **Microservices-based Fitness Recommendation System** built using **Spring Boot, Kafka, Eureka, API Gateway, and AI integration (Gemini API)**.

---

## 📌 Project Overview

This project is designed to demonstrate a **real-world microservices architecture** where multiple services communicate asynchronously using Kafka and are managed via service discovery.

The system provides:

* User management
* Activity tracking
* AI-based fitness recommendations

---

## 🏗️ Architecture

### 🔹 Components:

* **API Gateway** → Entry point for all client requests
* **User Service** → Manages user data
* **Activity Service** → Tracks user activities
* **AI Service** → Generates recommendations using Gemini API
* **Kafka** → Event-driven communication between services
* **Eureka Server** → Service discovery
* **Config Server** → Centralized configuration
* **Database** → Each service has its own DB (Microservices principle)

📊 Flow:

1. Client (Postman/Frontend) sends request to API Gateway
2. Gateway routes request to respective service
3. Activity Service publishes events to Kafka
4. AI Service consumes events from Kafka
5. AI Service calls Gemini API and stores recommendations
6. Response is sent back via Gateway

---

## 🧰 Tech Stack

* **Backend**: Spring Boot, Spring Cloud
* **Microservices Tools**: Eureka, API Gateway, Config Server
* **Messaging Queue**: Apache Kafka
* **Database**: MySQL
* **AI Integration**: Gemini API
* **Build Tool**: Maven

---

## 🔐 Authentication

* Authentication is handled using **Keycloak**
* ⚠️ Note: Keycloak integration and frontend were implemented by a team member

---

## 📂 Project Structure

```
fitness-app-microservices/
│
├── api-gateway/
├── user-service/
├── activity-service/
├── ai-service/
├── config-server/
├── eureka-server/
└── kafka-config/
```

---

## ⚙️ Setup & Run Locally

### 🔹 Prerequisites

* Java 17+
* Maven
* MySQL
* Kafka & Zookeeper

### 🔹 Steps

1. Clone the repository

```bash
git clone https://github.com/SunnySingh0001/fitness-app-microservices.git
cd fitness-app-microservices
```

2. Start services in order:

* Config Server
* Eureka Server
* Kafka & Zookeeper
* All Microservices

3. Run API Gateway

---

## 🔄 Kafka Flow Example

* Activity Service → Produces event (User workout data)
* Kafka → Message broker
* AI Service → Consumes event and generates recommendation

---

## 💡 Features

✔️ Microservices Architecture
✔️ Event-driven communication (Kafka)
✔️ AI-powered recommendations
✔️ Scalable & loosely coupled design
✔️ Service Discovery (Eureka)

---

## 🚀 Future Improvements

* Complete Keycloak integration
* Frontend dashboard
* Docker & Kubernetes deployment
* CI/CD pipeline (Jenkins)

---

## 👨‍💻 Author

**Sunny Singh/Yuvraj Vardhan/Satyam Gupta**

* Java Backend Developer
* Spring Boot & Microservices Enthusiast

---

## ⭐ Contribute

Feel free to fork this repo and improve it!

---

## 📌 Note

This project is built for **learning and interview demonstration purposes** to showcase real-world microservices architecture.

