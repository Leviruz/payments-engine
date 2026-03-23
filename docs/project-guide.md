# Project Overview

This file contains informations about the project practices, including folder structure, commit patterns, github issue-oriented roadmap and infos

# Repository Structure

    /docs
      /diagrams
      /adr
    /src
      /domain
      /application
      /infrastructure
      /interfaces
    /tests
    /docker
    /.github
      /workflows
    README.md
    docker-compose.yml

### Description

| Directory          | Purpose                                 |
| ------------------ | --------------------------------------- |
| docs/diagrams      | Architecture diagrams and flow diagrams |
| docs/adr           | Architecture Decision Records           |
| src/domain         | Business entities and core rules        |
| src/application    | Use cases and business services         |
| src/infrastructure | Database, queues, external integrations |
| src/interfaces     | Controllers and API layer               |
| tests              | Unit and integration tests              |
| docker             | Container configuration                 |
| .github/workflows  | CI/CD pipelines                         |

# GitHub Project Management Strategy

The project follows a structured workflow using:

- Milestones
- Issues
- Sub-issues
- Semantic commits
- Architecture documentation

### Semantic Commit Patterns

| Type     | When to use                                                           | Example                                     |
| -------- | --------------------------------------------------------------------- | ------------------------------------------- |
| feat     | When adding a new feature                                             | feat: add user authentication               |
| fix      | When fixing a bug                                                     | fix: correct login validation error         |
| docs     | Changes to documentation only                                         | docs: update README with setup instructions |
| style    | Code style changes (formatting, semicolons, spacing, no logic change) | style: format code with prettier            |
| refactor | Code changes that neither fix a bug nor add a feature                 | refactor: simplify user service logic       |
| perf     | Performance improvements                                              | perf: optimize database queries             |
| test     | Adding or updating tests                                              | test: add unit tests for auth service       |
| build    | Changes that affect the build system or dependencies                  | build: update dependencies                  |
| ci       | Changes to CI/CD configuration                                        | ci: update GitHub Actions workflow          |
| chore    | Other changes that don't modify src or test files                     | chore: update .gitignore                    |
| revert   | Revert a previous commit                                              | revert: revert "feat: add payment gateway"  |

# Project management

the project will be managed in a Github repository/project, using kanban boards along with milestones and issues to track the work schedule

---

# Issue Writing Standard

Each issue should follow a structured format.

### Example Issue

**Title**

    Implement Payment Processing Service

**Description**

    Context:
    We need a service responsible for handling payment creation and status updates.

    Requirements:
    - Validate wallet balance
    - Support idempotency keys
    - Persist payment with pending status
    - Publish event to message queue

    Acceptance Criteria:
    - Payment is created successfully
    - Duplicate idempotency key returns existing payment
    - Unit tests cover main flows

---

# Milestones

## Milestone Example:

description:
Implement the core payment engine, according to {requirements}
to achieve {goal}

Issues:

- issue 01
- issue 02
- issue 03

## Milestone 1 --- Core Payment Engine

Issues:

- Setup project structure
- Configure Docker environment
- Implement User entity
- Implement Wallet entity
- Implement Payment entity
- Implement Payment Service
- Create database schema
- Implement idempotency key mechanism
- Add unit tests for core services

---

## Milestone 2 --- Persistence and Transactions

Issues:

- Implement database transactions
- Add indexes for performance optimization
- Handle concurrency edge cases
- Improve application logging

---

## Milestone 3 --- Asynchronous Processing

Issues:

- Integrate message queue
- Implement payment worker
- Implement retry strategy
- Handle duplicate message processing

---

## Milestone 4 --- Security Layer

Issues:

- Implement JWT authentication
- Add refresh tokens
- Implement password hashing
- Add rate limiting
- Implement input validation middleware

---

## Milestone 5 --- Observability and Production Readiness

Issues:

- Add structured logging
- Implement correlation IDs
- Add health check endpoint
- Add metrics endpoint

---

## Milestone 6 --- Deployment and Documentation

Issues:

- Configure CI pipeline
- Add GitHub Actions workflow
- Deploy application to AWS
- Write system design document
- Create architecture diagrams
- Finalize README documentation

# Engineering Practices Demonstrated

This project demonstrates:

- Clean Architecture
- Domain-driven design principles
- Event-driven processing
- Idempotent financial operations
- Transactional data integrity
- API security practices
- Containerized deployment
- Continuous Integration pipelines
- Architecture documentation

# Future Improvements

Potential improvements include:

- Distributed tracing
- Kubernetes deployment
- Advanced rate limiting
- Multi-region deployment
- Fraud detection simulation
- Event sourcing architecture

# Author

Levir Melo Software Engineer focused on distributed backend systems,
fintech platforms, and cloud-native architectures.
