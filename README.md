# Docker Containerization Lab 🐳

[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)
[![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Linux](https://img.shields.io/badge/Linux-Ubuntu-FCC624?style=for-the-badge&logo=linux&logoColor=black)](https://ubuntu.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

> A hands-on Docker lab covering containerization, networking, persistent storage, and container-to-container communication — built and tested on Ubuntu running on AWS EC2.

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

[`01-container-basics/`](01-container-basics)

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
```

---

## 2. Port Mapping

[`02-port-mapping/`](02-port-mapping)

Learned how to:

- Expose container ports to the host
- Map host ports to container ports (`-p HOST:CONTAINER`)
- Run a containerized Nginx server reachable from outside the container
- Verify connectivity using `curl` and browser access via the EC2 public IP

### Commands Practiced

```bash
docker run -d -p 8080:80 nginx
docker port <container_id>
curl localhost:8080
```

---

## 3. Docker Networking

Docker networking allows containers to communicate with each other and provides controlled connectivity between application components.

In this lab, I created a custom Docker bridge network named `my-app-network` and connected the application containers to it.

### Custom Network Configuration

```bash
sudo docker network create my-app-network
---

## 4. Docker Volumes

[`04-docker-volumes/`](04-docker-volumes)

Learned how to:

- Create and manage named Docker volumes
- Persist data outside the container's writable layer
- Share a volume across multiple containers
- Confirm data survives container removal

### Commands Practiced

```bash
docker volume create my-data
docker run -d -v my-data:/usr/share/nginx/html nginx
docker volume inspect my-data
docker volume ls
```

---

## 5. Bind Mounts

[`05-bind-mounts/`](05-bind-mounts)

Learned how to:

- Mount a host directory directly into a container
- Edit files on the host and see changes reflected live inside the container
- Understand the difference between bind mounts and named volumes
- Share files between host and container in both directions

### Commands Practiced

```bash
docker run -d -v /home/ubuntu/site:/usr/share/nginx/html nginx
docker inspect --format='{{json .Mounts}}' <container_id>
```

---

## 📸 Screenshots

Supporting screenshots for each stage of the lab are available in [`screenshots/`](screenshots).

---

## 🔜 What's Next

- **Dockerfile & Custom Images** – building images from scratch instead of using base images
- **Docker Compose** – defining and running multi-container setups declaratively
- **Multi-Container Application** – wiring together an app + database container
- **Docker + AWS Deployment** – pushing images to ECR and running them on ECS/EC2

---

## 🎓 About This Lab

Part of my ongoing hands-on learning as a Cloud Pre-Sales Engineer building practical, infrastructure-adjacent skills alongside AWS architecture work. See my other repos for AWS Well-Architected reviews, cost optimization case studies, and architecture design examples.

## 📫 Connect With Me

[![Email](https://img.shields.io/badge/Email-abhishek071700%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:abhishek071700@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Abhishek%20Pandey-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/abhishek-pandey-045241316)
[![GitHub](https://img.shields.io/badge/GitHub-abhishek071700-181717?style=flat&logo=github&logoColor=white)](https://github.com/abhishek071700)

## 📄 License

This project is licensed under the [MIT License](LICENSE).
