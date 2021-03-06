# Incuvers Grafana Image
[![deploy](https://github.com/Incuvers/grafana/actions/workflows/deploy.yaml/badge.svg)](https://github.com/Incuvers/grafana/actions/workflows/deploy.yaml)

![img](docs/img/Incuvers-black.png)

Modified: 2021-11

## Usage

`Incuvers/grafana` extends the grafana server image including custom initialization declarations and plugins. From github container registry:
```bash
docker pull ghcr.io/incuvers/grafana:arm64
```

### Compose File
Or integrate the container in any compose stack:
```yaml
networks:
  monitor:
    driver: bridge

volumes:
  grafana_data: {}

services:
  grafana:
    image: ghcr.io/incuvers/grafana:arm64
    container_name: grafana
    restart: unless-stopped
    volumes:
      - grafana_data:/var/lib/grafana
    ports:
      - "3000:3000"
    networks:
      - monitor
    labels:
      org.label-schema.group: "monitoring"
```
