# docker-gallery
Dockerfiles for hub.docker.com to build convenient images.

## Multi-platform images
```sh
% docker buildx build --platform linux/amd64,linux/arm64 -t kirl0076/rsyslog:latest --push .
```