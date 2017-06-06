Specific image version
======================

Using latest tag for image versions might result
breaking changes in the container. Defining specific
version for the image helps with predictability.

Maintainers of the images are responsible what the
version actually contains. For example python:2.7
does not automatically mean the image contains
python 2.7 binaries. It's just a convention for naming.


Build images with

`$ docker build -f Dockerfile.bad -t imageversion/bad .`

`$ docker build -f Dockerfile.good -t imageversion/good .`

and then run containers

`$ docker run --rm imageversion/bad`

`$ docker run --rm imageversion/good`


#### Reference

https://hub.docker.com/

https://hub.docker.com/_/python/
