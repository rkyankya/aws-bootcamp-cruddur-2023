# Week 1 — App Containerization

  ## Homework Challenge

1. ### Install Docker and run application on Local Machine

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

