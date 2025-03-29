# When does an architecture become Microservices?

***`If I use 2 monoliths behind a load balancer, is it still concidered to be monoliths architecture, not microservices one?`***

If you have **two identical monoliths** behind a **load balancer**, it is still considered a **monolithic architecture**, not **microservices**. Here’s why:  

### **✅ Why It’s Still Monolithic Architecture**
1. **Same Codebase & Functionality**  
   - Both monoliths are running **identical** copies of the same application.
   - This is essentially **horizontal scaling** of a monolith, not microservices.

2. **Tightly Coupled Components**  
   - If all business logic is inside a single application and different functionalities (e.g., authentication, payments, orders, etc.) are part of the same deployable unit, it remains a monolith.
   - Even if you scale it with multiple instances, the internal structure is still monolithic.

3. **Single Database (Usually)**  
   - If both monolith instances share the **same database**, they are not decoupled.
   - Microservices typically have **separate databases** per service.

4. **Deployment & Scaling**  
   - In a monolith, you **deploy the entire application** together.
   - Microservices allow **independent deployment** of each service.

---

### **🔄 When Does It Become Microservices?**
It would be considered **microservices architecture** only if:
✅ The application is split into **independent** services.  
✅ Each service **has its own database or data store** (not a shared monolithic DB).  
✅ Services **communicate via APIs** instead of direct function calls.  
✅ Each service **can be deployed independently** without affecting others.  

---

### **🛠 Example Scenarios**
| Scenario | Architecture Type |
|----------|------------------|
| **Two identical monoliths with a load balancer** | **Monolithic (just horizontally scaled)** |
| **A single monolith split into multiple deployable services** | **Microservices** |
| **A monolith with some functionality offloaded to microservices** | **Hybrid (Monolith + Microservices)** |
| **Multiple independent services, each with its own logic & database** | **True Microservices** |

---

### **🏆 Conclusion**
**Running multiple instances of a monolith behind a load balancer is still a monolithic architecture.** It is just **scaled horizontally** for better performance and availability, but the core architecture remains the same.
