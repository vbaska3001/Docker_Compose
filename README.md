# Docker Compose – Multi-Service Web Deployment

This repository demonstrates a **Docker Compose–based deployment** of multiple web applications using isolated services and port mapping in docker.

## Services

- **Custom Web App**
  - Nginx-based application
  - Uses a **custom Docker image from Docker Hub**
  - Exposed via a dedicated port - 8080

- **Netflix Clone App**
  - Sample web application
  - Runs on a **separate port - 3000** to avoid conflicts

Both services are orchestrated using a single `compose.yaml` file.

---

## Prerequisites

- Docker
- Docker Compose (v2)

```bash
docker --version
docker compose version

Deployment:
git clone <repo-url:https://github.com/vbaska3001/Docker_Compose.git>
cd <repo-name:Docker_Compose>
docker compose -f docker-compose.yaml up -d
docker ps

Cleanup:
docker compose down
docker ps -a
docker stop ContainerID
docker rm ContainerID
```

## Access

| Service        | URL                                         |
| -------------- | ------------------------------------------- |
| Custom Web App | [http://localhost](http://localhost):8080 |
| Netflix App    | [http://localhost](http://localhost):3000 |


## Architecture Highlights
- Multi-container orchestration using Docker Compose
- Image pull from Docker Hub
- Nginx as reverse/static web server
- Port isolation per service
- Single-command deployment & teardown
---
## Screenshots
<img width="700" height="500" alt="Screenshot 2025-12-31 at 8 31 38 AM" src="https://github.com/user-attachments/assets/2fef17cb-7c95-4ed6-95ab-5daafd457afd" />
<img width="700" height="500" alt="Screenshot 2025-12-31 at 8 31 51 AM" src="https://github.com/user-attachments/assets/8bd91eb5-c783-405c-a4c3-f1c0136b3f65" />
<img width="700" height="500" alt="Screenshot 2025-12-31 at 8 30 11 AM" src="https://github.com/user-attachments/assets/a85ee2dd-03a4-4374-8f13-ebc92f4774fc" />
<img width="700" height="500" alt="Screenshot 2025-12-31 at 8 30 42 AM" src="https://github.com/user-attachments/assets/efc0c869-10d3-45cd-8587-14dffe9728b8" />
<img width="700" height="500" alt="Screenshot 2025-12-31 at 8 30 53 AM" src="https://github.com/user-attachments/assets/ba995ba1-267d-4f21-83d2-1f9d7796d48e" />
<img width="700" height="500" alt="Screenshot 2025-12-31 at 8 31 12 AM" src="https://github.com/user-attachments/assets/942dfb2b-cd4b-485e-84ab-21a023f4adb1" />

## Repo Note
- This repo is for training and learning friendly and can be used for practicising docker compose in a test environment.
- Before replicating and testing, make sure the ports and components are used only for test purposes.

