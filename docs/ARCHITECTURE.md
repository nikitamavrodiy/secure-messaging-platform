## Architectural Style

Modular Monolith:
- Cleanly separated feature modules
- Single deployable Spring Boot application
- External services: PostgreSQL, Redis

## Architecture Decision Rationale

A modular monolith was chosen to maintain simplicity while enforcing clean separation of features.
This allows scalable architecture without premature microservice complexity.
