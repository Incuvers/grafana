# Grafana Configuration

Modified: 2021-11

## Source Build
Build the container from source
```bash
docker build -f docker/Dockerfile -t grafana .
...
```
Run the container
```bash
docker run -p "3000:3000" -it grafana
```
