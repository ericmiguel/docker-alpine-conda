# Alpine + Miniconda3 Docker image

Based on Alpine Linux, this image is ```~50% lighter``` than ```continuumio/miniconda3```.

More details about Alpine compiled against glibc, see [frolvlad`s repository](https://github.com/Docker-Hub-frolvlad/docker-alpine-glibc).

## Versions
- miniconda ```4.10.3```
- python ```3.9.5```
- alpine ```3.14```

## Usage Example

```bash
docker pull ericmiguel/alpine-conda:{tag}
```

```Dockerfile
FROM ericmiguel/alpine-conda:0.0.1
LABEL MAINTAINER="Your name"

COPY requirements.yaml /app
RUN conda env update -f requirements.yaml -n base

COPY app /app
WORKDIR /app
CMD ["bash", "-c", "python app"]
```
