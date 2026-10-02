# HowestPrime Infrastructure Test

This repository contains the infrastructure and test setup for the HowestPrime movie platform. It brings together the supporting services, Docker-based test environment, API containers, and the front-end apps used during integration testing.

## Overview

The project is designed to run the platform in a local containerized environment with:

- PostgreSQL for the movies database
- MongoDB for ticketing data
- LavinMQ for messaging
- Movies API
- Ticketing API
- Backoffice UI
- Client web app

## Repository structure

- `howestprime-test/` – Docker Compose environment and startup instructions
- `http_requests/` – HTTP files for quick API testing
- `Dockerfile` – image used for the ticketing microservice build
- `Commands.md` – Docker image build commands for related repositories

## Prerequisites

Before running the environment, make sure the following are installed:

- Docker
- Docker Compose
- Access to the required project images or repositories used by the stack

## Start the environment

From the repository root, run:

```bash
docker compose -f howestprime-test/docker-compose.yml up -d --remove-orphans
```

To stop it:

```bash
docker compose -f howestprime-test/docker-compose.yml down
```

## Service access

| Service | URL |
|---|---|
| Client WebApp | http://localhost:10200/ |
| Client Backoffice | http://localhost:10210/ |
| Movies API Swagger | http://localhost:40220/swagger |
| Ticketing API | http://localhost:40230/ |
| LavinMQ Management UI | http://localhost:40201/ |

## Useful commands

Check logs for a specific container:

```bash
docker logs -f <container_name>
```

## Related notes

- See `howestprime-test/run.md` for the test environment commands and quick links.
- See `Commands.md` for the image build commands used for the other microservices.
- See `http_requests/http_files.md` for information about `.http` files for API testing.

## Purpose

This repository acts as the local infrastructure layer for validating how the different HowestPrime services connect and communicate together in a realistic test environment.
