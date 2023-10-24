# docker-cheatsheet

This file will list a few of the most used commands to interact with Docker CLI.

```
docker run
```
Main command to run docker images locally. If the image is not present in the machine it will fetch from Docker's public repository if it exists.

```
docker container ls
```
Presents a list of running containers. If desired to list all containers (including stopped state) append the flag ```-a```.

```
docker rm <container-name | container-id>
```
Removes the docker container. If container is in running state you can force the removal by appending the flag ```-f```.

```
docker stop <container-name | container-id>
```
Stop the docker container in running state.

```
docker start <container-name | container-id>
```
Starts a container in stopped state.
