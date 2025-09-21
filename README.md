# ☁️ Novacron – MinIO Based Cloud Storage App

Novacron is a simple yet powerful **cloud storage system** built with **Node.js, React, MinIO, and PostgreSQL**, containerized with **Docker Compose**.  
It lets you securely upload, manage, and download files via a modern web UI and a REST API.

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18-green?logo=node.js" />
  <img src="https://img.shields.io/badge/React-18-blue?logo=react" />
  <img src="https://img.shields.io/badge/MinIO-S3-red?logo=minio" />
  <img src="https://img.shields.io/badge/Postgres-Database-blue?logo=postgresql" />
  <img src="https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker" />
</p>

---

## 📖 Overview

The app consists of three main parts:

1. **Backend API (Node.js)**  
   Provides REST endpoints for file operations and metadata.  

2. **Frontend App (React)**  
   A simple, user-friendly UI to interact with your storage.  

3. **Storage Layer (MinIO + PostgreSQL)**  
   - **MinIO**: S3-compatible object storage to hold the files.  
   - **PostgreSQL**: Stores file metadata and user data.  

Everything is orchestrated using **Docker Compose**, so you can bring the entire stack up with a single command.

---

## 🚀 Quick Start Guide (Windows, macOS, Linux)

### Step 1: Install the Tools

- [Docker & Docker Compose](https://docs.docker.com/get-docker/)  
- Node.js (for local development)  
- Bash (to run helper scripts)  

Confirm installation:

```bash
docker compose version
node -v
```

### Step 2: Clone and Setup
```bash
git clone <your-repo-url>
cd CCStorage
```
Copy the environment file and set your configs:
```bash
cp .env.example .env
```
### Step 3:Run The Aplication
You can use the start script:
```bash
bash start.sh
```
Or run manually with Docker:
```bash
docker compose up --build
```
- Backend: http://localhost:4000
- Frontend: http://localhost:3000
- MinIO Console: http://localhost:9001