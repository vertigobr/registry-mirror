# registry-mirror

Docker Registry Mirror (Docker Hub).

## Automated build

Since automated builds are no longer available for free, this build has been moved to Github Action.

Build uses buildkit in order to produce multi-platform images.

## Manual build

To build multi-platform images locally:

```sh
# must "docker login" before push
docker buildx create --use
docker buildx build --platform linux/amd64,linux/arm64 -t vertigo/registry-mirror .
```
