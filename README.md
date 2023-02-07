## Deploy Docker application on a server with Docker Compose

This app shows a simple user profile app set up using

- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage

All components are docker-based

### Technologies used:

Docker compose, Node.js,HTML, CSS, JavaScript, AWS ECR, MongoDB, MongoExpress

### Project Description:

1- Copy Docker-compose file to remote server

2- Login to private Docker registry on remote server to fetch our app image

3- Start our application container with MongoDB and MongoExpress services using docker compose

### With Docker compose

#### To start the application

Step 1: Create docker-compose file

![Alt text](app/images/compose-yaml.png?raw=true)

Step 2: Copy docker-compose file to a remote server

Step 3: login to private docker registry on remote server via AWS CLI

![Alt text](app/images/view-docker-login-command.png?raw=true)

![Alt text](app/images/docker-login-command.png?raw=true)

Step 4: Run node-app, mongodb, mongo-express containers by docker compose on remote server

    docker compose up

or

    docker compose -f docker-compose.yaml up

Step 5: Node app , mongodb, mongo-express are running

node app: listening on port 3000

mongodb: listening on port 27015

mongo-express: listening on prot 8083

![Alt text](app/images/Screenshot%202023-02-07%20at%206.57.46%20pm.png?raw=true)

Step 6: open mongo-express on browser via port 8083

1-Create a new database: my-app

2-Create a new collection inside my-app database: users

Step 7: edit the user profile

![Alt text](app/images/Screenshot%202023-02-07%20at%206.56.15%20pm.png?raw=true)

![Alt text](app/images/Screenshot%202023-02-07%20at%206.56.57%20pm.png?raw=true)
Step 8: Stop the node app

    docker compose down

or

    docker compose -f docker-compose.yaml down
