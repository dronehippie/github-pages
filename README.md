# github-pages

[![Current Tag](https://img.shields.io/github/v/tag/dronehippie/github-pages?sort=semver)](https://github.com/dronehippie/github-pages) [![Build Status](http://drone.webhippie.de/api/badges/dronehippie/github-pages/status.svg)](http://drone.webhippie.de/api/badges/dronehippie/github-pages) [![Join the Matrix chat at https://matrix.to/#/#webhippie:matrix.org](https://img.shields.io/badge/matrix-%23webhippie-7bc9a4.svg)](https://matrix.to/#/#webhippie:matrix.org) [![Docker Size](https://img.shields.io/docker/image-size/dronehippie/github-pages/latest)](https://hub.docker.com/r/dronehippie/github-pages) [![Docker Pulls](https://img.shields.io/docker/pulls/dronehippie/github-pages)](https://hub.docker.com/r/dronehippie/github-pages) [![Go Reference](https://pkg.go.dev/badge/github.com/dronehippie/github-pages.svg)](https://pkg.go.dev/github.com/dronehippie/github-pages) [![Go Report Card](https://goreportcard.com/badge/github.com/dronehippie/github-pages)](https://goreportcard.com/report/github.com/dronehippie/github-pages) [![Codacy Badge](https://app.codacy.com/project/badge/Grade/6439ac599f6f4f709f154e4314bcf383)](https://www.codacy.com/gh/dronehippie/github-pages/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=dronehippie/github-pages&amp;utm_campaign=Badge_Grade)

Drone plugin to publish GitHub pages. For the usage information and a listing of the available options please take a look at the [documentation](https://dronehippie.github.io/github-pages/).

## Build

Build the binary with the following command:

```console
export GOOS=linux
export GOARCH=amd64

make build
```

## Docker

Build the image with the following command:

```console
docker build \
  --label org.opencontainers.image.source=https://github.com/dronehippie/github-pages \
  --label org.opencontainers.image.revision=$(git rev-parse --short HEAD) \
  --label org.opencontainers.image.created=$(date -u +"%Y-%m-%dT%H:%M:%SZ") \
  --file docker/Dockerfile.amd64 --tag dronehippie/github-pages .
```

## Usage

```console
docker run --rm \
  -e PLUGIN_DUMMY="dummy" \
  -v $(pwd):$(pwd) \
  -w $(pwd) \
  dronehippie/github-pages
```

## Security

If you find a security issue please contact [thomas@webhippie.de](mailto:thomas@webhippie.de) first.

## Contributing

Fork -> Patch -> Push -> Pull Request

## Authors

-   [Thomas Boerger](https://github.com/tboerger)

## License

Apache-2.0

## Copyright

```console
Copyright (c) 2021 Thomas Boerger <thomas@webhippie.de>
```
