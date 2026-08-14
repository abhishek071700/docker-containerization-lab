# Docker Port Mapping

## Objective

Understand how a Docker container can expose an application to the host system using port mapping.

---

## Architecture

```text
AWS EC2 / Ubuntu Host
        |
        | Port 8080
        ↓
Docker Container
        |
        | Port 80
        ↓
Nginx Web Server
        |
        ↓
HTML Application
