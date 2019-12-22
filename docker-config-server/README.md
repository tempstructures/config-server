# Docker Config Server Example

> Simple Docker example of config server/service app


## config-server 

Place jar file of project config-server in this directory to create image
Run Dockerfile to create image
```
docker build -t “config-server:Dockerfile” .
```

## bank-account-service
Contain jar file of project bank-account-service in this directory to create image
Run Dockerfile to create image
```
docker build -t “bank-account-service:Dockerfile” .
```

## docker-compose
Once the images are created run the compose file to create and run container
```bash
# Run in Docker
docker-compose up
# use -d flag to run in background

# Tear down
docker-compose down

