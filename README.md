# 🐳 Docker on AWS EC2 -- Complete Beginner to Practical Guide 

This repository documents my hands-on journey of installing Docker on AWS EC2, containerizing applications (Java & Flask), running MySQL in containers, and understanding Docker fundamentals.

This guide is structured so beginners can follow it step-by-step and use it as future reference.

---

# 📌 Table of Contents

1. What is Docker?
2. Key Docker Concepts
3. Installing Docker on AWS EC2
4. Verifying Docker Installation
5. Running MySQL in Docker
6. Building a Java Docker Application
7. Building a Flask Docker Application
8. Opening Port 80 in AWS Security Group
9. Essential Docker Commands
10. Dockerfile Explanation
11. Common Errors & Fixes
12. Architecture Overview
13. What I Learned

----

# 1️⃣ What is Docker?

Docker is a containerization platform that allows you to package applications and their dependencies into lightweight containers.

Containers ensure applications run consistently on:
- Local Machine
- Cloud Servers
- Production Environments

-----

# 2️⃣ Key Docker Concepts

| Term | Meaning |
|------|----------|
| Image | Blueprint of an application |
| Container | Running instance of an image |
| Dockerfile | Script used to build an image |
| Volume | Persistent storage |
| Port Mapping | Connecting container port to host port |
| Environment Variable | Runtime configuration |

----

# 3️⃣ Installing Docker on AWS EC2

## Step 1: Launch EC2 Instance

- Ubuntu 24.04 LTS
- Instance type: t2.micro
- Allow SSH (Port 22)
- Allow HTTP (Port 80)
- Create a key pair (.pem)

---

## Step 2: Connect via SSH

```bash
chmod 400 docker.pem
ssh -i docker.pem ubuntu@<public-ip>



