# Chapter take away

1. Observability is a property of cloud native applications that measures how well we can infer the internal state of an application from its outputs
2. Monitoring is about controlling known faulty states. Observability goes beyond that and permits us to ask questions about the unknown
3. Logs (or event logs) are discrete records of something that happened over time in a software application
4. Spring Boot supports logging through SLF4J, which provides a facade for the most common logging libraries
5. By default, logs are printed through the standard output as recommended by the 15-factor methodology
6. Using the Grafana observability stack, Fluent Bit collects logs produced by all applications and forwards them to Loki, which stores them and makes them searchable. Then you can use Grafana to navigate the logs
7. Applications should expose health endpoints to check their status
8. Spring Boot Actuator exposes an overall health endpoint showing the status of the application and all the components or services it might use. It also provides specialized endpoints to be used as liveness and readiness probes by Kubernetes
9. When the liveness probe is down, it means the application has entered an unrecoverable faulty state, so Kubernetes will try to restart it
10. When the readiness probe is down, the application is not ready to handle requests, so Kubernetes will stop any traffic directed to that instance
11. Metrics are numeric data about the application, measured at regular time intervals
12. Spring Boot Actuator leverages the Micrometer facade to instrument the Java code, generate metrics, and expose them through a dedicated endpoint
13. When the Prometheus client is on the classpath, Spring Boot can expose metrics in the Prometheus or OpenMetrics format
14. Using the Grafana observability stack, Prometheus aggregates and stores metrics from all applications. Then you can use Grafana to query metrics, design dashboards, and set alerts
15. Distributed tracing, a technique for tracking requests as they flow though a distributed system, lets us localize where errors occur in a distributed system and troubleshoot performance issues
16. Traces are characterized by a trace ID and are composed of multiple spans, representing steps in a transaction
17. The OpenTelemetry project includes APIs and instrumentation that generates traces and spans for the most common Java library
18. The OpenTelemetry Java Agent is a JAR artifact provided by the project that can be attached to any Java application. It injects the necessary bytecode dynamically to capture traces and spans from all those libraries and export them in different formats without having to change your Java source code explicitly
19. Using the Grafana observability stack, Tempo aggregates and stores metrics from all applications. Then you can use Grafana to query traces and correlate them with logs
20. Spring Boot Actuator provides management and monitoring endpoints to fulfill any reqirements you might have to make your application production-ready