# 🐳 Docker on AWS EC2 – Complete DevOps Practice Guide

This repository documents my hands-on journey of installing Docker on AWS EC2, building Java and Flask applications, running MySQL in containers, managing networking, and understanding Docker fundamentals.

This serves as my personal DevOps reference and future guide.

---

# 📌 Project Overview

This project covers:

- Launching EC2 (Ubuntu 24.04 LTS)
- Installing Docker
- Fixing Docker permissions
- Running MySQL container
- Building Java Docker image
- Building Flask Docker image
- Port mapping & security groups
- Docker logs & lifecycle
- Database creation inside container
- Understanding Docker architecture

---

# ☁️ Step 1: Launch AWS EC2

- Ubuntu 24.04 LTS
- Instance type: t2.micro
- Key pair (.pem)
- Allow SSH (Port 22)
- Allow HTTP (Port 80)

---

# 🔐 Step 2: Connect to EC2

```bash
chmod 400 docker.pem
ssh -i "docker.pem" ubuntu@<public-dns>
