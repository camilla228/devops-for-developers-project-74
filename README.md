[![Build, Test and Publish](https://github.com/tominvadim/devops-for-developers-project-74/actions/workflows/push.yml/badge.svg)](https://github.com/tominvadim/devops-for-developers-project-74/actions/workflows/push.yml)
### Hexlet tests and linter status:
[![Actions Status](https://github.com/TominVadim/devops-for-developers-project-74/actions/workflows/hexlet-check.yml/badge.svg)](https://github.com/TominVadim/devops-for-developers-project-74/actions)

# Docker Compose Package 

## Docker Image
Available on Docker Hub: [tominvadim/devops-for-developers-project-74](https://hub.docker.com/r/tominvadim/devops-for-developers-project-74)

## Requirements
- Docker 20.10+
- Docker Compose 1.27+

## Quick Start

### Development
```bash
make dev
# or
docker-compose up
```
### Application will be available at:
- Frontend: https://localhost (via Caddy reverse proxy)
- Backend API: http://localhost:8080

### Testing
```bash
make test
# or
docker-compose -f docker-compose.yml up --abort-on-container-exit
```
### Setup
```bash
make setup
```
### Project Structure
- docker-compose.yml - Production configuration with PostgreSQL
- docker-compose.override.yml - Development configuration with Caddy
- Dockerfile - Development image
- Dockerfile.production - Production image
- services/caddy/Caddyfile - Reverse proxy configuration
### CI/CD
- Tests run on every push to main branch
- Docker image automatically built and pushed to Docker Hub
