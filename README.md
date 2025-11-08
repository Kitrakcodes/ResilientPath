# ResilientPath: An Event-Driven Order Processing Pipeline

> A fault-tolerant, event-driven e-commerce order processing system built with Node.js, Kafka, and MongoDB, demonstrating a modern microservices architecture and the Saga pattern for compensation.

This project is a complete Minimum Viable Product (MVP) that simulates a real-world, asynchronous order pipeline. It is designed to be resilient to failures, scalable under load, and observable through a real-time dashboard.

## ✨ Key Features

*   **Event-Driven Architecture:** Services are fully decoupled and communicate asynchronously using Kafka, eliminating single points of failure.
*   **Microservices:** Each business domain (Orders, Inventory, Payments, Shipping) is handled by a small, independent Node.js service.
*   **Saga Pattern for Fault Tolerance:** The system gracefully handles business failures (e.g., a declined payment) by triggering compensating events to ensure data consistency across the entire pipeline.
*   **State Persistence:** The complete state and history of every order is durably stored in a MongoDB database.
*   **Real-Time Observability:** A React-based dashboard provides a live window into the status of any order, visualizing its journey through the pipeline.
*   **Containerized Infrastructure:** The entire infrastructure stack (Kafka, Zookeeper, MongoDB) is managed via a single `docker-compose.yml` file for easy, one-command setup.
