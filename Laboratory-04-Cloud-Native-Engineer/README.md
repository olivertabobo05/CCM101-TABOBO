# Laboratory 04 – Cloud-Native Engineer


## Mission Overview

This laboratory activity focuses on understanding the shift from traditional Virtual Machines (VMs) to containerization. As a Cloud-Native Engineer, the goal is to understand how containers provide lightweight, portable, and fast environments for running applications.

In this activity, Docker is used through the KillerCoda Playground to deploy an Nginx web server. The activity includes comparing Virtual Machines and Containers, executing fundamental Docker commands, deploying an Nginx container, managing its lifecycle, and documenting the procedures using Markdown.

## Objectives

At the end of this laboratory activity, I should be able to:

* Differentiate between traditional Virtual Machines (VMs) and Containers.
* Access a Docker-enabled cloud environment using KillerCoda.
* Execute fundamental Docker CLI commands.
* Pull, run, manage, and terminate a containerized Nginx application.
* Create professional technical documentation of container operations using Markdown.
* Continue developing an organized GitHub Cloud Computing Portfolio.

## Docker Commands Executed

### Checkpoint 3 – Verify Docker

```bash
docker --version
```

This command displays the installed Docker version and verifies that Docker is available in the environment.

```bash
docker info
```

This command displays information about the current Docker environment and helps verify that the Docker service is operational.

### Checkpoint 4 – Deploy Nginx

```bash
docker pull nginx
```

This command downloads the official Nginx image from Docker Hub.

```bash
docker run -d -p 8080:80 --name nginx-server nginx
```

This command creates and starts an Nginx container in detached mode and maps port 8080 on the host to port 80 inside the container.

```bash
curl http://localhost:8080
```

This command sends an HTTP request to the Nginx web server running inside the container and verifies that the server is responding.

### Checkpoint 5 – Container Lifecycle

```bash
docker ps
```

This command lists the currently running Docker containers.

```bash
docker stop nginx-server
```

This command stops the running Nginx container.

```bash
docker ps -a
```

This command lists all containers, including containers that have been stopped.

```bash
docker rm nginx-server
```

This command removes the stopped Nginx container completely.

## Skills Learned

Through this laboratory activity, I learned how containerization differs from traditional virtualization and why containers are useful in cloud-native environments. I also practiced basic Docker CLI operations, including pulling images, running containers, checking container status, stopping containers, and removing containers.

I learned how port mapping allows a service inside a container to be accessed through a port on the host system. I also gained experience documenting technical procedures using Markdown and organizing evidence as part of a GitHub Cloud Computing Portfolio.

## Challenges Encountered

One challenge was becoming familiar with Docker commands and understanding the difference between a Docker image and a running container. Another challenge was understanding how port mapping connects the host machine to a service running inside the container.

The KillerCoda environment also required careful execution of commands in the correct order. Checking the Docker environment before deploying Nginx helped ensure that the necessary tools were available. Taking screenshots at the required checkpoints also required attention to the laboratory instructions.

Overall, the activity helped me become more comfortable with the Docker command line and with the basic workflow of deploying and managing a containerized application.

