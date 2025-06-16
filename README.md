# 💬 Chat-Lite – Real-Time Chat Application (Microservices Architecture)
![Docker](https://img.shields.io/badge/Dockerized-Yes-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Microservices](https://img.shields.io/badge/Architecture-Microservices-blueviolet?style=for-the-badge)
![Backend](https://img.shields.io/badge/Backend-ASP.NET%20Core%208.0-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Frontend](https://img.shields.io/badge/Frontend-Angular%2019.2.0-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![Database](https://img.shields.io/badge/Database-PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)
![Message Broker](https://img.shields.io/badge/Messaging-RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**Chat-Lite** is a full-stack real-time chat application built with modern technologies using a microservices architecture. It demonstrates production-grade patterns like clean architecture, domain-driven design, message-based communication, and containerized deployment — all bundled into one cohesive project.

_currently supports P2P messaging only_

---

## 🧩 Microservices & Tech Stack

| Service         | Technology                              | Responsibility                                                |
|-----------------|------------------------------------------|----------------------------------------------------------------|
| **Frontend**     | Angular 19.2.0                           | SPA that handles login, chat UI, and SignalR integration        |
| **Auth Server**  | ASP.NET Core 8.0, JWT, PostgreSQL       | Handles user registration, login, JWT issuance, and user events |
| **Chat Server**  | ASP.NET Core 8.0, SignalR, PostgreSQL   | Real-time messaging logic; manages conversations and messages   |
| **API Gateway**  | ASP.NET Core 8.0                        | Routes client requests to services; handles CORS and auth       |
| **RabbitMQ**     | RabbitMQ                                | Message broker for event propagation (user creation)            |
| **Database**     | PostgreSQL                              | Data persistence for users and messages                         |
| **Infra**        | Docker, Docker Compose                  | Microservices container orchestration                           |



### 🕸️ **Ports Used**

| Service         | Port  |
|------------------|--------|
| Frontend (Angular) | `4200` |
| Auth Server        | `7001` |
| Chat Server        | `7002` |
| API Gateway        | `7000` |
| RabbitMQ Dashboard | `15672` |

---

## 🚀 Features

- ✅ Real-time 1:1 chat using SignalR
- ✅ JWT Authentication with PostgreSQL
- ✅ RabbitMQ-based user creation event propagation
- ✅ Clean Architecture, DDD, Repository + Unit of Work patterns
- ✅ PostgreSQL for persistent chat and user data
- ✅ Docker-based microservices orchestration
- ✅ Angular frontend with strict typing & CSS Grid layout
- 🛡️ API Gateway centralizing service exposure

---

## 🧪 Getting Started (with Docker)

### 📦 Prerequisites
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

### 🚀 Run All Services

```bash
git clone [https://github.com/AnuvindM02/chat-app-microservices.git](https://github.com/AnuvindM02/chat-app-microservices.git)
cd chat-app-microservices

# Clone all submodules (client, chat-server, etc.)
git submodule update --init --recursive

# Start everything
docker-compose up --build
```
### 🌐 Access Points

| Service             | URL                                                                 |
|---------------------|----------------------------------------------------------------------|
| Frontend            | [http://localhost:4200](http://localhost:4200)                      |
| API Gateway         | [http://localhost:7000](http://localhost:7000)                      |
| RabbitMQ Dashboard  | [http://localhost:15672](http://localhost:15672) <br>*(username: user/password: password)* |

---

### 🔐 RabbitMQ Credentials

Default credentials (can be changed in `docker-compose.yml`):

```yaml
RABBITMQ_DEFAULT_USER: user
RABBITMQ_DEFAULT_PASS: password
```
---
## 📝 License

This project is licensed under the MIT License.

---
## 🙋‍♂️ Contact

Built by Anuvind M
If you find this project helpful, feel free to ⭐ star the repo and connect on [LinkedIn](https://www.linkedin.com/in/anuvindm/)


