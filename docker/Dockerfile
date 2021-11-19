FROM grafana/grafana-arm64v8-linux:latest

LABEL version "v1.0.0"
LABEL Christian Sargusingh "https://github.com/cSDes1gn"

ENV GF_SECURITY_ADMIN_USER "admin"
ENV GF_SECURITY_ADMIN_PASSWORD "incuvers"

# package incuvers custom config
ADD grafana/grafana.ini /etc/grafana/grafana.ini

ENTRYPOINT [ "/run.sh" ]