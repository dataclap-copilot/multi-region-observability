# 🌐 Multi-Region Observability Stack

A production-grade observability stack that supports multi-region Kubernetes microservices applications. Includes distributed tracing, centralized logging, monitoring, alerting, and dashboards.

---

## 📦 Stack Components

| Layer         | Tools Used                                |
|---------------|-------------------------------------------|
| Tracing       | Jaeger, OpenTelemetry                     |
| Logging       | Fluentd, Elasticsearch, Kibana            |
| Monitoring    | Prometheus, Alertmanager                  |
| Dashboards    | Grafana                                   |
| Orchestration | Kubernetes / Docker Compose               |

---

## 📁 Folder Structure

```bash
multi-region-observability/
├── docker-compose.yml
├── tracing/
├── logging/
├── monitoring/
├── dashboards/
├── multi-region-setup/
└── README.md
```

---

## 🚀 Quick Start

### 🐳 Run Locally via Docker Compose

> Useful for local testing without Kubernetes

```bash
cd multi-region-observability
docker-compose up -d

```
---

## ☸️  Deploy on Kubernetes
Apply all components:
```bash
kubectl apply -f tracing/
kubectl apply -f logging/
kubectl apply -f monitoring/
kubectl apply -f dashboards/

```
Multi-region support:
```bash
kubectl apply -f multi-region-setup/region-us.yaml
kubectl apply -f multi-region-setup/region-eu.yaml
kubectl apply -f multi-region-setup/global-gateway.yaml
```
---
## 🔧 Customize
Ports to expose
You can change ports in:

docker-compose.yml

K8s deployment.yaml files

Add Services to Monitor
Update:

prometheus-config.yaml

fluentd-config.yaml
---
## 📤 Exporting Logs, Metrics, Traces
Each service supports:

HTTP and gRPC OTLP (OpenTelemetry)

Fluentd TCP/UDP log forwarding

Prometheus scraping targets
---
## 📌 Notes
Tested with Kubernetes v1.27+ and Docker Engine 24+

Can integrate with tools like Loki, Tempo, Thanos

Supports multi-cluster extensions via gateways


