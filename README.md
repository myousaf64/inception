# inception

A multi-service Docker infrastructure built from scratch: NGINX with TLS, WordPress
with php-fpm, and MariaDB, each in its own container on a dedicated network, with
persistent volumes. A 42 Abu Dhabi project.

## Build and run

```
make up      # build images and start the stack
make down    # stop the stack
make clean   # stop and remove volumes and images
make re      # clean rebuild
```

## Notes

- Every image is built from a Dockerfile in `srcs/requirements/`; no pre-built
  application image is pulled.
- Configuration comes from an env file that is deliberately not committed.
- Requires Docker and Docker Compose.
