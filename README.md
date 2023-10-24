# docker-cheatsheet

This file will list a few of the most used commands to interact with Docker CLI.

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
