# Docker Compose YAML Practice

This directory contains Docker and Docker Compose YAML files used for **practice and learning purposes**.
The goal is to understand how to define, run, and manage **multi-container applications** using Docker Compose.

---

## 📁 Directory Contents

- `docker-compose.yml`  
  Defines a multi-container application with:
  - MySQL database service
  - Frontend application service

- `Dockerfile`  
  Used to build the frontend application image.

- `README.md`  
  Documentation for Docker-related practice.

---

## 🧱 Services Overview

### 1️⃣ Database Service (MySQL)
- Uses the official **MySQL 8.0** image
- Environment variables are used to configure:
  - Root password
  - Database name
  - Database user
- Data persistence is handled using **Docker volumes**

### 2️⃣ Frontend Service
- Built from a local `Dockerfile`
- Exposes the application on port **3000**
- Depends on the database service to start first

---

## ▶️ How to Run the Project

Make sure Docker and Docker Compose are installed.

From the `docker/` directory:

```bash
docker-compose up -d


---

##  How to stop the project 

To stop and remove the running containers:

docker-compose down


To stop containers and also remove volumes (this will delete database data):

docker-compose down -v


To stop containers without removing them:

docker-compose stop


