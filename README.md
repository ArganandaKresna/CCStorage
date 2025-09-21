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
### WSL and Docker
1. Install WSL2
- Open PowerShell as Administrator and run:
  ```powershell
  wsl --install
  ```
- Restart your computer if prompted.
- By default, Ubuntu will be installed. You can check with:
   ```powershell
   wsl -l -v
   ```
- Make sure it’s running with Version 2. If not, convert:
   ```powershell
   wsl --set-version Ubuntu 2
   ```

    **Docker Desktop**: [Download Docker here](https://www.docker.com/products/docker-desktop/). 
- During installation, enable:

   ✅ Use WSL 2 based engine

   ✅ Integrate with Ubuntu (or your chosen distro)
- After installing, **start Docker Desktop** and let it run in the background.

    **Docker Compose**
- Comes bundled with Docker Desktop (Windows & macOS).
- Inside WSL (Linux terminal), confirm it works:
```bash
docker compose version
```
### Node.js Installation

1. **Install Node.js using Node Version Manager (NVM)**
    NVM allows you to easily install and switch between Node.js versions.

- Install `curl` if not already available:
     ```bash
     sudo apt update && sudo apt install curl -y
     ```

- Download and install NVM:
     ```bash
     curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
     ```

- Reload your shell:
     ```bash
     source ~/.bashrc
     ```

- Verify NVM installation:
     ```bash
     nvm --version
     ```

2. **Install Node.js (Recommended LTS version)**
- To install the latest **LTS (Long Term Support)** version:
     ```bash
     nvm install --lts
     ```

- Set the installed version as default:
     ```bash
     nvm use --lts
     nvm alias default lts/*
     ```

3. **Verify Installation**
   Confirm Node.js and npm versions:
    ```bash
    node -v
    npm -v
    ```

   You should see something like:
    ```
    v18.x.x
    9.x.x
    ```

    ✅ Now your system has Node.js and npm properly installed inside WSL2, ready to run the **backend** of this project.

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
---
## 🌐 API Endpoints

Backend (Node.js)

- ```POST /upload``` → Upload a file

- ```GET /download/:id``` → Download a file by ID

- ```GET /files``` → List all files

Frontend (React)

- ```http://localhost:3000```

MinIO Console

- ```http://localhost:9001```
---
## 🧑‍💻 Developer Guide
Development Workflow

Start only the backend:
```bash
cd backend && npm install && npm start
```

Start the frontend:
```bash
cd frontend && npm install && npm start
```

Run everything together with Docker Compose in project root:
```
docker compose up --build -d
```

Stopping the App
```
docker compose down
```