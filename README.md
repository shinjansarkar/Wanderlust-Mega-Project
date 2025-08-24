# 🐳 Dockerized Wanderlust Blog Application

I have Dockerized the **Wanderlust MERN Stack Blog Application** to make it lightweight, portable, and production-ready.  

---

## 🚀 Key Highlights
- ✅ **Multi-stage Dockerfiles** → optimized image size and faster builds.  
- ✅ **Nginx Reverse Proxy** → efficient frontend serving and request routing.  
- ✅ **Docker Compose Setup** → easy orchestration of frontend, backend, and database services.  
- ✅ **Docker Volumes** → persistent data storage across container restarts.  

---

## 🖼️ Architecture Overview


*(Frontend → Nginx Proxy → Backend API → MongoDB with persistent volume)*

---

## ⚡ Quick Start with Docker Compose
```bash
# Clone the repository
git clone https://github.com/shinjansarkar/Wanderlust-Mega-Project.git
cd Wanderlust-Mega-Project

# Build and run containers
docker-compose up --build
