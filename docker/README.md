# Docker Notes

## Basics commands

- docker run nginx
  - Download the image if wasn't.

- docker ps
  - list all running containers.

- docker ps -a
  - list all containers running or not.

- docker stop *container name/id*

- docker rm *container name/id*
  - If returns the container name we're good.

- Remove all or Stop all
  - docker rm/stop $(docker ps -a -q)
  - *-a* = all.
  - *-q* = Only display container IDs.

- docker images
  - list all images downloaded.

- docker rmi *image_name*
  - Remove image.

- docker pull *image_name*
  - Download the image

- docker exec *container_name* cat /etc/hosts

## Run - attach and detach

### Attach

  - docker run kodekloud/simple-webapp

### Detach

  - docker run -d kodekloud/simple-webapp

### Attach a detach container
  - docker attach *container_id*

### Run - tag

- docker run redis (without tag = latest version)

- docker run redis:4.0

###  Run - stdin

- docker run kodekloud/simple-prompt-docker

- docker run *-i* kodekloud/simple-prompt-docker

- docker run *-it* koedekloud/simple-prompt-docker

### Run - port mapping

- docker run *-p* **80:5000** kodekloud/simple-webapp

### Run - volume mapping

- docker run -v /opt/datadir:/var/lib/mysql mysql

## Inspect Container

- docker inspect *container_name*

## Container logs

- docker logs *container name*

## Making your own image

- docker build Dockerfile -t matheus/my-custom-app