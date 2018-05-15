# helm-docker

[![Docker Pulls](https://img.shields.io/docker/pulls/wolmi/helm-docker.svg?style=flat-square)](https://hub.docker.com/r/wolmi/helm-docker/)

Docker images are automatically built on [Docker
Hub](https://hub.docker.com/r/wolmi/helm-docker/):

- `latest` always corresponds with the latest build from master
- Docker `tag` always correspond with git `tag`

## Usage

`helm`, `gcloud` and `kubectl` are all available.

The image also includes the `helm diff` Helm Plugin.

## Docker

```bash
docker build -t devth/helm .
```

## Release procedure

1. Bump `VERSION` in the [Dockerfile](Dockerfile)
1. Commit and create tag matching the version:

   ```bash
   version=v2.9.0
   git commit -am "Bump to $version"
   git tag $version
   git push && git push --tags
   ```
