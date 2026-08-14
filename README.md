# Docker Containerization Lab 🐳

A hands-on Docker lab focused on understanding containerization, networking, storage, and container-to-container communication using Docker on Ubuntu running on AWS EC2.

This project documents practical implementation and troubleshooting rather than only theoretical concepts.

---

## 🎯 Objective

The objective of this lab is to build a strong practical understanding of Docker fundamentals and how containers behave in a cloud-based Linux environment.

The lab covers:

- Container lifecycle management
- Port mapping
- Docker bridge networking
- Container-to-container communication
- Docker internal DNS
- Persistent storage using Docker volumes
- Bind mounts
- Host-to-container and container-to-host file sharing
- Basic Docker troubleshooting

---

## 🏗️ Lab Environment

| Component | Configuration |
|---|---|
| Cloud Platform | AWS EC2 |
| Operating System | Ubuntu Linux |
| Container Platform | Docker |
| Network Driver | Bridge |
| Web Server | Nginx |
| Access | SSH |

---

## 📚 Topics Covered

| # | Topic | Status |
|---|---|---|
| 01 | Docker Container Basics | ✅ Completed |
| 02 | Port Mapping | ✅ Completed |
| 03 | Docker Networking | ✅ Completed |
| 04 | Docker Volumes | ✅ Completed |
| 05 | Bind Mounts | ✅ Completed |
| 06 | Dockerfile & Custom Images | 🔜 Next |
| 07 | Docker Compose | 🔜 Planned |
| 08 | Multi-Container Application | 🔜 Planned |
| 09 | Docker + AWS Deployment | 🔜 Planned |

---

## 1. Docker Container Basics

Learned how to:

- Run Docker containers
- List running containers
- List all containers
- Access a running container
- Execute commands inside containers
- Stop and remove containers
- Understand container names and IDs

### Commands Practiced

```bash
docker ps
docker ps -a
docker run
docker exec
docker stop
docker rm
