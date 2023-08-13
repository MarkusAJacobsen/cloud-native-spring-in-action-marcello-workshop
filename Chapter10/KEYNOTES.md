# Chapter take away

1. Event-driven architectures are distributed systems that interact with each other by producing and consuming events
2. An event is something relevant that happened in a system
3. In the pub/sub model, producers publish events, which are sent to all subscribers to be consumed
4. Event processing platforms like RabbitMQ and Kafka is responsible for collecting events from the producers, routing, and distributing them to the interested consumers
5. In the AMQP protocol, producers send messages to an exchange in a broker that forwards them to queues according to specific routing algorithms 
6. In the AMQP protocol, messages are data structures composed of key/value attributes and a binary payload
7. RabbitMQ is a message broker based on the AMQP protocol that you can use to implement event-driven architectures based on the pub/sub model
8. RabbitMQ provides high availability, resilience, and data replication
9. Spring Cloud Function enables you to implement your business logic using the standard Java Function, Supplier, and Consumer interfaces
10. Spring Cloud Function wraps you function and provides several exciting features like transparent type conversion and function composition
11. Functions can be exposed as REST endpoints, packaged, and deployed in a FaaS platform as serverless applications (Knative, AWS Lambda, Azure Function, Google Cloud Functions), or they can be bound to message channels
12. Spring Cloud Stream, built on top of Spring Cloud Functions, provides you with all the necessary plumbing to integrate your functions with external message systems like RabbitMq or Kafka
13. Once you implement your functions, you don't have to make any changes to your code. You only need to add a dependency on Spring Cloud Stream and configure it to adapt to your needs
14. In Spring Cloud Stream, destination binders provide integration with external message systems
15. In Spring Cloud Stream, destination bindings (input and output) bridge the producers and consumers in your applications with exchanges and queues on a message broker
16. Functions and consumers are activated automatically when new messages arrive
17. Suppliers need to be explicitly activated, such as by explicitly sending a message to a destination binding