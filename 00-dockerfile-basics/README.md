Dockerfile basics
=================

Copy static content inside Docker image and start
simple python web server serving the content.


Build image with

`$ docker build -t webserver .`

and then run container

`$ docker run --rm -t -p 9000:8080 webserver`


#### Reference

https://docs.docker.com/engine/reference/builder/
