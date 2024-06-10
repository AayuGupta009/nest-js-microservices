# NestJS Microservices Architecture

This repository showcases a scalable microservices architecture built with NestJS, Docker, Prisma, Joi, PostgreSQL, and MongoDB. It includes services for authentication, team management, and notifications, communicating via TCP and WebSockets for real-time updates, all managed by an API Gateway. Ideal for learning and reference in building modern, modular applications.

## Features

- **Microservices with NestJS**: Each service is developed using NestJS, promoting modularity and scalability.
- **Dockerized Environment**: The entire architecture is containerized using Docker for seamless deployment.
- **Database Integration**: Uses PostgreSQL for relational data and MongoDB for NoSQL data storage.
- **Prisma ORM**: Simplifies database interactions with a type-safe ORM.
- **Request Validation**: Implements Joi for robust request validation across services.
- **Real-Time Communication**: Utilizes WebSockets for real-time updates and inter-service communication.

## Services

### Auth Service

- Handles user registration and login.
- Communicates with the Team Service and Notification Service.
- JWT-based authentication.

### Team Service

- Manages team creation and updates.
- Propagates changes to the Notification Service for real-time updates.

### Notification Service

- Sends notifications to users.
- Listens for updates from the Team Service.

### API Gateway

- Acts as a central entry point for client requests.
- Routes requests to appropriate microservices.
- Handles cross-cutting concerns like authentication and rate limiting.

## Communication

- **TCP Communication**: Microservices communicate internally using TCP transport provided by `@nestjs/microservices`.
- **WebSockets**: Used for real-time updates to ensure users receive instant notifications regarding changes in their subscribed teams.

## Getting Started

### Clone the repository

```bash
git clone https://github.com/AayuGupta009/nest-js-microservices.git
