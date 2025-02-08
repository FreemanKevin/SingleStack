# SingleDocker

A comprehensive Docker Compose solution for rapid deployment of middleware and database services.

## Supported Services

- Nginx
- Minio 
- Nacos
- Redis
- RabbitMQ 
- PostgreSQL
- Elasticsearch 
- Geoserver

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



