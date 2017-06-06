Dockerfile command ordering
===========================

Depending on the command in Dockerfile there is
different semantics for fs layer invalidation.
Expensive commands should come first and by default
unnecessary layers should be avoided.

Some commands only see if the command itself is changed
but for example COPY and ADD detect changes if the
required files are changed.


Build images with

`$ docker build -f Dockerfile.bad -t ordering/bad .`

`$ docker build -f Dockerfile.good -t ordering/good .`

and then run containers and look up for the host port

`$ docker run --rm -i -t -P --name ordering_bad ordering/bad`

`$ docker port ordering_bad`

`$ docker run --rm -i -t -P --name ordering_good ordering/good`

`$docker port ordering_good`


#### Reference

https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/

https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/
