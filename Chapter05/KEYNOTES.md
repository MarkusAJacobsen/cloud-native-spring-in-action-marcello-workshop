# Chapter take away

1. The state is everything that should be preserved when shutting down a service and spinning up a new instance
2. Data services are the stateful components of a cloud native architecture, requiring storage technologies to persist the state 
3. Some issues to consider when choosing a data service are scalability, resilience, performance, and compliance with regulations and laws
4. You can use data services that are offered and managed by your cloud provider or manage your own, either relying on virtual machines or containers
5. Spring Data provides common abstractions and patterns for accessing data, making it straightforward to navigate the different modules dedicated to relational and non-relational databases
6. The main elements in Spring Data are database drivers, entities, and repositories
7. Spring Data JDBC is a framework that supports integrating Spring applications with relational databases relying on a JDBC driver
8. Entities represent domain objects and can be managed by Spring Data JDBC as immutable objects. They must have the field hosting the primary key annotated with @Id
9. Spring Data lets you capture audit metadata whenever an entity is created or updated. You can enable this feature with @EnableJdbcAuditing
10. Data repositories grant access to entities from the database. You need to define an interface, and then Spring Data will generate the implementation for you
11. In Spring Data JDBC, all mutating custom operations (create, update, delete) should run in transactions
12. Use the @Transactional annotation to run operations in a single unit of work
13. Environment parity is essential for the quality and reliability of your tests and development pipeline
14. You can test the integration between your application and backing services defined as containers by using the Testcontainers library. It lets you use lightweight, throwaway containers in your integration tests
15. Database schemas are critical for applications. In production, you should use a tool like Flyway, which provides version control for your database
16. Flyway should manage any database changes to ensure reproducibility, traceability, and reliability