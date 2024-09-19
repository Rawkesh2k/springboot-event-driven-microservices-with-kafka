# Event-Driven Microservices Architecture with Spring Boot and Apache Kafka

This project demonstrates the implementation of an **event-driven microservices architecture** using **Spring Boot** and **Apache Kafka** for asynchronous communication between multiple microservices. 

## Overview

In this project, we will develop three microservices:
1. **Order Service** – Handles order placement and creates order events.
2. **Stock Service** – Manages stock availability based on the order events.
3. **Email Service** – Sends notification emails upon order creation.

You can easily extend this architecture by adding more services such as SMS notifications, package tracking, or payment processing, but we will keep it simple for this example.

### Architecture

The **Order Service** will receive orders from customers, generate an `OrderEvent`, and publish it to a Kafka topic. The **Stock Service** and **Email Service**, which act as consumers, will listen to the Kafka topic and process the `OrderEvent` asynchronously. This design allows seamless and scalable communication between microservices without direct coupling.

In this project, we will:
- Set up a **Kafka Broker** to act as the messaging system for our microservices.
- Create a **single Kafka topic** and configure **multiple consumers** (Stock Service and Email Service) to listen and react to order events.
  
### Key Features:
- **Event-Driven Architecture**: Microservices communicate asynchronously via events, improving scalability and decoupling services.
- **Multiple Consumers**: Demonstrates how to create multiple Kafka consumers subscribed to the same topic.
- **Apache Kafka**: Leverages Kafka's messaging capabilities for reliable and scalable data streaming.
- **Spring Boot**: Provides a robust and lightweight framework for building the microservices.

### Prerequisites:
- **Java 11** or later
- **Apache Kafka** (locally or via Docker)
- **Spring Boot 2.5+**

### Getting Started

To set up and run the project, follow these steps:

1. Clone the repository.
2. Set up and configure Apache Kafka (locally or using Docker).
3. Build and run each microservice using Spring Boot.
4. Place an order through the **Order Service** and observe the event being processed by both the **Stock Service** and **Email Service**.

### Extending the Architecture

While this project includes three microservices, the architecture can be easily extended by adding new services like:
- **SMS Service**: To send SMS notifications for order updates.
- **Package Service**: To handle shipping and delivery.
- **Payment Service**: To manage payment processing.

### Conclusion

This project is a simple yet powerful demonstration of how **event-driven microservices** can communicate asynchronously using **Apache Kafka**. By decoupling services and using Kafka as a messaging system, this architecture promotes scalability, flexibility, and maintainability in a microservices ecosystem.
