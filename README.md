# React + Flask Application

This is an application which contains a connected flask backend to a react frontend

## Backend
Step1: Enter the backend directory and create and activate your environment:

For mac/unix users: 

**create:** ```python3 -m venv env```

**activate:** `source env/bin/activate`

For windows users: 

**create:** `py -m venv env`

**activate:** `.\env\Scripts\activate`


Step2: Then install the requirements using:
`pip install -r requirements.txt`

## Available Scripts

Return to the base directory and run: `npm install` before running the scripts below.

Then, run `npm run start-backend` to start the flask backend server.

Open [http://localhost:5000](http://localhost:5000) to view it in the browser.

Next, run `npm start` to start the frontend section of the application.

Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

## Testing the application
Click on the button that appears on the page to make the request to the API endpoint in the backend. 

# Docker

![Docker](https://jeddict.github.io/tutorial/Docker/DOCKER.png)

Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.

# Dockerfile

A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image

# Docker Compose 

![Docker Compose](https://jeddict.github.io/tutorial/Docker/COMPOSE.png "Docker Compose Logo")


Docker Compose is a tool for running multi-container applications on Docker
defined using the [Compose file format](https://compose-spec.io).
A Compose file is used to define how one or more containers that make up
your application are configured.
Once you have a Compose file, you can create and start your application with a
single command: `docker compose up`.



Quick Start
-----------

Using Docker Compose is a three-step process:
1. Define your app's environment with a `Dockerfile` so it can be
   reproduced anywhere.
2. Define the services that make up your app in `docker-compose.yml` so
   they can be run together in an isolated environment.
3. Lastly, run `docker compose up` and Compose will start and run your entire
   app.

A Compose file looks like this:

```yaml
services:
  web:
    build: .
    ports:
      - "5000:5000"
    volumes:
      - .:/code
  redis:
    image: nginx
```

Contributing
------------

Dont hesitate to create a pull request
