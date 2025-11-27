# FocusX <img src="assets/focusx-logo.png" alt="FocusX Logo" width="50" height="50" align="left" style="padding-right: 10px;"/>
**Stay focused. Get things done.**

![App Showcase](assets/focusx.gif)

FocusX is a full-stack productivity web app designed to help users stay focused by gamifying tasks.  
It pairs focused work sessions with progress tracking and personalized rewards, making productivity feel more intentional and fun.

## Content
- [Tech Stack](#-tech-stack)
- [Features](#-features)
- [Architecture Overview](#%EF%B8%8F-architecture-overview)
- [Installation](#installation)


## 🛠 Tech Stack

### ♦️ Frontend
🔗 [GitHub - Frontend](https://github.com/angelinakumanova/focusx-frontend)

- **React** with **TypeScript** - building a scalable, type-safe user interface
- **Vite** - lightning-fast build tool for a smooth developer experience

### ♦️ Backend
🔗 [GitHub - Backend](https://github.com/angelinakumanova/focusx-backend)

- Java 21 + Spring Boot
- JWT Authentication
- Microservice Architecture
- Apache Kafka - for asynchronous communication
- MongoDB - NoSQL database
- Redis - caching frequently accessed data to reduce database load
- Docker - containerized services for consistent environments

## 🚀 Features

- **Customizable Pomodoro timer** ⏳ with adjustable work and break intervals to boost productivity.  
- **Goal tracking system** 🎯 to monitor progress on your personal or professional objectives.  
- **Reward system** 🎁 where users set and earn personalized rewards for achieving milestones.  
- **Secure authentication** 🔐 using JWT for safe access and data privacy.  
- **Microservices architecture** with Apache Kafka enabling real-time communication between services.  
- **Responsive and fast UI** built with React and TypeScript for smooth user experience.

## 🏗️ Architecture Overview

FocusX follows a **microservices architecture**, where each backend service is responsible for a specific domain, communicating asynchronously via **Apache Kafka** for scalability and reliability.

### 🔸 Backend
- Multiple Spring Boot microservices written in Java 21.
- MongoDB is used as the primary database for storing user data, goals, sessions and notifications.
- Kafka handles real-time messaging between services, enabling event-driven updates.
- Redis caches frequently accessed data as to reduce DB load.

### 🔸 Frontend
- A React + TypeScript single-page application built with Vite.
- Connects to backend microservices through REST APIs.
- Uses JWT tokens for secure authentication and authorization.

### 🔸 Deployment
- All services are containerized with Docker for consistent environments.

## Installation

### Step 1: Clone the Repository
```
git clone https://github.com/angelinakumanova/focusx.git
cd focusx-docker
```

### Step 2: Configure Environment
```
# Copy the example environment file and edit the config settings
cp .env.example .env
```

### Step 3: Start Application
```
# Start all services in detached mode
docker-compose up -d

# View logs (optional)
docker-compose logs -f
```

### Step 4: Verify services
```
# Check service status
docker-compose ps
```

Wait until all services show `healthy` status (usually 30-60 seconds).

### 🌐 Accessing the Application
Once all services are healthy:
<br>
**Frontend UI: http://localhost:5173**

**API Documentation (Swagger)**

User Service: http://localhost:8080/swagger-ui.html
<br>
Goal Service: http://localhost:8081/swagger-ui.html
<br>
Session Service: http://localhost:8082/swagger-ui.html
<br>
Notification Service: http://localhost:8083/swagger-ui.html

## 🙏 Thank You!

Thank you for checking out FocusX!  
I hope this project inspires you to boost your productivity and achieve your goals.  

If you have any feedback or questions, feel free to reach out!


**Happy focusing! 🚀**
