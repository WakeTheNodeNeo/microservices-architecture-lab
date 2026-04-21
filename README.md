<img width="1536" height="1024" alt="962d2340-0c1d-4c14-9cbc-e0a22a093177" src="https://github.com/user-attachments/assets/54f52a93-03cb-440e-9e03-cecde638a28c" />


# Time App — Dockerized Microservices Lab

Minimal full-stack application deployed using Docker Compose.
This project demonstrates how multiple services interact within a containerized environment.

---

## Architecture

The application consists of 4 services:

* **Frontend (Vue.js)** — user interface
* **Backend (Node.js)** — API layer
* **MySQL** — database
* **Adminer** — database management UI

All services communicate through a Docker internal network.

---

## 🔗 How it works

```
Client → Frontend → API → Backend → MySQL
                               ↓
                           Adminer
```

---

## ⚙️ Ports Mapping

| Service  | Container Port | Host Port |
| -------- | -------------- | --------- |
| Frontend | 3000           | 3333      |
| Backend  | 5000           | 5555      |
| MySQL    | 3306           | internal  |
| Adminer  | 8080           | 8888      |

---

## Docker Setup

Run the application:

```bash
docker compose up --build
```

Stop containers:

```bash
docker compose down
```

---

## Features

* Save current time to database
* Retrieve stored timestamps
* Delete entries
* Real-time UI updates
* Notifications (success / delete)

---

## What this project demonstrates

* Multi-container architecture
* Docker networking (service-to-service communication)
* Port mapping and exposure
* Backend ↔ Database integration
* Debugging container issues (DNS, paths, connectivity)
* Basic full-stack interaction flow
  The application allows you to:
* Click **"Save Time"** → store timestamp in MySQL
* View saved entries
* Delete records via API

---


---

##  Notes

This project was built as part of a Docker learning process, focusing on infrastructure and service interaction rather than frontend or backend complexity.

---

##  About me

Sagadat Kuandykov
IT Infrastructure / DevOps (in progress)

---
