# the base image to create the image from
FROM python:3.6.0-alpine

# copies local directory static content under /src
# in container
COPY static/ /src

# sets the working directory as /src
WORKDIR /src

# instructs Docker that the container listens port 8080
EXPOSE 8080

# defines an executable command in exec form
ENTRYPOINT [ "python3", "-m", "http.server", "8080" ]
