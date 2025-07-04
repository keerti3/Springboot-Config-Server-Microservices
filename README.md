## Project: Springboot-Config-Server-Microservices

This project demonstrates a simple microservices architecture built using Spring Boot, Spring Cloud, and Netflix OSS components. It includes key features such as:

1. Client-side load balancing with Ribbon
2. Service discovery using Eureka
3. Distributed error tracing with Zipkin and Spring Cloud Sleuth
4. Monitoring and resiliency
5. Centralized configuration with Spring Cloud Config
6. Distributed messaging using Spring Cloud Bus and RabbitMQ
7. Fault tolerance with Hystrix

### Project Structure
The project consists of six Maven-based components:

**Microservices**
currency-conversion-service
This microservice depends on the currency-exchange-service to perform currency conversions.

**currency-exchange-service**
Provides exchange rate data used by the currency-conversion-service.

**limit-service**
A simple microservice whose configuration is managed by the Spring Cloud Config Server.

**Service Registry**
netflix-eureka-naming-server
Handles service registration and discovery so that microservices can locate each other dynamically.

**API Gateway**
netflix-zuul-api-gateway-server
Zuul serves as the API gateway that routes incoming requests to the appropriate microservices. It supports features such as dynamic routing, monitoring, and security.

**Configuration Server**
spring-cloud-config-server
Provides centralized configuration management for all microservices. Properties are version-controlled and can be refreshed across services.

**Supporting Components and Features**
Client-Side Load Balancing
Implemented using Netflix Ribbon, allowing microservices to communicate efficiently through Eureka-based service discovery.

**Distributed Error Tracing**
Achieved using Spring Cloud Sleuth and Zipkin, with RabbitMQ used as the transport mechanism for trace data.

**Distributed Messaging**
Implemented through Spring Cloud Bus, enabling real-time configuration updates across microservices.

**Fault Tolerance**
Handled using Hystrix, which enables fallback methods and ensures resilience during service failures.
