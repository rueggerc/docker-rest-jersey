Project to learn/demonstration RESTful using Jersey

# Build Image
docker image build -t docker-rest-jersey:1.0 .

# Run Detached
docker container run -d --name rest1 -p 8080:8080 docker-rest-jersey:1.0

# Run Detached
docker container run -d --name rest1 -p 8080:8080 restjersey:latest
docker container run -d --name rest1 -p 8088:8080 restjersey:latest
docker container run -d --name rest2 -p 8089:8080 restjersey:latest


# Run Interactive
docker container run -it --name rest1 -p 8080:8080 restjersey:latest
docker container run -it restjersey:latest /bin/bash

# Stop
docker container stop <id or name>

#Remove Container
docker rm <id> or <name>

#Remove Exited Containers
docker rm $(docker ps -a -q -f status=exited)

#Inspect
docker image inspect tomcat:8.0.47-jre8

#Remove Image
docker rmi <IMAGE ID>
