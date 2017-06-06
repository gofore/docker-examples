Installation of additional packages
===================================

Installation of additional packages for the operating
system can slow down the image build process radically.

There are also pitfalls how the package updates affect
the image predicatbility and file system layers.


Build images with

`$ docker build -f Dockerfile.bad -t packages/bad .`

`$ docker build -f Dockerfile.good -t packages/good .`

and then run containers

`$ docker run --rm packages/bad`

`$ docker run --rm packages/good`


#### Reference

https://docs.docker.com/engine/reference/builder/