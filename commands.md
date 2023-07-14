# Docker Commands

## Docker Run

- **docker run image_name:** Run an image in Docker.

- **docker run -it image_name:** Run an image in Docker and keep an interactive session in the terminal. Type `exit` to exit the container.

- **docker run -d image_name:** Run an image in Docker in the background.

- **docker run -p 8080:80 image_name:** Run an image in Docker and map port 8080 of the container to port 80 of the host.

- **docker run -p 8080:80 -d image_name:** Run an image in Docker, map port 8080 of the container to port 80 of the host, and run it in the background.

- **docker run --name my_container image_name:** Run an image in Docker and set a name for the container.

## Container Management

- **docker stop id_or_name_of_container:** Stop a container by its ID or name.

- **docker start id_or_name_of_container:** Start a container by its ID or name.

- **docker ps:** List all running containers.

- **docker container ls:** An alternative way to list all running containers.

- **docker ps -a:** List all running and stopped containers.

- **docker container ls -a:** An alternative way to list all running and stopped containers.

- **docker logs id_or_name:** Show all logs of a container.

- **docker rm id_or_name_of_container:** Remove a container by its ID or name.

- **docker rm -f id_or_name_of_container:** Forcefully remove a container by its ID or name.