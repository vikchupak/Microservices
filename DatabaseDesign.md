# Database Design in Microservices Architecture

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

# Horizontal database scaling (sharding)

- The practice of adding more database **servers(shards)**
- The main problem with horizontally scaling SQL databases is that data is split **across different servers**
- Sharding separates large databases into smaller, more easily managed parts called shards
   - Each shard shares the **same schema**, though the **actual data on each shard is unique** to the shard
- Once a database has been sharded across multiple servers, it is **hard to perform join** operations across database shards

---

Horizontal scaling (sharding) of SQL databases is considered difficult or even impossible in some cases because traditional SQL databases are designed for strong consistency and ACID (Atomicity, Consistency, Isolation, Durability) transactions. These features make distributing data across multiple servers complex. If strict consistency and complex queries are needed, horizontal scaling requires extra engineering effort.
