# Mission 6: The Cloud Deployment Engineer

## Mission Overview

This laboratory activity focuses on deploying a multi-tier cloud application using Docker Compose. The project uses Nextcloud as the web application and MariaDB as the database. Both containers are configured through a `docker-compose.yml` file and deployed together using a single command.

## Objectives

- Understand two-tier application architecture.
- Identify the roles of the web/application tier and database tier.
- Create a Docker Compose configuration file using YAML.
- Deploy Nextcloud and MariaDB using Docker Compose.
- Access the Nextcloud web interface through port 8080.
- Document Infrastructure as Code (IaC) using Markdown.
- Practice deploying and removing a multi-container application.

## Commands Executed

```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

- Docker and Docker Compose
- Multi-tier application deployment
- YAML configuration
- Linux command-line operations
- Container networking
- Environment variables
- Infrastructure as Code (IaC)
- Technical documentation using Markdown

