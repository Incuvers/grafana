FROM grafana/grafana-arm64v8-linux:latest

LABEL version "v1.0.0"
LABEL Christian Sargusingh "https://github.com/cSDes1gn"

USER grafana

# package custom config
ADD grafana/provisioning /etc/grafana/provisioning
ADD grafana/grafana.ini /etc/grafana/grafana.ini
ADD grafana/dashboards /var/lib/grafana/dashboards

ENTRYPOINT [ "/run.sh" ]