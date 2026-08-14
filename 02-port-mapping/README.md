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



## Evidence

### Docker Port Mapping

The container is exposing port `80` through host port `8080`.

![Docker Port Mapping](../screenshots/docker-container-port-mapping.png)

### Web Application Output

The Dockerized web application was successfully accessed through the exposed port.

![Docker Web Application](../screenshots/docker-webapp-browser.png)
