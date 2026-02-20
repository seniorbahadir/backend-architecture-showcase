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
What this repository demonstrates

This repository demonstrates backend engineering patterns including:

JWT authentication and refresh token rotation

OTP-based authentication flows

event-driven messaging with RabbitMQ

audit pipelines using CDC → Debezium → Kafka → MongoDB

distributed caching with Redis

real-time communication patterns

clean architecture layering

service isolation and contract-driven design

failure-safe and idempotent backend operations

Technology Stack

Backend

.NET

ASP.NET Core Web API

Background Workers

Messaging & Streaming

RabbitMQ

Kafka

Debezium (CDC)

Caching

Redis

Databases

SQL Server

MongoDB

PostgreSQL

Authentication

JWT

Refresh Token Rotation

OTP Authentication

Infrastructure

Docker

Docker Compose

Repository Structure
backend-architecture-showcase/

adr/
Architecture decision records

diagrams/
System architecture diagrams

docs/
Architecture and design documentation

samples/
Example payloads and contracts

showcase/
Architecture showcase modules (auth, messaging, caching, audit pipeline)

docker-compose.yml
Infrastructure definition for local development
Current Status

This repository currently contains the architectural skeleton and documentation structure.

Implementation examples are being added incrementally to demonstrate production-grade backend patterns.

Design Principles

This repository prioritizes:

reliability over shortcuts

clarity over cleverness

maintainability over complexity

explicit system design over implicit behavior

Author

Bahadır Kayhan
Mid .NET Backend Engineer

LinkedIn
https://www.linkedin.com/in/bahadir-kayhan-31a55a1b2/

GitHub
https://github.com/seniorbahadir/

Engineering Philosophy

Secure by design.
Reliable by default.
Maintainable by intent.


---

# Bu README neden doğru?

Bu versiyon:

- iskelet repo için doğru positioning yapar
- içerik eksik olsa bile “intent” gösterir
- recruiter’a yanlış signal vermez
- architecture-level thinking gösterir
- senior engineer’ların saygı duyacağı formatta

---

# Bir sonraki en kritik adım (önem sırası)

1. showcase/auth-system klasörü ekle  
2. showcase/rabbitmq klasörü ekle  
3. showcase/redis klasörü ekle  

İstersen sana hangi klasörü önce eklemenin en çok etki yaratacağını da öncelik sırasıyla söyleyebilirim.
::contentReference[oaicite:0]{index=0}
