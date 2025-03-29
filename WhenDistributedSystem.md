# Distributed system

A **distributed system** is a system in which multiple independent computers (nodes) work together to achieve a common goal. These nodes communicate over a network and coordinate their actions. The key characteristics of distributed systems are:  

- **Decentralization** – No single node has a complete view or control over the system.  
- **Scalability** – The system can grow by adding more nodes.  
- **Fault Tolerance** – The system continues to operate even if some nodes fail.  
- **Concurrency** – Multiple components execute independently.  

# **Are Two Monoliths Behind a Load Balancer a Distributed System?**  
No, simply running **two instances of a monolith behind a load balancer** does **not** necessarily make it a **distributed system**.  

Here’s why:  
- **Shared State?** If both monoliths connect to a single database, then they are just replicas rather than truly distributed.  
- **No Decentralization** – A distributed system usually has independent nodes managing their own parts of the data or logic.  
- **No Inter-Node Communication** – If the monoliths don’t talk to each other or coordinate actions, it’s just horizontal scaling.  

However, if these two instances manage different parts of the application, maintain separate databases, or **communicate with each other to coordinate tasks**, then it could be considered a **basic** form of distributed system.  
