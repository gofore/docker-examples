SDK in container and multi-stage build
======================================

Note that this example requires Docker CE 17.05+.

Building the desired binary usually requires
additional tooling and SDKs which result big and
bloated images.

Multi-stage builds split image building in multiple
stages where deliverables from an earlier image can
be used in new image allowing the final binary image
to be as small as possible.


Build images with

`$ docker build -f Dockerfile.bad -t myapp/bad .`

`$ docker build -f Dockerfile.good -t myapp/good .`

and then run containers

`$ docker run --rm myapp/bad`

`$ docker run --rm myapp/good`

and check the image sizes

`$ docker images`


#### Reference

https://docs.docker.com/engine/userguide/eng-image/multistage-build/
