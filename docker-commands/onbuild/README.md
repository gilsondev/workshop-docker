# ONBUILD command

The ONBUILD instruction adds to the image a trigger instruction to be executed at a later time, when the image is used as the base for another build. The trigger will be executed in the context of the downstream build, as if it had been inserted immediately after the FROM instruction in the downstream Dockerfile.

## Build images

```bash
docker build -t foo_image:latest -f Dockerfile_foo .
```

```bash
docker build -t bar_image -f Dockerfile_bar .
```
