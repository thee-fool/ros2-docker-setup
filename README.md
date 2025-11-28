# ROS2 Jazzy on Docker 

This guide will help you run a complete **ROS 2 Jazzy** environment using Docker with a web-based VNC interface — no native installation required. Everything runs inside a secure container environment.

---

## 🐳 1️⃣ What is Docker?

Docker is a **containerization** platform that allows applications to run in isolated environments called **containers**.

### 🔹 Key Concepts

| Concept | Description |
|--------|-------------|
| **Docker Image** | A blueprint or template containing everything required to run (OS, dependencies, ROS 2, etc.) |
| **Docker Container** | A *running instance* of an image — lightweight, fast, isolated |
| **Port Mapping** | Access apps inside the container from your host machine |

Think of an image as a *recipe* 🧾, and a container as the *prepared dish* 🍽️ — many dishes can be made from the same recipe!

### ⚙️ How It Works
- Docker shares the host OS kernel → efficient performance
- Each container has its own filesystem/environment → isolation
- Allows Linux workloads like ROS 2 to run on Windows/macOS

---

## 💻 2️⃣ Install Docker Desktop

Download and install **Docker Desktop**:

| OS | Download Link |
|----|---------------|
| **Windows** | https://docs.docker.com/desktop/setup/install/window-install/ |
| **macOS (Intel & Apple Silicon)** | https://docs.docker.com/desktop/setup/install/mac-install/ |


After installation, **open Docker Desktop** and make sure it shows:

> 🟢 Docker Engine: Running

---

## 🧑‍💻 3️⃣ Open a Terminal

- **Windows** → PowerShell / Command Prompt  
- **macOS** → Terminal  
- Or Docker Desktop → Open in Terminal

Check if Docker works:

```bash
docker --version
```
---

## ▶️ 4️⃣ Run ROS 2 Jazzy Desktop Container

Copy and run this command in the terminal:
```bash
docker run -p 6080:80 --security-opt seccomp=unconfined --shm-size=512m adtyp/ros2-desktop-vnc:jazzy
```

Keep the terminal open while the container is running.

---
## 🌐 5️⃣ Access the ROS Desktop (noVNC)

Open your browser and enter:

> http://localhost:6080


A full ROS 2 Jazzy Linux Desktop will appear inside your browser

