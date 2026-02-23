# 🐳 Docker on AWS EC2 – Complete Beginner to Practical Guide

This repository documents my hands-on journey of installing Docker on AWS EC2, containerizing applications (Java & Flask), running MySQL in containers, and understanding Docker fundamentals.

This guide is written in a structured way so that beginners can follow it step-by-step.

---

# 📌 Table of Contents

1. What is Docker?
2. Key Docker Concepts
3. Installing Docker on AWS EC2
4. Essential Docker Commands
5. Building Custom Docker Images
6. Running Applications in Containers
7. Running MySQL in Docker
8. Dockerfile Explanation
9. Common Errors & Fixes
10. Interview Notes
11. Real Workflow Summary

---

# 1️⃣ What is Docker?

Docker is a containerization platform that allows you to package applications and their dependencies into lightweight containers.

Containers ensure that applications run the same way on:
- Local Machine
- Cloud Servers
- Production Environments

---

# 2️⃣ Key Docker Concepts

| Term | Meaning |
|------|----------|
| Image | Blueprint of an application |
| Container | Running instance of an image |
| Dockerfile | Script used to build an image |
| Volume | Persistent storage |
| Port Mapping | Connecting container port to host port |
| Environment Variable | Runtime configuration values |

---

# 3️⃣ Installing Docker on AWS EC2

## Step 1: Launch EC2 Instance
- Ubuntu 24.04 LTS
- t2.micro
- Allow SSH (22)
- Allow HTTP (80)

## Step 2: Connect via SSH

```bash
chmod 400 docker.pem
ssh -i docker.pem ubuntu@<public-ip>
