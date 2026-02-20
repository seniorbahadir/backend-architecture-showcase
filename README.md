Backend Architecture Showcase

Production-grade backend architecture showcase built with .NET, focused
on authentication, event-driven systems, audit pipelines, and
reliability patterns.

This repository serves as a structured engineering portfolio
demonstrating backend system design principles used in modern
distributed applications.

  --------------------------------------------------
  Purpose
  --------------------------------------------------
  Architecture Overview

  Client → API Gateway → Auth Service → SQL Server
  Client → API Gateway → Application Service → SQL
  Server

  SQL Server → Debezium CDC → Kafka → Audit Consumer
  → MongoDB

  Application Service → Redis Cache Application
  Service → RabbitMQ
  --------------------------------------------------

What this repository demonstrates

-   JWT authentication and refresh token rotation
-   OTP-based authentication flows
-   event-driven messaging with RabbitMQ
-   audit pipelines using CDC → Debezium → Kafka → MongoDB
-   distributed caching with Redis
-   real-time communication patterns
-   clean architecture layering
-   service isolation and contract-driven design
-   failure-safe and idempotent backend operations

  --------------------------------------------------
  Technology Stack
  --------------------------------------------------
  Repository Structure

  backend-architecture-showcase/ adr/ diagrams/
  docs/ samples/ showcase/ docker-compose.yml
  --------------------------------------------------

Current Status

This repository currently contains the architectural skeleton and
documentation structure.

Implementation examples are being added incrementally to demonstrate
production-grade backend patterns.

  -------------------------------------------------------
  Design Principles
  -------------------------------------------------------
  Author

  Bahadır Kayhan Mid .NET Backend Engineer

  LinkedIn:
  https://www.linkedin.com/in/bahadir-kayhan-31a55a1b2/
  GitHub: https://github.com/seniorbahadir/
  -------------------------------------------------------

Engineering Philosophy

Secure by design. Reliable by default. Maintainable by intent.
