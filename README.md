# 🚀 **Project: Springboot-Config-Server-Microservices**

[![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)](https://www.oracle.com/java/)
[![Netflix OSS](https://img.shields.io/badge/Netflix-OSS-E50914?style=for-the-badge&logo=netflix&logoColor=white)](https://netflix.github.io/)

---

### 📖 Overview

This project demonstrates a microservices architecture using **Spring Boot**, **Spring Cloud**, and **Netflix OSS** components. It showcases a fully modular system with centralized configuration, fault tolerance, load balancing, and service discovery.

---

### 🧩 Key Features

1. **Client-side Load Balancing** with Ribbon  
2. **Service Discovery** using Eureka  
3. **Centralized Configuration** with Spring Cloud Config Server  
4. **API Gateway** using Netflix Zuul  
5. **Distributed Messaging** via Spring Cloud Bus and RabbitMQ  
6. **Error Tracing & Monitoring** with Zipkin and Spring Cloud Sleuth  
7. **Fault Tolerance** with Hystrix

---

### 📁 Project Structure

This system is composed of **six Maven-based components**:

#### 🟢 Microservices

- **`currency-conversion-service`**  
  Consumes exchange rates from the `currency-exchange-service` and handles currency conversion logic.

- **`currency-exchange-service`**  
  Provides real-time exchange rate data and registers itself with Eureka.

- **`limit-service`**  
  A sample microservice using externalized config from Spring Cloud Config Server.

#### 🧭 Service Registry

- **`netflix-eureka-naming-server`**  
  Handles dynamic service registration and discovery.

#### 🚪 API Gateway

- **`netflix-zuul-api-gateway-server`**  
  Routes external requests to internal microservices with support for filtering, logging, and monitoring.

#### 🛠️ Configuration Server

- **`spring-cloud-config-server`**  
  Provides centralized and version-controlled configuration to all services. Config data is sourced from a Git-based repo.

---

### 🔌 Supporting Components

- **Ribbon + Eureka:** Enables load-balanced communication between microservices  
- **Spring Cloud Sleuth + Zipkin + RabbitMQ:** Distributed tracing and event transport for debugging and monitoring  
- **Spring Cloud Bus:** Real-time config refresh across services using message broker  
- **Hystrix:** Fallback methods and circuit breakers for fault tolerance

---

### 🚀 Getting Started

1. Clone the repository and run `mvn clean install` for each module  
2. Start services in the following order:  
   - `spring-cloud-config-server`  
   - `netflix-eureka-naming-server`  
   - `netflix-zuul-api-gateway-server`  
   - All other microservices

3. Make API calls through the API Gateway to access services

---

### 📈 Future Enhancements

- Add OAuth2/JWT-based authentication and role-based access  
- Integrate monitoring dashboards with Spring Boot Admin or Prometheus  
- Add Docker support for containerization and deployment

---
