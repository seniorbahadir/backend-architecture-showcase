# Backend Architecture Showcase

Production-grade backend architecture showcase built with .NET, focused on authentication, event-driven systems, audit pipelines, and reliability patterns.

This repository serves as a structured engineering portfolio demonstrating backend system design principles used in modern distributed applications.

---

## Purpose

The goal of this repository is to showcase how production-ready backend systems are designed, structured, and implemented.

It focuses on:

- authentication and session management
- event-driven communication between services
- distributed caching strategies
- audit and event pipelines
- clean architecture and maintainable system design
- reliability, observability, and failure-safe patterns

This repository is intentionally structured as an engineering showcase rather than a single application.

---

## Architecture Overview

```mermaid
flowchart LR

Client --> Gateway[API Gateway]

Gateway --> AuthService[Auth Service]
Gateway --> AppService[Application Service]

AuthService --> SQL[(SQL Server)]
AppService --> SQL

SQL --> Debezium[Debezium CDC]
Debezium --> Kafka[(Kafka)]

Kafka --> AuditConsumer[Audit Consumer]

AuditConsumer --> Mongo[(MongoDB)]

AppService --> Redis[(Redis Cache)]
AppService --> RabbitMQ[(RabbitMQ)]
