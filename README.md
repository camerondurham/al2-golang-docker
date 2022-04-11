# unofficial-al2-golang docker image

As suggested in the repo's name, this is very unofficial and **NOT** supported by my employer.

However, feel free to fork and use how you please! :)

Docker Hub Link: [camerondurham/unofficial-al2-golang](https://hub.docker.com/repository/docker/camerondurham/unofficial-al2-golang)

Tagging is kind of a mess, but followed the <GO_VERSION>-<GO_ARCH>

```bash
docker run -it camerondurham/unofficial-al2-golang:1.17.7-arm64 bash
bash-4.2# go version
go version go1.17.7 linux/arm64
```

Build Args:

- `GO_ARCH`: Go architecture (e.g. `arm64`, `amd64`), should match naming scheme from https://go.dev/dl/ since that's where the image downloads from in build process [default: `arm64`]
- `GO_VERSION`: Go major/minor version, also from https://go.dev/dl/ (e.g. `1.17.7`, `1.18`) [default: `1.17.7`]


Example build command:

```bash
docker buildx build --platform linux/amd64 --build-arg GO_VERSION=1.17.8 --build-arg GO_ARCH=amd64 -t amd64 .
```

