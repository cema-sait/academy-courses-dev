---
name: Service Delivery and Production Considerations
tags: [docker, security, production, containerization]
learningOutcomes:
  - Understand image layers and caching
  - Apply container security practices
  - Manage container resources and cleanup
---

# Service Delivery and Production Considerations

## Image layers and caching

Inspect image layers:

``` bash
docker history <image>
```

Build multi-platform images:

``` bash
docker buildx build --platform linux/amd64,linux/arm64 .
```

## Security and scanning

Recommended practices:

-   Keep base images updated.
-   Pin image versions.
-   Avoid running containers as root.
-   Remove unnecessary capabilities.

Scan images:

``` bash
docker scout <image>
```

## Operational tools

Copy files:

``` bash
docker cp
```

Manage storage and networks:

``` bash
docker volume ls
docker network ls
```

Cleanup:

``` bash
docker system prune
docker image prune
```

## Hands-on exercise

Modify an application image to run as a non-root user and verify it
still works.
