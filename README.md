# Docker Notes
## Introduction
* Containerisation software. The whole idea of Docker is for developers to easily develop applications, ship them into containers which can then be deployed anywhere.
* Docker enables developers to easily pack, ship, and run any application as a lightweight, portable, self-sufficient container, which can run virtually anywhere.
* [use cases](https://www.airpair.com/docker/posts/8-proven-real-world-ways-to-use-docker)
* Containers are completely isolated environments

### Advantages
* Containers use shared operating systems. This means they are much more efficient than hypervisors in system resource terms. Instead of virtualizing hardware, containers rest on top of a single Linux instance. This means you can "leave behind the useless 99.9 percent VM junk, leaving you with a small, neat capsule containing your application

## Definitions
### images
* An image is a combination of a file system and parameters.
* The run command is used to mention that we want to create an instance of an image, which is then called a container.

### containers
* a container is a running instance of an image.

### dockerfile
* Docker also gives you the capability to create your own Docker images, and it can be done with the help of Docker Files. A Docker File is a simple text file with instructions on how to build your images.

* docker image is created using 'Docker build' command on Dockerfile.

## Commands
### containers
* docker run [image]
	* run container of image
	* **creates a new container** every time
* docker ps
    * dislays all running instances
* docker ps  -a
    * displays all containers on pc
* docker rm [container id]
    * remove container
* docker stop [container id]
	* stop container
* docker start [container id]
	* start an already created (stopped) container
### images
* docker images
    * display images on pc
* docker pull [image name]:[version number]
    * pulls a docker image from docker hub
* docker rmi [image id]
    * remove docker image

### misc
* docker pull [docker image]
* docker build -t(tag) [tag name] .(current directory)
* docker run --name[container name] -d(detach) -p(port mapping) [host port]:[container port] -v(volume mapping) [host dir]:[container dir] [image name]

* docker exec
    * can execute a command in a running container
    * docker exec -ti_-it [container] /bin_sh

* docker attach [docker id]
    * attach to a running container

* docker rm $(docker ps -a -q)
    * remove all containers
* docker rmi $(docker images -q)
    * remove all images

* docker system prune -a
* https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes
