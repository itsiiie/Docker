# 🚀 Docker Projects Repository

![Docker Projects Banner](https://images.unsplash.com/photo-1605745341112-85968b19335b?w=1200&h=300&fit=crop&q=80)

> **A curated collection of containerized applications showcasing modern development practices, CI/CD automation, and Docker best practices.**

[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)
![Multi-Platform](https://img.shields.io/badge/Multi--Platform-amd64%20%7C%20arm64-orange?style=for-the-badge)

---

## 📋 Overview

![Container Architecture](https://images.unsplash.com/photo-1493946740644-2d8a1f1a6aff?w=800&h=400&fit=crop&q=80)

This repository serves as a **comprehensive portfolio of containerized applications**, each demonstrating different technologies, frameworks, and architectural patterns. Every project is fully Dockerized with production-ready configurations and automated CI/CD pipelines.

### ✨ What's Inside

| 📦 Independent Projects | 🐳 Docker Best Practices |    ⚙️ Dedicated CI/CD    |  🌐 Multi-Architecture  |
| :---------------------: | :----------------------: | :----------------------: | :---------------------: |
|  Isolated directories   |    Multi-stage builds    | GitHub Actions workflows |      amd64 & arm64      |
|    Complete autonomy    |     Optimized layers     |  Independent pipelines   | Cross-platform support  |
|     Self-contained      |     Security-focused     |   Automated deployment   | Universal compatibility |

---

## 🗂️ Repository Structure

```
📦 Docker-Projects-Repository
 ┣ 📂 Flask-Hello-World          # 🐍 Python Flask web application
 ┃ ┣ 📜 app.py
 ┃ ┣ 📜 requirements.txt
 ┃ ┣ 🐳 Dockerfile
 ┃ ┗ 📖 README.md
 ┃
 ┣ 📂 [Future-Project-1]         # 🚧 Coming Soon
 ┣ 📂 [Future-Project-2]         # 🚧 Coming Soon
 ┃
 ┣ 📂 .github
 ┃ ┗ 📂 workflows
 ┃   ┣ ⚙️ flask-hello-world.yml      # CI/CD for Flask project
 ┃   ┣ ⚙️ [project-1].yml            # CI/CD for future project 1
 ┃   ┣ ⚙️ [project-2].yml            # CI/CD for future project 2
 ┃   ┗ ⚙️ ...                        # Each project gets its own workflow
 ┃
 ┗ 📖 README.md                   # 👈 You are here!
```

**🎯 Each project directory contains:**

- 💻 **Application Code** - Source files and dependencies
- 🐳 **Dockerfile** - Multi-stage build configuration
- 📖 **Documentation** - Project-specific README
- ⚙️ **Dedicated CI/CD Workflow** - Independent GitHub Actions pipeline
- 🧪 **Tests** - Unit and integration tests (where applicable)

---

## 🛠️ Getting Started

![Getting Started](https://images.unsplash.com/photo-1618401479427-c8ef9465fbe1?w=800&h=300&fit=crop&q=80)

### 📋 Prerequisites

Before running any project, ensure you have:

|                    🐳 Docker                    |                  🔧 Git                   |                  🎼 Docker Compose                   |
| :---------------------------------------------: | :---------------------------------------: | :--------------------------------------------------: |
|                 v20.10 or later                 |              Latest version               |                       Optional                       |
| [Download](https://docs.docker.com/get-docker/) | [Download](https://git-scm.com/downloads) | [Download](https://docs.docker.com/compose/install/) |

### 🚀 Quick Start Guide

Follow these steps to run **any project** in this repository:

#### **1️⃣ Clone the Repository**

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

#### **2️⃣ Navigate to a Project**

```bash
cd PROJECT_NAME
```

#### **3️⃣ Build the Docker Image**

```bash
docker build -t project-name:local .
```

#### **4️⃣ Run the Container**

```bash
docker run -p HOST_PORT:CONTAINER_PORT project-name:local
```

#### **5️⃣ Access the Application**

Open your browser and navigate to:

```
http://localhost:HOST_PORT
```

---

## 📦 Projects

### 1️⃣ Flask-Hello-World

![Flask Application](https://images.unsplash.com/photo-1629654297299-c8506221ca97?w=1000&h=400&fit=crop&q=80)

![Flask](https://img.shields.io/badge/Flask-3.1.2-000000?style=flat&logo=flask&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat&logo=python&logoColor=white)
![Docker Hub](https://img.shields.io/badge/Docker_Hub-itsiiie%2Fflask--app-2496ED?style=flat&logo=docker&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-success?style=flat)

A lightweight Python Flask web application demonstrating containerization fundamentals and automated multi-architecture builds.

#### 🎯 Features

| Feature                           | Description                                       |
| --------------------------------- | ------------------------------------------------- |
| ✅ **Minimal Flask App**          | Simple "Hello from Docker!" endpoint              |
| ✅ **Multi-Stage Build**          | Optimized Dockerfile with reduced image size      |
| ✅ **Multi-Architecture Support** | Builds for `linux/amd64` and `linux/arm64`        |
| ✅ **Automated CI/CD**            | GitHub Actions workflow for continuous deployment |
| ✅ **Docker Hub Integration**     | Automatic image publishing                        |

#### 📁 Project Components

| Component               | Description                               |
| ----------------------- | ----------------------------------------- |
| 📜 **app.py**           | Flask application running on 0.0.0.0:5000 |
| 📋 **requirements.txt** | Dependencies: Flask==3.1.2, pytest        |
| 🐳 **Dockerfile**       | Multi-stage build with Python 3.11-slim   |

**🔑 Dockerfile Highlights:**

- 🐍 Base Image: `python:3.11-slim`
- 🏗️ Multi-stage build for optimized image size
- 🔓 Exposes port `5000`
- 👤 Non-root user for enhanced security
- 📦 Only essential files in final image

#### 🔧 Running Locally

```bash
# Navigate to project directory
cd Flask-Hello-World

# Build the image
docker build -t flask-hello-world:local .

# Run the container
docker run -p 5000:5000 flask-hello-world:local

# Access the application
curl http://localhost:5000
# Output: Hello from Docker!
```

#### 🔄 CI/CD Pipeline

![CI/CD Pipeline](https://images.unsplash.com/photo-1667372393119-3d4c48d07fc9?w=800&h=250&fit=crop&q=80)

Each project in this repository has its **own dedicated GitHub Actions workflow** for complete independence and isolation.

**⚙️ Workflow Configuration** (`.github/workflows/flask-hello-world.yml`)

| Stage               | Description                                                 |
| ------------------- | ----------------------------------------------------------- |
| 🎯 **Trigger**      | Automatic on push/PR to `Flask-Hello-World/` directory only |
| 🔨 **Build**        | Multi-platform Docker images using Buildx                   |
| 🔐 **Authenticate** | Secure login to Docker Hub                                  |
| 🏗️ **Compile**      | Builds for `linux/amd64` and `linux/arm64`                  |
| 🏷️ **Tag**          | Creates `latest` and commit SHA tags                        |
| 🚀 **Deploy**       | Pushes images to Docker Hub                                 |

**🏷️ Tagging Strategy:**

- `itsiiie/flask-app:latest` → Latest stable version
- `itsiiie/flask-app:${{ github.sha }}` → Commit-specific tag

**✨ Benefits of Independent Workflows:**

| Benefit                  | Impact                                                 |
| ------------------------ | ------------------------------------------------------ |
| ✅ Individual Deployment | Deploy projects independently without affecting others |
| ✅ Custom Strategies     | Different deployment schedules per project             |
| ✅ Faster Execution      | Only builds what changed                               |
| ✅ Easy Maintenance      | Simpler debugging and troubleshooting                  |

**🐳 Pull from Docker Hub:**

```bash
docker pull itsiiie/flask-app:latest
docker run -p 5000:5000 itsiiie/flask-app:latest
```

#### 📊 Image Details

| Metric          | Value               |
| --------------- | ------------------- |
| 🐍 Base Image   | `python:3.11-slim`  |
| 🏗️ Architecture | `amd64`, `arm64`    |
| 🔓 Exposed Port | `5000`              |
| 🐳 Registry     | Docker Hub          |
| 📦 Image Name   | `itsiiie/flask-app` |

---

## 🚧 More Projects Coming Soon!

![Coming Soon](https://images.unsplash.com/photo-1519389950473-47ba0277781c?w=800&h=300&fit=crop&q=80)

**This repository is actively growing. Future projects will include:**

### 🟢 Node.js Applications

- Express REST APIs
- NestJS backend services
- Real-time microservices

### 🔵 Go Services

- High-performance APIs
- CLI tools and utilities
- gRPC services

### 🟠 Database Projects

- PostgreSQL configurations
- MongoDB setups
- Redis caching solutions

### 🟣 Full-Stack Applications

- React + Backend integrations
- Vue.js applications
- Modern SPA architectures

### 🔴 Microservices Architecture

- Service mesh examples
- Container orchestration
- Distributed systems patterns

### 🟡 DevOps & Infrastructure

- Monitoring solutions
- Logging stacks
- Infrastructure as Code

**⭐ Star this repository to get notified about new projects!**

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

### How to Contribute:

**1️⃣ Fork the Repository**

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
```

**2️⃣ Create a Feature Branch**

```bash
git checkout -b feature/AmazingFeature
```

**3️⃣ Commit Your Changes**

```bash
git commit -m 'Add some AmazingFeature'
```

**4️⃣ Push to the Branch**

```bash
git push origin feature/AmazingFeature
```

**5️⃣ Open a Pull Request**

- Go to the repository on GitHub
- Click "New Pull Request"
- Describe your changes

---

## 📝 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

**Maintainer:** Shashank

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/itsiiie)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/itsiiie/)
[![Docker Hub](https://img.shields.io/badge/Docker_Hub-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://hub.docker.com/u/itsiiie)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mdpkdy@gmail.com)

---

![Footer Wave](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=150&section=footer&text=Made%20with%20❤️%20and%20Docker&fontSize=30&fontAlignY=70&animation=twinkling)

**⭐ If you find this repository helpful, please consider giving it a star!**
