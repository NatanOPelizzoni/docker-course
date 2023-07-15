# Docker Commands

## <span style="color:green">Docker Run</span>

### Default

- **docker run image_name :** Run an image in Docker.

- **docker run image_name:tag_name :** Run an image in Docker with a specific tag.

### Iteractive

- **docker run -it image_name :** Run an image in Docker and keep an interactive session in the terminal. Type `exit` or `ctrl+D` to exit the container.

### Detach

- **docker run -d image_name :** Run an image in Docker in the background.

### Ports
- **docker run -p 8080:80 image_name :** Run an image in Docker and map port 8080 of the container to port 80 of the host.

- **docker run -d -p 8080:80 image_name :** Run an image in Docker, map port 8080 of the container to port 80 of the host, and run it in the background.

### Naming

- **docker run --name my_container image_name :** Run an image in Docker and set a name for the container.

## Run and remove after stop

- **docker run -d --rm image_name :** Run an image in Docker in the background and remove it after it stops.

## <span style="color:green">Container Management</span>

### Start 

- **docker start id_or_name_of_container :** Start a container by its ID or name.

- **docker start -i id_or_name_of_container :** Start a container by ID or name in interactive mode.

### Stop

- **docker stop id_or_name_of_container :** Stop a container by its ID or name.

### Listing

- **docker ps :** List all running containers.

- **docker container ls :** An alternative way to list all running containers.

- **docker ps -a :** List all running and stopped containers.

- **docker container ls -a :** An alternative way to list all running and stopped containers.

### Log

- **docker logs id_or_name :** Show all logs of a container.

### Remove

- **docker rm id_or_name_of_container :** Remove a container by its ID or name.

- **docker rm -f id_or_name_of_container :** Forcefully remove a container by its ID or name.

### Renaming

- **docker rename id_or_name_of_container new_name :** Rename a container by its ID or name.

### Copy file or directory
- **docker cp id_or_name_of_container:/path/to/file/in/container /path/to/file/on/host :** Copy a file from a container to the host.

### Check what have in container

- **docker top id_or_name_of_container :** Show all processes running in a container.

### Check how was builded container

- **docker inspect id_or_name_of_container :** Show all information about a container.

## <span style="color:green">Docker image build</span>

### Default

- **docker build dockerfile_directory :** Build an image wihtout name from a Dockerfile.


- **docker build -f Dockerfile_name :** Build an image from a Dockerfile with a custom name.

### Naming

- **docker build -t image_name dockerfile_directory :** Build an image from a Dockerfile.

- **docker build -t image_name:tag_name dockerfile_directory :** Build an image wiht name and tag from a Dockerfile.


## <span style="color:green">Docker image Management</span>

### Rename

- **docker tag image_name_or_id new_image_name :** Rename an image.

### Remove
- **docker rmi id_or_name_of_image :** Remove an image by its ID or name.

- **docker rmi -f id_or_name_of_image :** Forcefully remove an image by its ID or name.

## <span style="color:green">Dockerfile</span>

**Commands to create a Dockerfile :**

- **FROM :** Specifies the base image for the container.
- **WORKDIR :** Sets the working directory for any RUN, CMD, ENTRYPOINT, COPY and ADD instructions that follow it in the Dockerfile.
- **COPY :** Copies new files or directories from the host and adds them to the container.
- **RUN :** Executes any commands in a new layer on top of the current image and commit the results.
- **EXPOSE :** Exposes a port to the host.
- **CMD :** Specifies the default command that will be executed when running the container.


## <span style="color:green">Docker</span>

### Docker Commands

- **docker help command :** Get help to a specific command.

- **docker version :** Show the Docker version information.

- **docker info :** Show system-wide information.

### Useful

- **docker system prune :** Remove all unused images, containers, networks, and build cache.

- **docker stats :** Display a live stream of container(s) resource usage statistics.

### Authentication

- **docker login :** Login to Docker Hub to authenticate your image push and pull.

- **docker logout :** Logout from Docker Hub.

### Images

- **docker push username/image_name :** Push an image to Docker Hub. <span style="color:yellow">IMPORTANT: The image need have same name of repository on Docker Hub</span>.

- **docker push username/image_name:tag :** Push a new version of image to Docker Hub.

- **docker pull image_name :** Download an image from Docker Hub.

- **docker pull image_name:tag_name :** Download an image from Docker Hub with a specific tag.