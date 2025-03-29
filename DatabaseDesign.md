# Microservices Architecture

- https://microservices.io/patterns/microservices.html

# Database Design in a Microservices Architecture

- https://www.baeldung.com/cs/microservices-db-design

---

- Database **(server)** per service
  - https://microservices.io/patterns/data/database-per-service.html
  - https://learn.microsoft.com/en-us/dotnet/architecture/cloud-native/distributed-data#database-per-microservice-why
  - Some business transactions need to span multiple services (Distributed transaction). Solution:
      - Saga pattern **(eventual consistency)**
        - Choreography - each local transaction publishes domain events that trigger local transactions in other services
        - Orchestration - an orchestrator (object) tells the participants what local transactions to execute
      - 2 Phase Commit (2PC) protocol. Generally not recommended in modern microservices architectures. **(strong consistency)**
- Shared **(server)** database (considered to be anti-pattern)
  - https://microservices.io/patterns/data/shared-database.html
  - Uses the same database server, but each service gets its own database inside server

