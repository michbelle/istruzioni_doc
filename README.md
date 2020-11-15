# Docker instruction

Follow instruction on this [site](https://collabnix.com/introducing-new-docker-cli-api-support-for-nvidia-gpus-under-docker-engine-19-03-0-beta-release/) for using gpu inside docker.

### launch a docker from image

##### for normal docker

```sh
docker run -it --name ______  image(ex. ubuntu) 
```
##### for nvidia docker

First run   
```sh
xhost +local:docker
```

then
```sh
docker run -it --gpus all --env=DISPLAY --env=QT_X11_NO_MITSHM=1 -v /tmp/.X11-unix:/tmp/.X11-unix ros2_foxy /bin/bash
```

### start a container

```sh
docker start ______
```
### execute other commands on existing and alive docker
to launch the terminal in bash mode from ____ docker
```sh
docker exec -it ______ bash
```
Work fine with rviz and gazebo
