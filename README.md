# DevOps Assignment

## Project Overview

Production-ready DevOps infrastructure using:

- FastAPI
- Docker
- Docker Compose
- PostgreSQL
- Redis
- NGINX Reverse Proxy
- GitHub Actions CI/CD

## Architecture

Client
↓
NGINX
↓
FastAPI
↓
PostgreSQL

Redis (Caching Layer)

## Setup Instructions

### Clone Repository

```bash
git clone <repository-url>
cd devops-assignment
```

### Start Application

```bash
docker compose up --build -d
```

### Verify Containers

```bash
docker ps
```

### Health Check

```bash
http://localhost/health
```

Expected:

```json
{
 "status":"healthy"
}
```

## Services

| Service | Port |
|----------|------|
| FastAPI | 8000 |
| PostgreSQL | 5432 |
| Redis | 6379 |
| NGINX | 80 |

## Security Measures

- Environment variable isolation
- Docker container separation
- Reverse proxy using NGINX
- Git ignore for secrets

## CI/CD

GitHub Actions pipeline:

- Dependency validation
- Docker image build
- Docker compose validation

## Backup Strategy

PostgreSQL volume persistence enabled.

## Restart Strategy

Docker Compose manages service recovery.

## SSL Approach

NGINX ready for SSL certificate integration.
