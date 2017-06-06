Service dependencies and networks
=================================

In real world services depend on each other.
Application or integration might fail if the
depended on database is not running.

Services also have logical network boundaries
that can be modeled with Docker Compose Networking.

Docker Compose introduces networks and depends
on syntax that help to build complex systems within
Docker.

These solutions are not bullet proof because depends
on cannot make sure the actual services are running.
Networks created in Docker Compose are not usually
the same as real operational environment networks.


Build images with

`$ docker-compose build`

and start database

`$ docker-compose up applicationdb`

and run the integration

`$ docker-compose run --rm application`

or start everything in one go

`$ docker-compose up`

and finally stop services

`$ docker-compose stop`


#### Reference

https://docs.docker.com/compose/

https://docs.docker.com/compose/compose-file/

https://docs.docker.com/compose/networking/

