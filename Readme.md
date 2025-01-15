# SingleStack

A comprehensive Docker Compose solution for rapid deployment of middleware and database services.

## Supported Services

- Nginx (Reverse Proxy)
- Minio (Object Storage)
- Nacos (Service Discovery)
- Redis (Cache)
- RabbitMQ (Message Queue)
- PostgreSQL (Database)
- Elasticsearch (Search Engine)
- Geoserver (GIS)

## Quick Start

```bash
chmod +x load-images
./load-images

chmod +x ./scripts/unzip-plugins
./scripts/unzip-plugins

chmod +x ./scripts/init-env
./scripts/init-env

docker-compose up -d
```



