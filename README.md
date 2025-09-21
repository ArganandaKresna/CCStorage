# ☁️ CCStorage – Cloud Storage Project

> A simple yet powerful **cloud storage system** built with **Node.js, React, MinIO, and PostgreSQL**, containerized with **Docker Compose**.  

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-18-green?logo=node.js" />
  <img src="https://img.shields.io/badge/React-18-blue?logo=react" />
  <img src="https://img.shields.io/badge/MinIO-S3-red?logo=minio" />
  <img src="https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker" />
</p>

---

## ✨ Features
- 📂 Upload & download files  
- 🔒 Secure object storage using **MinIO (S3 compatible)**    
- 🖥️ Interactive **React frontend**  
- ⚡ REST API with **Node.js backend**  
- 🐳 Fully containerized with **Docker Compose**

---

## 🚀 Quick Start

Clone the repository and run:

```bash
git clone <your-repo-url>
cd CCStorage
bash start.sh
```

---

## 📂 Folder Structure
```bash
CCStorage/
├── backend/          # Node.js REST API
│   ├── server.js
│   └── ...
├── frontend/         # React web app
│   ├── src/
│   └── ...
├── docker-compose.yml
├── start.sh          # Auto-start script
└── README.md

```

---
## 🛠️ Requirements

- Docker 
- Node.js (for development outside Docker)
- Bash (to run ```start.sh```)

---

## 🌐 Endpoints

Backend (Node.js):

- POST /upload → Upload file

- GET /download/:id → Download file

- GET /files → List uploaded files

Frontend (React):

- http://localhost:3000

MinIO Console:

- http://localhost:9001

---
## 🖼️ Demo Preview

<p align="center"> <img src="https://dummyimage.com/800x400/ddd/000&text=Cloud+Storage+Demo" width="600"/> </p>

---
## 🤝 Contribution

Pull requests are welcome! Please fork the repo and submit PRs.