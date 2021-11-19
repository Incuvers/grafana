# Incuvers Grafana Image
![img](docs/img/Incuvers-black.png)

[![deploy](https://github.com/Incuvers/grafana/actions/workflows/deploy.yaml/badge.svg)](https://github.com/Incuvers/grafana/actions/workflows/deploy.yaml)

Modified: 2021-11

## Usage

`Incuvers/grafana` extends the grafana server image including custom initialization declarations and plugins. From github container registry:
```bash
docker pull ghcr.io/incuvers/grafana:latest
```

### Compose File
Or integrate the container in any compose stack:
```yaml
services:
  grafana:
    image: ghcr.io/incuvers/grafana:latest
    container_name: grafana
    restart: always
    # user: "1000" # needs to be `id -u` // alternatively chown the grafana/data dir to 472:472
    ports:
      - "3000:3000"
    volumes:
        # define persistant volumes
      - /var/lib/grafana:/var/lib/grafana
      - /etc/grafana/provisioning:/etc/grafana/provisioning 
```
