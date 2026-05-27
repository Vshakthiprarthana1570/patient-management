# Patient Management System

# Patient Management System – Project Summary

**Patient Management System** is a cloud-native microservices application built with Spring Boot 3.4, designed to manage patient records, billing, and analytics with enterprise-grade security.

## Core Services

- **Patient Service** (Port 4000): RESTful API for patient CRUD operations with JPA persistence, email validation, and UUID-based identification
- **Auth Service** (Port 4007): JWT-based authentication and token validation with Spring Security
- **Billing Service** (Port 4001): Billing account management exposed via gRPC for inter-service communication
- **Analytics Service** (Port 4002): Event-driven analytics processor consuming patient events from Kafka
- **API Gateway** (Port 4004): Spring Cloud Gateway routing all client requests with JWT validation filter; blocks unauthenticated traffic

## Key Features

- **Distributed Architecture**: Independent deployable services with clear separation of concerns
- **Security**: JWT token-based authentication through the gateway; auth-service validates tokens for protected endpoints
- **Event-Driven**: Kafka integration in analytics-service for asynchronous patient event processing
- **RPC Communication**: gRPC used for billing-service inter-service calls
- **Database**: PostgreSQL support with H2 option for local development
- **Containerization**: Docker images and Dockerfiles for each service; ready for Kubernetes or Docker Compose deployment

## Tech Stack

Java 17 | Spring Boot 3.4 | Maven | PostgreSQL/H2 | Kafka | gRPC | JWT | Docker
