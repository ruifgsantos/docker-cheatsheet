# docker-cheatsheet

## This file will list a few of the most used commands to interact with Docker CLI and Dockerfile.

### Docker CLI

```
docker run
```
Main command to run docker images locally. If the image is not present in the machine it will fetch from Docker's public repository if it exists.
</br>
</br>
```
docker container ls
```
Presents a list of running containers. If desired to list all containers (including stopped state) append the flag ```-a```.
</br>
</br>
```
docker rm <container-name | container-id>
```
Removes the docker container. If container is in running state you can force the removal by appending the flag ```-f```.
</br>
</br>
```
docker stop <container-name | container-id>
```
Stop the docker container in running state.
</br>
</br>
```
docker start <container-name | container-id>
```
Starts a container in stopped state.
</br>
</br>
```
docker rmi <image-id>
```
Removes local docker images.
</br>
</br>
```
docker logs <container-name | container-id>
```
Displays all container logs until the execution of the command. If needed to follow the real time logs, append the flag ```-f```.
</br>
</br>
```
docker build <path-to-dockerfile>
```
Create a custom docker image from a custom Dockerfile. To tag the image with correct name, flag ```-t```needs to added like so ```docker build -t my-custom-image:1.0 ./path-to-Dockerfile```
</br>
</br>
```
docker exec -it <container-name | container-id> <COMMAND>
```
Execute commands inside Docker image from the host machine. The flags ```-it``` correspond respectively to **I**nteractive **T**erminal allowing to create a shell to run commands. Usually this is widely adopted to navigate through the files inside the container using *bash* console, like so ```docker exec -it <container-name> bash```.
</br>
</br>
```
docker inspect <container-name | container-image | container-volume>
```

### Dockerfile instructions

```
ADD <source> <destination>
```
Allows to move files from one host destination or remote to a docker container destination.
</br>
</br>
```
COPY <source> <destination>
```
Similar to ADD instruction, but only accepts source files from host machine.
</br>
</br>
```
RUN <instruction>
```
Runs command instructions and creates docker layers for caching purposes.
</br>
</br>
```
CMD <instruction>
```
Sets the command to be executed when the Docker container starts. Can be overrided by ```docker run```parameterization.
</br>
</br>
```
ENTRYPOINT <instruction>
```
Configures the command to be executed when the container starts.
</br>
</br>
```
FROM <docker-image>
```
Initializes the base image to be used in the build process and execution of following instruction.
</br>
</br>
```
ENV <key> <valyue>
```
Sets environment variables to used inside the container.
</br>
</br>
```
VOLUME <directory>
```
Creates a mount point to be used with another directory in host machine.
</br>
</br>
```
ARG <key>=<value>
```
Arguments to be used when in build phase of the image. These become required and will triggers warn messages when not supplied.
</br>
</br>
```
WORKDIR <directory>
```
Sets the working directory for the following commands like ```RUN``` ```CMD```.
