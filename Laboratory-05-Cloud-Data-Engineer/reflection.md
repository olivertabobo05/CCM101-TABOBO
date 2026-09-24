# Mission Reflection

Object storage is better suited for storing millions of photos because photos are unstructured data and can be stored as individual objects. A photo-sharing application may receive a very large number of uploads, so object storage provides a storage model designed for large collections of unstructured data. It also separates the stored photos from the web-server container. This is important because containers are ephemeral, meaning that their contents are temporary.

Docker made it easier to deploy the MinIO storage server because the service could be downloaded and started from a Docker image using a single command. Instead of manually installing and configuring every component, the Docker command created the container, mapped the required ports, configured the login credentials through environment variables, and started the MinIO service. This made the deployment process faster and more repeatable.

A bucket in cloud storage is a logical storage container used to organize objects. In this laboratory, the bucket named `client-photos` provides a location where the application's uploaded images and test files can be stored.

Large enterprise companies need to protect their object storage data from physical server failures. They can use redundant storage and maintain additional copies of data so that a hardware failure does not result in the permanent loss of the only copy. The exact method used depends on the storage system and its architecture.

My confidence in navigating the Linux command line is growing because this activity required me to use Docker commands and verify that a container was running. Commands such as `docker run` and `docker ps` are becoming more familiar as I use them in practical cloud computing tasks. This activity also helped me understand how command-line skills can be used to deploy and manage a real cloud storage service.
