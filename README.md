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
```bash

## Install dependencies

```bash
cd auth-service
npm install
cd ../team-service
npm install
cd ../notification-service
npm install
cd ../api-gateway
npm install
```bash

## Run the services

```bash
docker-compose up --build
```bash

## Access the API Gateway
The API Gateway will be available at http://localhost:3000.

## Configuration
- **Environment Variables**: Each service uses environment variables for configuration. Refer to the .env.example file in each service's directory for required variables.
- **Prisma ORM**: Configure your database connection in the prisma/schema.prisma file for each service.

## Documentation
- **API Documentation**: Comprehensive API documentation is available via Postman collections.
- **WebSocket Events**: Events are documented to demonstrate real-time communication between services.

## Contributing
We welcome contributions! Please read our contributing guidelines for details on how to contribute to this project.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

