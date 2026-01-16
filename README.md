# MERN Stack Application with Docker

This project demonstrates a clean, production‑aware Docker setup for a **MERN (MongoDB, Express, React, Node.js)** application. It is structured to clearly separate concerns, follow Docker best practices.
---

## 🚀 Tech Stack

* **Frontend:** React (Vite)
* **Backend:** Node.js, Express
* **Database:** MongoDB
* **Containerization:** Docker & Docker Compose

---

## 📁 Project Structure

```
mern_docker/
│── docker-compose.yml
│
├── frontend/
│   ├── Dockerfile
│   ├── package.json
│   └── src/
│
├── backend/
│   ├── Dockerfile
│   ├── package.json
│   ├── .env
│   └── src/
│
└── README.md
```

Each service (frontend, backend, database) runs in its own container, following the **one‑process‑per‑container** principle.

---

## 🧠 Architecture Overview

```
Browser
   ↓
Frontend (React / Vite)
   ↓ HTTP API
Backend (Node / Express)
   ↓
MongoDB
```

* The **frontend** communicates with the backend via HTTP.
* The **backend** handles business logic and database access.
* **MongoDB** persists application data using a Docker volume.

---

## 🐳 Docker Setup

### Docker Compose Services

* **mongo** – MongoDB database with persistent volume
* **backend** – Express API server
* **frontend** – React (Vite) development server

Docker Compose is used to orchestrate all services with clear dependencies and isolated environments.

---

## ▶️ How to Run the Project

### Prerequisites

* Docker
* Docker Compose

### Start the application

```bash
cd mern_docker
docker compose up --build
```

### Access the app

* **Frontend:** [http://localhost:5173](http://localhost:5173)
* **Backend API:** [http://localhost:5000](http://localhost:5000)
* **MongoDB:** exposed internally to backend

---

## 🔐 Environment Variables

The backend uses an `.env` file located in `backend/.env`.

Example:

```
PORT=5000
MONGO_URI=mongodb://mongo:27017/mydb
```

Environment variables are injected using Docker Compose, not hardcoded.

---

## ✅ Best Practices Followed

* Clean Docker build contexts
* No unnecessary bind mounts
* Stateless containers
* Persistent database storage via volumes
* Clear service dependency definition
* Readable and maintainable configuration

---

## 📌 Why This Project Matters

This repository is designed to show:

* Practical understanding of Docker & Docker Compose
* Real‑world MERN stack containerization
* Clean infrastructure code suitable for production environments
* Ability to structure and document a project professionally

---

## 📄 Future Improvements

* Multi‑stage production build for frontend (Nginx)
* Health checks for services
* CI/CD pipeline integration
* Kubernetes deployment

---

## 👤 Author

**Ishola Oluwatobi**
Aspiring DevOps / Cloud Engineer
Focused on Docker, Linux, and cloud‑native tooling

---

If you are reviewing this project and have feedback or suggestions, they are welcome.
