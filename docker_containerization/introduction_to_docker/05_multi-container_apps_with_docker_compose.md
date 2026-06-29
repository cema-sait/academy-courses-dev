---
name: Multi-container Apps with Docker Compose
tags: [docker, docker-compose, orchestration, containers]
learningOutcomes:
  - Understand Docker Compose fundamentals
  - Define multi-service applications
  - Manage application stacks
---

# Multi-container Apps with Docker Compose

## Compose fundamentals

A `compose.yml` file defines:

-   Services
-   Images or build contexts
-   Ports
-   Volumes
-   Networks
-   Dependencies

Example structure:

``` yaml
services:
  web:
    build: ./web
    ports:
      - "8080:80"
    depends_on:
      - redis

  redis:
    image: redis:latest
```

## Managing Compose applications

Start:

``` bash
docker compose up -d
```

View services:

``` bash
docker compose ps
```

Follow logs:

``` bash
docker compose logs -f
```

Stop:

``` bash
docker compose stop
```

Remove:

``` bash
docker compose down -v
```

## Hands-on exercise

Create your own `compose.yml` file for an application with multiple
services.
