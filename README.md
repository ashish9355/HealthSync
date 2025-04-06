# 🏥 Healthsync – Scalable Microservices-Based Healthcare Platform

**Healthsync** is a production-grade healthcare platform architected with **Spring Boot**, **Docker**, **gRPC**, **Kafka**, and **AWS**. Designed using microservices principles, it ensures high modularity, scalability, and cloud-native deployment capabilities.

---

## 📐 Architecture Overview

![Architecture Diagram](docs/architecture.png)

- **Microservices**: 5+ independently deployable services  
- **Communication Protocols**: REST, gRPC, Kafka  
- **Security**: OAuth2.0, JWT, Role-Based Access Control  
- **Infrastructure**: AWS-ready with Docker, LocalStack, and CloudFormation

---

## 📌 Key Features

- ⚙️ **Microservices Architecture** – Modular services (Patient, Auth, Billing, Analytics, API Gateway) with separation of concerns  
- 🚀 **Multi-Protocol Communication** – REST via OpenAPI 3.0, high-performance gRPC, and asynchronous Kafka messaging  
- 🔐 **Secure Authentication** – OAuth2.0 with JWT-based access control using Spring Security  
- ☁️ **Cloud-Native Infrastructure** – Dockerized services deployable on AWS ECS/RDS/MSK (mocked via LocalStack)  
- 📊 **Real-Time Analytics** – Kafka consumers track patient lifecycle events for reporting  
- 📄 **API Documentation** – Swagger UI + gRPC Protobuf contracts for easy consumption  

---

## 🛠️ Tech Stack

| Category     | Stack                                                                 |
|--------------|-----------------------------------------------------------------------|
| **Backend**  | Java 21, Spring Boot 3 (Web, Data JPA, Security, Cloud Gateway), gRPC |
| **Database** | PostgreSQL, Hibernate, Flyway                                         |
| **Messaging**| Apache Kafka                                                          |
| **DevOps**   | Docker, AWS (via LocalStack), CloudFormation (IaC)                    |
| **Auth**     | JWT, Spring Security, OAuth2.0                                        |
| **API**      | REST (OpenAPI 3.0), gRPC (Protocol Buffers)                           |

---

## 🚀 Quick Start

### ✅ Prerequisites

- Java 21  
- Docker + Docker Compose  
- Maven  
- AWS CLI (for LocalStack)  

---

### 1. 📦 Run Services Locally

```bash
# Start dependencies (PostgreSQL, Kafka, etc.)
docker-compose -f docker-compose.local.yml up

# Build all microservices
mvn clean install

# Run individual service (e.g., Patient)
java -jar patient-service/target/*.jar
