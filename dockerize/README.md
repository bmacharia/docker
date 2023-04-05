# Dockerize a simple Application

First and foremost have Docker installed on your machine.

## Download a simple nodejs applicatipn

```
  wget https://raw.githubusercontent.com/vladimirmukhin/nodejs-hello/main/app.js
```

## Launch the application locally

```
  node app.js
```

## Make Sure the application responds on port 3000

```
  curl http://127.0.0.1:3000/
```

## Create a file called Dockerfile and add the following lines inside

### Use nodejs as your base image

```
  FROM node:latest
```

### On a container startup run the application

```
  CMD node app.js
```

### Build the container

```
  docker build -t nodejs-hello:latest .
```

### Run the container

```
  docker run -d -p 3000:3000 nodejs-hello:latest
```

### Make sure the applicatio responds on port 3000 but this time from the container.

```
  curl http://127.0.0.1:3000/
```
