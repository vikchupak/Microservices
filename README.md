# Microservices

__Saga Design Pattern__ (for managing Distributed Transactions)

ACID is important.

Distributed Transaction - transactions performed across more than one service - database or data repository (consists of __local trnsactions__). There are also __compensating transactions__ to revert the __local transactions__ done previously in case of failure.

There are two common saga implementation approaches, __choreography and orchestration__. 

https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/saga/saga
