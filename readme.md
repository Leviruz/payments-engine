# Fintech Backend Portfolio Project

A production-inspired backend system designed to demonstrate advanced
engineering practices, system design, and scalability patterns.

---

## Project Overview

This project simulates a **Fintech Payment Processing System** capable of:

- Managing users and wallets
- Processing payments with idempotency guarantees
- Handling asynchronous workflows via message queues
- Ensuring transactional consistency
- Providing observability and security

The goal is to showcase **real-world backend architecture**, not just CRUD.

---

## Architecture

- API Layer (Controllers)
- Application Layer (Use Cases)
- Domain Layer (Business Rules)
- Infrastructure Layer (DB, Queue, External Services)

Detailed diagrams available in:  
`./docs/diagrams`

Architecture decisions (ADR):  
`./docs/adr`

---

## Repository Structure

| Directory          | Purpose                                 |
|------------------|---------------------------------------|
| docs/diagrams    | Architecture diagrams                 |
| docs/adr         | Architecture Decision Records         |
| src/domain       | Core business logic                   |
| src/application  | Use cases                            |
| src/infrastructure | External systems & persistence      |
| src/interfaces   | API layer                            |
| tests            | Unit & integration tests             |
| docker           | Container setup                      |

Full project structure and workflow:  
`./docs/project-guide.md`

---

## Running the Project

```bash
docker-compose up --build
```

## Testing

```bash
npm test
```

## Engineering Practices
- Clean Architeture
- Domain-Driven Design
- Event-driven processing
- Idempotent operations
- CI/CD pipelines

