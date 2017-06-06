Mount volume and host directory to container
============================================

All container data is lost when the container is
deleted so nothing should be stored inside a
container. Docker provides a concept of volumes
which allows storing data outside of the container.

Docker daemon must with the operating system super
user privileges and therefore all commands run
inside a container use the same user. This will be
a problem when a writable volume is provided from the
host machine.

Docker volumes tackle the issue of writable directory
mounts from host machine yet still providing permanent
data storage for containers.


Build image with

`$ docker build -t volumes .`

and then run container

`$ docker run --rm -v $PWD/mydata:/data volumes`

or create a volume and then run container

`$ docker volume create mydata`

`$ docker run --rm -v mydata:/data volumes`

and inspect the contents of the volume

`$ docker run --rm -i -t mydata:/data ubuntu:16.10 /bin/bash`


#### Reference

https://docs.docker.com/engine/tutorials/dockervolumes/
