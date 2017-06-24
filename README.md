# Docker

I am writing now.

What is Docker?
Docker is a platform to run each application isolated and securely. Internally it achieves it by using kernel containerization feature.

What is Docker Image?
It is necessary to create a container. You can create a container by running a Docker Image.
this is similar when a VM is created by using ISO file. Basically, a image name in Docker is based on [repository name]/[image name]:[tag]

Repository: There is a place to save an image. If the image’s name is not specified, this is an official image, which provides users with a basic image from the Docker Hub.

Image name: This is an image’s role. We cannot omit the name of the image. We must configure name on Docker image.

What is Docker Container?
A Docker Container is what Docker is built on. They encapsulate an application and all of the application libraries and dependencies. When we create the container by using a Docker image which is in suitable applications.

What is the use case for Docker?
Docker is extremely useful in development environments. Especially for testing purposes. You can deploy and re-deploy apps in a blink of an eye.
There are use cases where you can use Docker in production. Imagine you have some Node.js application providing some services on the web. Eventually, if Docker is good or not should be decided on an application basis. For some apps, it can be sufficient, for others not.


Basic command line on Docker
## Create  and start a container
```bash
$ .docker run -i -t --name <container_name> <image> 
```
## Start, stop and restart  a container
```bash
$ docker [start|stop|restart] <container_name> or <container_id>
```
## Show images in docker
```bash
$ docker images
```

## Attach to a running container
```bash
$ docker attach <container_name> or <container_id>
```

## Check containers status
```bash
$ docker ps
```

- CONTAINER ID: This is specified id which allocates automatically. If you want to check the whole id, You can use the option of "inspect" 
