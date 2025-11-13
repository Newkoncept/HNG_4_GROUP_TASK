# 📨 HNG 4 Distributed Notification System (Group Task)

This repository is part of the **HNG Stage 4 Backend Task**:  
**Distributed Notification System using Microservices and Message Queues (RabbitMQ).**

Each microservice handles a different part of the notification workflow — all working together asynchronously through a shared message queue.

---

## 🧩 Microservices Overview

| Service | Developer | Repository |
|----------|------------|-------------|
| 🧍‍♂️ **User Service** | [@El-kufahn](https://github.com/KhalifahMB) | 🔗 [github.com/KhalifahMB/User_Service](https://github.com/KhalifahMB/User_Service) |
| 🔔 **Push Service** | [@zeal_izu](https://github.com/zealizu) | 🔗 [github.com/zealizu/Distributed-Notification-System](https://github.com/zealizu/Distributed-Notification-System) |
| 🌐 **API Gateway** | [@Rishi](https://github.com/collab-rishi) | 🔗 [github.com/collab-rishi/Distributed-Notification-Gateway-Service](https://github.com/collab-rishi/Distributed-Notification-Gateway-Service) |
| ✉️ **Email Service** | [@PresidentialProgrammer](https://github.com/Newkoncept) | 🔗 [github.com/Newkoncept/HNG_4_Email_Service](https://github.com/Newkoncept/HNG_4_Email_Service) |

---

## 🚀 Project Goal

To build a **scalable, asynchronous distributed notification system** that:
- Sends **emails** and **push notifications** via separate microservices  
- Uses **RabbitMQ** for inter-service communication  
- Supports **retries**, **failure handling**, and **horizontal scaling**

---

## 🛠️ Core Technologies

- **Python / Django** – backend framework for Email Service  
- **Node.js / TypeScript** – for other microservices  
- **RabbitMQ** – message queue (asynchronous communication)  
- **PostgreSQL / Redis** – data storage and caching  
- **Docker** – containerization and deployment  

---

## 📡 Architecture Summary

```
           ┌─────────────────────┐
           │     API Gateway     │
           │  (Routes requests)  │
           └─────────┬───────────┘
                     │
          ┌───────────────────────┐
              RabbitMQ Exchange
          └───────────┬───────────┘
       ┌──────────────┼──────────────┐
       │                             │
┌────────────┐                 ┌────────────┐
│ Push Svc   │                 │ Email Svc  │
│ (push,    │                  │ (emails,   │
│ prefs)     │                 │ bounces)   │
└────────────┘                 └────────────┘
       
```

---

## 👥 Contributors
- **@El-kufahn** – User Service  
- **@zeal_izu** – Push Service  
- **@Rishi** – API Gateway  
- **@PresidentialProgrammer** – Email Service  
