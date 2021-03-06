### Hi there 👋, I am Bharath

- I am software engineer, previously worked for Zoho Corporation for 4 years.
- Right now, I am looking for an opportunity as a software developer.

### Rentpal
This repository primarily focuses on my personal project "rentpal", the objective of the project is to leverage exisiting concept electronic signature to share rental agreements between owners and the tenants. With this project, I am hoping there is a conversation to utilize e-sign to transfer any form legal documents as opposed to having paper based documents. Out of the 17 billion cubic feet of trees deforested each year, over 60% are used to make paper. Obviously, we cannot eradicate paper usage completely but we can slow move away from paper based legal documents. 

#### System Design
    
![rentpal architecture](https://user-images.githubusercontent.com/49817583/111836725-0ceb9f00-88f7-11eb-83de-26cf3450a5b2.png)

#### Monolithic vs Microservices
The pain points of monolithic are,
- tightly coupled, for a small change of code be it front end or backend, the whole application must be redeployed and if the system goes down, there is 100% failure.
- monolithic comprises many services, all these services must be written in the same language, there is no choice of choosing different tech stack according to the services.
- ineffective resource utilization, the whole application must be scaled just for few time-consuming services.

On the other hand, microservices overcomes the constraints in monolith architecture.
- each microservices can be scaled and deployed independently according to the requirement.
- can utilize different tech stack for each microservices.
- minimal failure, even if a microservice down, the whole system is not comprised.

Microservice could be challenging if it not designed properly,
- design the microservices based on domains, this helps us to avoid data duplication and maintains data integrity if the tables are referenced.
- increases network call between microservices, increasing the network latency. Use event driven approach and send partial response to the users.

#### Choices of technology
- PostgreSQL - has lots of indexing option such as partial, cardinality and GIN, uses MVCC for transactions, materliazed views for complex time consuming queries. 
- Redis - we can all agree the time operation is database, storing prequeried results in redis avoids hitting the database. Redis supports structures such as hashmap, hashset, sorted set.
- Docker - captures the environment setup and builds a package with dependencies. 
- Jenkins - pulls the code from github, performs unit test, builds maven jar, creates docker image and to pushes it to dockerhub.
- AWS - to host microservices using container orchestration



    
