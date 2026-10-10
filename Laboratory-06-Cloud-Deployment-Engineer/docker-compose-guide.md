# Docker Compose Guide

## Overview

Docker Compose is a tool used to define and manage applications that consist of multiple containers. It uses a YAML configuration file named `docker-compose.yml` to describe the services and their settings.

## Docker Compose Configuration

The following configuration defines the Nextcloud application and MariaDB database.

```yaml
services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - "8080:80"
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

## What Does the `services:` Block Do?

The `services:` block defines the containers that make up the application. In this configuration, the `database` service runs MariaDB, while the `app` service runs Nextcloud. Docker Compose manages the two services together.

## How Does Nextcloud Find the Database?

The environment variable `MYSQL_HOST=database` identifies the database service by its Compose service name. Docker Compose provides service discovery on its application network, allowing Nextcloud to connect to the MariaDB container using the hostname `database`.

## What Is the Difference Between `docker run` and `docker-compose up -d`?

The `docker run` command starts an individual container using options provided directly in the command. In contrast, `docker-compose up -d` reads the Compose configuration and starts the services defined in the file in detached mode, allowing multiple related containers to be managed together.
