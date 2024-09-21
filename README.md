# phpMyAdmin Service with Docker

This guide will help you set up and run the phpMyAdmin service using Docker Compose. Follow the steps below to get started.

## Prerequisites

- Docker installed on your machine
- Docker Compose installed on your machine
- GitHub Desktop installed on your machine

## Step-by-Step Guide

### 1. Clone the Repository

1. Open GitHub Desktop.
2. Click on `File` > `Clone repository`.
3. Enter the repository URL or choose the repository from your GitHub account.
4. Select the local path where you want to clone the repository.
5. Click `Clone`.

### 2. Navigate to the Project Directory

Open a terminal and navigate to the project directory:

```sh
cd /D:/Project/Personal/Docker/phpmyadmin-service
```

### 3. Run Docker Compose

Ensure you have a `docker-compose.yaml` file in the project directory. Then, run the following command to start the phpMyAdmin service:

```sh
docker-compose up -d
```

This command will build and start the containers in detached mode.

### 4. Access phpMyAdmin

Once the containers are up and running, you can access phpMyAdmin by navigating to `http://localhost:8080` in your web browser.

## Stopping the Service

To stop the running containers, use the following command:

```sh
docker-compose down
```

This will stop and remove the containers defined in the `docker-compose.yaml` file.

## Additional Information

For more details on Docker and Docker Compose, refer to the official documentation:

- [Docker Documentation](https://docs.docker.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
