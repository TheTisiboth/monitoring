# Monitoring Stack

Uptime Kuma instance for service monitoring.

## Deploy with Dokploy

1. In Dokploy, create new Docker Compose project
2. Point to this repo
3. Dokploy will use `docker-compose.yml`
4. Access at `http://<raspberry-pi-ip>:3005`

## Restore data from backup

```bash
# Stop container
docker-compose down

# Extract backup
mkdir -p data
tar -xzf uptime-kuma-backup.tar.gz -C ./data

# Start container
docker-compose up -d
```

## Fresh install

First access creates admin account at `http://<ip>:3005`
