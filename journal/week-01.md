# Week 1 — App Containerization

## Homework Challenge

### Install Docker and run application on Local Machine

Installed Docker Desktop by following the instructions on the [Docker Desktop Installation Instructions](https://docs.docker.com/get-docker/) page.

To make it run locally i set the **FRONTEND_URL** and **BACKEND_URL** environment variables to `"*"`. And **REACT_APP_BACKEND_URL** to `http://127.0.0.1:4567`.

Then ran docker-compose up to start the app.
![Local Variables set](assets/docker-compose.svg)

To access the app it was on `http://127.0.0.1:3000`. Was able to access both the front and backend as the app was working as exected.

![Proof of working app](assets/working-app.png)

Docker images and network were also created as expected.
![Docker Containers](assets/docker-container.png)

Docker Compose was used to run the app.
![Docker Compose](assets/docker-comp.png)

### Push and tag a image to DockerHub

First I created a Docker repository on DockerHub. Then I tagged the image with my DockerHub username/repository:tag and pushed it to DockerHub.
I set it to public so that anyone can access it.

[Published Docker Image](https://hub.docker.com/repository/docker/rkyankya/aws-bootcamp/general)

![Docker Image](assets/docker-image.png)

### Multi-stage building for a Dockerfile build

I used the frontend Dockerfile for this assignment. The first stage, named "build", is used to build the application. It starts with the base image of Node.js, copies the application code to the container. The second stage, named "run", is used to run the application. It starts with the smaller Alpine-based Node.js image, copies the built application from the previous stage and runs it.

![Dockerfile](assets/dockerfile-front.svg)
