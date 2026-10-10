# Two-Tier Architecture

## Introduction

A two-tier architecture is an application structure that separates a system into two main parts: the web/application tier and the database tier. In this mission, Nextcloud serves as the web application, while MariaDB stores the application's database information. Docker Compose connects these two services so they can work together.

## The Web/Application Tier

The web/application tier handles the user interface and processes requests from users. In this deployment, Nextcloud runs inside a Docker container and provides the interface for a private cloud storage system. Users can access the Nextcloud web interface through a web browser using port 8080.

## The Database Tier

The database tier stores persistent information required by the application. MariaDB is used in this project to store Nextcloud database information, including user account information and file metadata. The database runs in a separate container and is accessed by the Nextcloud application through the service name `database`.

## Why Separate Them?

Separating the web application and database into different containers makes the system easier to manage, maintain, and troubleshoot. Each service can be configured, updated, or restarted independently without placing both components inside one container. This separation also makes it easier to scale services and organize the application infrastructure.
