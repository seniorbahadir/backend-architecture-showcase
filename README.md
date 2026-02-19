# Backend Architecture Showcase

Production-grade backend architecture examples built with .NET, focusing on reliability, security, and event-driven design.

This repository demonstrates real-world backend patterns including authentication systems, event-driven messaging, distributed caching, audit pipelines, and clean architectural layering.

---

## Purpose

This repository exists to showcase backend engineering practices used in modern distributed systems.

It focuses on:

- clean architecture
- event-driven communication
- secure authentication flows
- reliable data handling
- observable and maintainable backend systems

All examples reflect production-oriented design decisions.

---

## Architecture Principles

- Clean layering (API / Application / Domain / Infrastructure)
- Explicit contracts between layers
- Stateless services where possible
- Idempotent operations
- Failure-safe design
- Observability and auditability
- Security-first authentication flows

---

## Technology Stack

**Backend**
- .NET
- ASP.NET Core Web API
- Background Workers

**Messaging & Streaming**
- RabbitMQ
- Kafka
- Debezium (CDC)

**Caching**
- Redis

**Databases**
- SQL Server
- MongoDB
- PostgreSQL

**Authentication**
- JWT
- Refresh Token Rotation
- OTP-based authentication

**Real-time Communication**
- WebSocket

**Infrastructure**
- Docker
- Docker Compose

---

## Included Examples

### Authentication System
Demonstrates secure authentication flows including:

- JWT issuance and validation
- Refresh token rotation
- secure session lifecycle management

---

### Event-Driven Messaging
Demonstrates event-driven architecture using:

- RabbitMQ publishers and consumers
- reliable message processing
- decoupled service communication

---

### Distributed Caching
Demonstrates Redis integration for:

- performance optimization
- cache invalidation strategies
- reducing database load

---

### Audit Pipeline
Demonstrates audit/event ingestion pipeline:

- SQL Server → CDC → Debezium → Kafka
- Kafka Consumer → MongoDB
- event persistence for audit timelines

---

### MongoDB Data Provider
Demonstrates reusable MongoDB infrastructure including:

- DI-friendly design
- connection management
- clean abstraction layer

---

## Folder Structure
