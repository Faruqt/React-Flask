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

## Docker
Writing Dockerfile for both frontend and backend 
>step1: create Dockerfile and write commands
`vi Dockerfile`

>step2: Creating Docker image in frontend and backend using :
`docker build -t <imagename> . `

>step3: Creating container using Docker image by this command :
`docker run -itd --name <container_name> -p <portno> <imagename>`

>step4: Checking the containers created using :
>To see running containers
`docker ps` 
>To see running and non-running containers
`docker ps -a` 

>step5: In browser exposing the container by :
>`localhost:portno`

## Dockerswarm
Creating Dockerstackfile
>step1: Initializing dockerswarm in manager node by :
>`docker swarm init --advertise-addr <IPaddr of manager node>`

>step2: Assigning workernode to managernode using managernode token  
>`docker swarm join --token (token will be provided after executing step1)`

>step3: Creating the dockerstackfile by :
>`vi docker.stack.yml` 

>step4: Deploying the docker stack using :
>`docker stack deploy -c docker.stack.yml <name>`

>step5: Exposing the container in browser by :
>`ipaddr:portno`
