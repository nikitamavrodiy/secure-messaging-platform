## Architectural Style

The system is designed as a modular monolith, where all core components are deployed as a single Spring Boot application with clearly separated internal modules.

## Architecture Decision Rationale
It's chosen to balance:
- System simplicity (single deployment unit)
- Clear separation of concerns/features (modular internal design)
- Controlled scalability (via Redis and stateless design principles)
- Reduced architectural overhead compared to microservices

## High-Level Structure
- Authentication Module (User login and session handling)
- Messaging Module (Private and group messaging)
- Group Management Module (Chat room handling)
- Persistence Layer (Data storage and retrieval)

## External infrastructure components:
- PostgreSQL (persistent storage)
- Redis (real-time message distribution support)

## 1. Alignment with Functional Requirements
FR-1 to FR-3 require secure authentication and session handling → fits centralized Auth module

FR-4 and FR-5 require real-time private and group messaging → fits unified Messaging module

FR-6 requires group management → supports modular separation within same system boundary

FR-8 and FR-9 require message persistence and retrieval → centralized data layer fits monolith design


## 2. Alignment with Non-Functional Requirements
Maintainability (NFR-7): Modular internal structure ensures components can evolve independently without affecting the whole system.

Scalability (NFR-5): Redis-based messaging layer supports scaling communication flow while keeping core system simple.

Performance (NFR-3): Single-deployment architecture reduces inter-service communication overhead.

Reliability (NFR-4): Monolithic consistency simplifies message flow control and reduces distributed failure points.

Security (NFR-1, NFR-2): Centralized authentication and access control simplify enforcement of secure messaging rules.

Portability (NFR-9): Single deployable artifact ensures easy environment portability.
