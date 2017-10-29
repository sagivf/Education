## Useful Docker Commands

### Docker Machine
- `docker-machine start` - Start VM
- `docker-machine stop` - Stop VM
- `docker-machine env` - Display Docker client setup commands

### Docker Client
- `docker <command> --help` - Get help on a specific command
- `docker pull <Name of Image>` - Pull image from Docker Hub
- `docker images` - Show all images
- `docker rmi <ImageID>` - Remove specific images
- `docker rmi $(docker images | grep "^<none>" | awk "{print $3}")` - Remove untagged images - <none>
- `docker ps -a` - Show all containers
- `docker rm <ContainerID>` -Remove specific container
- `docker rm $(docker ps -a -q)` Remove all containers
- `docker ps --format 'table {{.Names}}\t{{.Image}}\t{{.Status}}'` - Formatted list of containers
- `docker run -d --name <Container Name> -p <External Port>:<Container Port> <Your Image>` - Run a container
- `docker build -f <Your Dockerfile> -t <Tag Name> .` - Build an image from a Dockerfile
- `docker login` - Login using your Docker credentials
- `docker push <Your Image Name>` - Push an image to Docker hub
- `docker attach [OPTIONS] CONTAINER` - Login to container
2) run - `docker-compose up --scale consumer=3 --scale ui=1 --scale publisher=1`
3) Locate rjq-ui IP - `docker inspect rjqui_ui_1 | grep IPAddress`(:3000) 

### Docker Compose
- `docker-compose build` - Build images based on docker-compose 
- `docker-compose up -d` - Start in daemon mode
- `docker-compose logs` - Show logs from containers
- `docker-compose up` - Start containers based on docker-compose
- `docker-compose stop` - Stop containers
- `docker-compose down` - Stop and remove containers

## Network modes
* Find port - `sudo ip addr show docker0`

* https://stackoverflow.com/a/24326540/1904390
* https://docs.docker.com/engine/userguide/networking/#related-information

## Enviroment variables
* https://docs.docker.com/compose/environment-variables/
* https://docs.docker.com/compose/env-file/

## Resources
* https://build-podcast.com/docker/
* http://paislee.io/the-ultimate-nodejs-development-setup-with-docker/


