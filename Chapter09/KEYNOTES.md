# Chapter take away

1. An API gateway provides several benefits in a distributed architecture, including decoupling the internal services from the external API and offering a central, convenient place for handling cross-cutting concerns like security, monitoring, and resilience
2. Spring Cloud Gateway is based on the Spring reactive stack. It provides an API gateway implementation, and it integrates with the other Spring projects to add cross-cutting concerns to the application, including Spring Security, Spring Cloud Circuit Breaker, and Spring Session
3. Routes are the core of Spring Cloud Gateway. They are identified by a unique ID, a collection of predicates determining whether to follow the route, a URI for forwarding the request if the predicates allow, and a collection of filters that are applied before or after forwarding the request downstream
4. The Retry filter is for configuring retry attempts for specific routes
5. The RequestRateLimier filter, integrated with Spring Data Redis Reactive, limits the number of requests that can be accepted within a specific time window
6. The CircuitBreaker filter, based on Spring Cloud Circuit Breaker and Resilience4j, defined circuit breakers, time limiters, and fallbacks to specific routes
7. Cloud native applications should be stateless. Data services should be used for storing the state. For example, PostgreSQL is used for persistence storage, and Redis for cache and session management
8. A Kubernetes Ingress resource allows you to manage external access to applications running inside the Kubernetes cluster
9. The routing rules are enforced by an ingress controller, which is an application that also runs in the cluster