__Saga Design Pattern__ (introduced to solve problems of managing Distributed Transactions)

https://stackoverflow.com/questions/56720868/what-does-saga-stand-for

ACID is important.

Distributed Transaction - transactions performed across more than one service - database or data repository (consists of __local trnsactions__). There are also __compensating transactions__ to revert/rollback the __local transactions__ done previously in case of failure.

There are two common saga implementation approaches, __choreography and orchestration__.

Orchestration uses a state machine to manage transactions (tasks).

https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/saga/saga \
https://www.geeksforgeeks.org/saga-design-pattern \
https://docs.aws.amazon.com/prescriptive-guidance/latest/cloud-design-patterns/saga.html

API gateway

https://highload.today/api-gateway-endpoints \
https://habr.com/ru/articles/557004/

![image](https://github.com/VIK2395/Microservices/assets/50545334/cd32dc8e-ce89-4ab0-923c-53e3c894dcc1)
