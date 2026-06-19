# Infrastructure

Infrastructure as code for the Tamkeen platform.

This repository contains:

- Dockerfiles for services
- Docker Compose configurations
- Infrastructure-related setup and supporting files

## Project Structure

The repository is organized around container and deployment configuration files. Typical contents include:

- `docker-compose.yml` for running the application stack locally or in deployment environments
- `Dockerfile` files for building service images
- environment-related configuration files
- supporting infrastructure scripts and assets

## How to Run Docker Compose

1. Make sure Docker and Docker Compose are installed.
2. Review the required environment variables.
3. Start the stack:

```bash
docker compose up -d
```

4. To stop the stack:

```bash
docker compose down
```

If your setup uses a custom compose file, specify it with `-f`:

```bash
docker compose -f docker-compose.yml up -d
```

## Environment Variables

Before starting the stack, ensure the needed variables are defined in a `.env` file or exported in your shell.

Common examples may include:

- service ports
- database credentials
- API keys or secrets
- backend and frontend service URLs

Check the compose and Dockerfiles in this repository for the exact variables required by your setup.

## Deployment Steps

1. Build the images if needed:

```bash
docker compose build
```

2. Start the services:

```bash
docker compose up -d
```

3. Verify that all containers are running:

```bash
docker compose ps
```

4. Check logs if something fails:

```bash
docker compose logs -f
```

5. When you need to shut everything down:

```bash
docker compose down
```

## Purpose

The repo is used to manage containerized environments and deployment setup for the Tamkeen project.
