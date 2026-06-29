---
name: Basic Docker Operations
tags: [docker, docker-compose, containerization, containers]
learningOutcomes:
    - Verify a Docker or Podman installation
    - Run, inspect, manage, and troubleshoot containers
    - Understand common Docker CLI operations

---

# Basic Docker Operations

## Installing and verifying your environment

-   Confirm that Docker or Podman is installed and running.

``` bash
docker info
```

-   List local images:

``` bash
docker images
```

-   Pull images:

``` bash
docker pull <name>:<tag>
```

-   List containers:

``` bash
docker ps -a
```

## Working with containers

Start an interactive Ubuntu container:

``` bash
docker run -it --name myubuntu ubuntu:latest bash
```

Detach without stopping:

    Ctrl+p Ctrl+q

Attach again:

``` bash
docker attach myubuntu
```

Stop and remove:

``` bash
docker stop myubuntu
docker rm myubuntu
```

Execute commands inside a running container:

``` bash
docker exec -it <container> <command>
```

Inspect containers and images:

``` bash
docker inspect <image_or_container>
docker history <image>
```

## Hands-on exercise

Run an NGINX web server:

``` bash
docker run -d -p 8080:80 nginx:latest
```

Open:

    http://localhost:8080

View logs:

``` bash
docker logs <container>
```

Clean up:

``` bash
docker rm -f <container>
```
