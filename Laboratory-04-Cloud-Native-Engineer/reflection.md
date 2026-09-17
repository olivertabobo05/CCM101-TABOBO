# Mission 4 Reflection

This laboratory activity helped me understand how containerization can simplify the deployment of applications compared with traditional Virtual Machines. A Docker container can be started much faster because it does not need to install and boot an entire operating system. A VM normally requires a guest operating system and its associated resources, while a container shares the host operating system. This makes containers lightweight and useful for quickly deploying applications such as web servers.

The port mapping `-p 8080:80` is necessary because the Nginx web server is running inside the container on port 80, while port 8080 is used on the host to access the application. The mapping connects the host's port 8080 to the container's port 80. Without this mapping, accessing the Nginx service through the host's port 8080 would not provide the intended connection to the web server.

When the `docker rm` command is used, the specified container is removed from Docker after it has been stopped. The container itself and its writable container filesystem are removed. This shows why important application data should not depend only on a container's temporary writable layer when that data needs to survive the container's removal.

Containerization also changes how software developers and IT operations teams can work together. Developers can package an application with the environment and dependencies needed to run it, while operations teams can use the same container image across different environments. This supports a more consistent workflow between development, testing, and deployment and contributes to DevOps practices.

Finally, my GitHub portfolio is evolving from a collection of cloud computing activities into a more organized record of my technical learning. This laboratory adds practical experience with Docker, containers, networking, lifecycle management, and technical documentation. Keeping the files and screenshots organized in the portfolio also gives me evidence of the skills I have practiced throughout the course.
  
