# MinIO Deployment

## Overview

MinIO is used in this laboratory as an S3-compatible object storage server. Docker makes it possible to download and run the MinIO server as a container.

## 1. Deploy the MinIO Server

The following Docker command was used to deploy MinIO:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
minio/minio server /data --console-address ":9001"
```

## 2. Explanation of the Docker Command

* `docker run -d` – creates and starts the container in detached mode.
* `-p 9000:9000` – maps port 9000 of the container to port 9000 of the environment. This is used for the MinIO API.
* `-p 9001:9001` – maps port 9001 of the container to port 9001 of the environment. This is used for the MinIO Web Console.
* `--name minio-server` – gives the Docker container the name `minio-server`.
* `minio/minio` – specifies the MinIO Docker image.
* `server /data` – starts the MinIO server and uses `/data` as its storage location.
* `--console-address ":9001"` – configures the MinIO Web Console to use port 9001.

## 3. Environment Variables

The `-e` flags define environment variables inside the Docker container.

```bash
-e "MINIO_ROOT_USER=cloudadmin"
-e "MINIO_ROOT_PASSWORD=CloudNova2026!"
```

The first environment variable sets the MinIO root username to `cloudadmin`.

The second environment variable sets the MinIO root password to `CloudNova2026!`.

These credentials are used to log in to the MinIO Web Console.

> **Security Note:** These credentials are the ones specified by the laboratory activity. In a real production environment, passwords should be managed securely and should not be publicly exposed or committed to a public repository.

## 4. Verify the Container

After running the Docker command, the container can be checked using:

```bash
docker ps
```

The output should show the `minio-server` container running.

## 5. Access the MinIO Web Console

The MinIO Web Console uses:

```text
Port: 9001
```

In the KillerCoda Playground, open the **Traffic / Ports** or **Custom Ports** section and enter port `9001`.

Click **Access** to open the MinIO Web Console.

Log in using:

```text
Username: cloudadmin
Password: CloudNova2026!
```

## 6. Create the Bucket

After logging into the MinIO Web Console:

1. Navigate to **Buckets**.
2. Click **Create Bucket**.
3. Enter the bucket name:

```text
client-photos
```

4. Save the bucket.

## 7. Upload a Test File

Open the `client-photos` bucket.

Click the **Upload** button and select a safe sample image or text file from the computer.

The uploaded file should then appear inside the `client-photos` bucket.

## 8. Screenshots

The following screenshots are required as evidence:

### MinIO Deployment

Save a screenshot showing the terminal and running container as:

```text
screenshots/minio-deployed.png
```

### Bucket and Uploaded File

Save a screenshot showing the MinIO Web Console, the `client-photos` bucket, and the uploaded file as:

```text
screenshots/minio-bucket-upload.png
```

## 9. Configuration Summary

| Item                  | Configuration             |
| --------------------- | ------------------------- |
| Container Name        | `minio-server`            |
| API Port              | `9000`                    |
| Web Console Port      | `9001`                    |
| Root Username         | `cloudadmin`              |
| Root Password         | `CloudNova2026!`          |
| Bucket Name           | `client-photos`           |
| Deployment Screenshot | `minio-deployed.png`      |
| Bucket Screenshot     | `minio-bucket-upload.png` |
