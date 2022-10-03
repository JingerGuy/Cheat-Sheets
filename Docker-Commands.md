# Docker Commands

## Docker Images
### Search for images
``` 
docker search
```
### Download an image
```
docker pull
```
### Upload an image to registry
```
docker push
```
### Tag an image or rename it
```
docker tag
```
### Delete an image from local disk
```
docker rmi
```
---
## Docker Run
### Runs the container in detached mode
```
docker run -d
```
### Publishes a port. Maps a port inside of the container to a port on the host so that it is accessible from the host's IP address
```
docker run -p [HOST PORT]:[CONTAINER PORT]
```
### Names the container. If no name is set, the container is given a randomly generated name
```
docker run --name [NAME]
```
### Sets an environment variable inside the container
```
docker run -e [VARIABLE_NAME]=[VARIABLE_VALUE]
```
---
## Containers
### Returns the current running containers
``` 
docker ps
```
### Returns all containers in a table
```
docker ps --all or -a
```
### Filter output based on a condition provided
```
docker ps --filter or -f
```
### Returns only the container IDs
```
docker ps --quiet or -q
```
### This returns the logs of a container 
```
docker logs [CONTAINER_NAME]
```
---
## Docker exec
### The docker exec command executes commands inside a container
```
# Example, creates a text file inside the container
docker exec mycontainer touch myfile.txt
```
### Interactive shell in a container
```
# docker exec -it [CONTAINER_NAME] [SHELL INTERPRETER]
# Example:
docker exec -it jenkins bash
```
---

# Start, stop, rename and remove existing containers
## Docker Start
### Starts a stopped container
```
# docker start [CONTAINER_NAME]
# Example:
docker start mysql_container
```

## Docker Stop
### Stops a running container
```
# docker stop [CONTAINER_NAME]
# Example:
docker stop mysql_container
```
## Docker Remove
### Deletes a container
```
docker rm
```
### Force remove docker container
```
docker rm --force or -f
```
### Removes volumes associated with the container
```
docker rm --volumes or -v
```
## Docker Rename
### Renames container
```
# docker rename [CONTAINER_NAME] [NEW_NAME]
# Example:
docker rename mysql_container app_db
```
---
# Docker Build
```
# docker build [CONTEXT]
docker build .
```
### Execute a Dockerfile from a different directory
```
docker build -f [PATH_TO_DOCKERFILE] [CONTEXT]
```
### Tag (name) the image being created
```
docker build -t [USER]/[IMAGE]:[TAG]
```
---
# Docker Networking
## Managing networks
### Creates a new user-defined bridge network
```
docker network create [NETWORK]
```
### Allows you to create different types of networks
```
docker network create --driver [NETWORK TYPE] [NETWORK]
```
### Lists available networks on the host machine
```
docker network ls
```
### Connects a container to a network
```
docker network connect [NETWORK] [CONTAINER]
```
### Disconnects a container from a network
```
docker network disconnect [NETWORK] [CONTAINER]
```
### Deletes a network
```
docker network rm [NETWORK]
```
---
# Volumes
## Managing Volumes
### Creates a volume
```
docker volume create [NEW_VOLUME_NAME]
```
### Lists the volumes stored locally
```
docker volume ls
```
### Deletes an existing volume
```
docker volume rm [VOLUME_NAME]
```
### Returns a JSON with metadata about the volume
```
docker volume inspect [VOLUME_NAME]
```
## Mounting Volumes

### -v or --volume
```
# docker run --volume [VOLUME_NAME]:[MOUNT_POINT] [IMAGE]
docker run --volume my-volume:/usr/share/nginx/html nginx
```
### --mount
```
# docker run --mount type=volume,source=[VOLUME_NAME],target=[MOUNT_POINT] [CONTAINER_NAME]
docker run --mount source=my-volume,destination=/usr/share/nginx/html nginx
```
---
# Docker Compose
## Docker Compose Run
```
docker-compose up -d 
```
## View the Running Containers Using Compose
```
docker-compose ps
```

---
# Docker Swarm


---