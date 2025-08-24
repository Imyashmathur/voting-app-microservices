# 🗳️ Microservices Voting App  
**A Dockerized Voting App with Redis, PostgreSQL, and Microservices**

![Docker](https://img.shields.io/badge/Docker-Compose-blue?logo=docker)
![Python](https://img.shields.io/badge/Python-3.9-yellow?logo=python)
![Node.js](https://img.shields.io/badge/Node.js-14-green?logo=node.js)
![PostgreSQL](https://img.shields.io/badge/Postgres-13-blue?logo=postgresql)
![Redis](https://img.shields.io/badge/Redis-Cache-red?logo=redis)

---

## 📌 About the Project
This project is a **microservices-based voting system** that demonstrates containerized services orchestrated using **Docker Compose**.  
It allows users to **vote between two options** and displays **real-time results** in a separate UI.

---

## 🛠️ Tech Stack
- **Frontend**:  
  - **Vote App** → Python (Flask)  
  - **Result App** → Node.js + Express  

- **Backend Services**:  
  - **Worker** → .NET  
  - **Redis** → Queue for votes  
  - **PostgreSQL** → Stores vote counts  

---

## 📂 Architecture

```mermaid
graph LR
    subgraph Frontend
        A[Vote App (Flask)]
        E[Result App (Node.js)]
    end

    subgraph Backend
        B[Redis Queue]
        C[Worker Service]
        D[PostgreSQL DB]
    end

    A -->|Send Vote| B
    B --> C
    C -->|Insert Data| D
    D --> E



## ✅ Features
✔️ Microservices-based  
✔️ Real-time results  
✔️ Dockerized for portability  
✔️ Redis queue for scalability  
✔️ PostgreSQL for persistence  

---

## 🚀 Getting Started

### 1️⃣ Prerequisites
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/)

---

### 2️⃣ Clone Repository
```bash
git clone https://github.com/Imyashmathur/voting-app-microservices
cd voting-app-microservices
```

---

### 3️⃣ Start Services
```bash
docker compose up --build
```

---

### 4️⃣ Access the Apps
- **Vote App:** [http://localhost:8080](http://localhost:8080)  
- **Result App:** [http://localhost:8081](http://localhost:8081)  

---

## ⚙️ Project Structure
```
.
├── docker-compose.yml      # Orchestration file
├── vote/                   # Flask voting app
├── result/                 # Node.js results app
├── worker/                 # Background processor
└── README.md
```

---

## 🛠 Useful Commands
```bash
# Scale worker services
docker compose up --scale worker=3 -d

# Stop containers
docker compose down
```

---

## 📸 Screenshots
<img width="1850" height="907" alt="image" src="https://github.com/user-attachments/assets/192ff073-eb09-4111-a3c0-f1849c2aaf9b" />


<img width="1836" height="910" alt="Screenshot 2025-08-24 113257" src="https://github.com/user-attachments/assets/d87f57ef-3145-4621-8e52-b54b93828ab5" />

---

## 🎥 Demo Video
Coming Soon! (Add link after recording your walkthrough)

---

## 🏷 License
MIT License © 2025  

---

✨ **If you like this project, give it a ⭐ on [GitHub]((https://github.com/Imyashmathur/voting-app-microservices)!**
