# Main image
FROM grafana/grafana:11.6 AS base

# Labels
LABEL description="MOV.AI Observability Dashboard - Grafana based dashboard for monitoring and visualization" \
      maintainer="devops@mov.ai" \
      org.opencontainers.image.source="https://github.com/MOV-AI/containers-obs-dashboard" \
      org.opencontainers.image.documentation="https://github.com/MOV-AI/containers-obs-dashboard/blob/main/README.md" \
      org.opencontainers.image.vendor="MOV.AI" \
      org.opencontainers.image.title="MOV.AI Observability Dashboard"

# Configuration: ini
COPY files/grafana.ini /etc/grafana/grafana.ini

# Configuration Files: YAML Format
COPY files/dashboards/*.yml /etc/grafana/provisioning/dashboards/
COPY files/datasources/*.yml /etc/grafana/provisioning/datasources/

HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 CMD [ "curl", "-s", "-f", "http://localhost:3000/api/health" ]