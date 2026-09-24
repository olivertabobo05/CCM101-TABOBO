# MinIO Deployment

## Docker Command Used

The following Docker command was used to deploy the MinIO server:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
quay.io/minio/minio server /data --console-address ":9001"
```

## Web Console Port

The MinIO Web Console was accessed through port:

**9001**

Port `9000` is used for the MinIO API, while port `9001` is used for the Web Console.

## Bucket Created

The bucket created for this activity is:

**`client-photos`**

A test object named `sample.txt` was uploaded to this bucket.

## Environment Variables

The `-e` flags in the Docker command define environment variables inside the MinIO container.

```bash
-e "MINIO_ROOT_USER=cloudadmin"
-e "MINIO_ROOT_PASSWORD=CloudNova2026!"
```

- `MINIO_ROOT_USER` sets the MinIO root username to `cloudadmin`.
- `MINIO_ROOT_PASSWORD` sets the MinIO root password to `CloudNova2026!`.

These credentials were used to log in to the MinIO Web Console.

## Deployment Verification

The MinIO container was verified using:

```bash
docker ps
```

The container appeared as `minio-server` and was running successfully.

## Evidence

The required screenshots are stored in the `screenshots/` folder:

- `minio-deployed.png` – terminal showing the MinIO container running.
- `minio-bucket-upload.png` – MinIO Web Console showing the `client-photos` bucket and uploaded `sample.txt`.
