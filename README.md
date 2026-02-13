# MOV.AI Observability Dashboard Container

This container provides a Grafana-based dashboard for monitoring and visualization of MOV.AI systems. It includes pre-configured dashboards and data sources to help users gain insights into their robotic applications.

## Features

- Grafana-based dashboard for real-time monitoring
- Pre-configured dashboards for common MOV.AI metrics
- Support for multiple data sources (e.g., Loki for logs)
- Easy integration with existing MOV.AI infrastructure
- Multi-platform support (amd64, arm/v7, arm64)


## Usage

To build the MOV.AI Observability Dashboard container, use the following command:

```bash
docker build -t qa/obs-dashboard:latest -f docker/Dockerfile .
```

To run the MOV.AI Observability Dashboard container, use the following command:

```bash
docker run -d \
  --name obs-dashboard \
  -p 3000:3000 \
  qa/obs-dashboard:latest
```
