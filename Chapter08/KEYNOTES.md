# Chapter take away

1. When you expect high traffic and concurrency with fewer computational resources, the reactive paradigm can improve the application's scalability, resilience, and cost-effectiveness at the expense of a steeper initial learning curve
2. Choose between a non-reactive and a reactive stack according to your requirements
3. Spring WebFlux is based on Project Reactor and is the core of the reactive stack in Spring. It supports asynchronous, non-blocking I/O
4. Reactive RESTful services can be implemented through @RestController classes or router functions
5. The Spring WebFlux slice can be tested through the @WebFluxTest annotation
6. Spring Data R2DBC provides support for reactive data persistence using the R2DBC driver. THe approach is the same as for any Spring Data project: database drivers, entities, and repositories
7. Database schemas can be managed with Flyway
8. The persitence slice of a reactive application can be tested using the @DataR2dbcTest annotation and Testcontainers
9. A system is resilient if it keeps providing its services in the face of faults without the user noticing it. Sometimes that's not possible, so the least you can do is ensure a graceful degradation of the services
10. WebClient is based on Project Reactor and works with Mono and Flux publishers
11. You can use the Reactor operators to configure timeouts, retries, fallbacks, and error handling to make the interaction more resilient to any failure in the service downstream or due to the network