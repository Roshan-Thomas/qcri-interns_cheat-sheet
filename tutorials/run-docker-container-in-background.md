# How to run a Docker container in the background?

To run a docker container in the background or the detached mode from the terminal, you can use the `docker run` command followed by the `-d` flag (or detached flag) and followed by the name of the docker image you need to use in the terminal.

```sh
# Run docker container in the background
# or detached mode in the terminal
docker run -d <YOUR_DOCKER_IMAGE_NAME>
```

For example, lets say we want to make a docker container from the `docker/getting-started` docker image and then run the docker container in the background or detached mode. So here we can use the `docker run` command like this,

```
docker run -d docker/getting-started
```

**Now since the docker container is started in the background you can use the terminal for other purposes too.**

That's all 😄!
