# monitoring-stack

Simple monitoring stack demo: Prometheus + Grafana + Alertmanager + Node Exporter using Docker Compose.

## Components
- Prometheus (9090)
- Grafana (3000)
- Alertmanager (9093)
- Node exporter (9100 host)

## Quick start (local)

1. Clone repo:
```bash
git clone <repo-url>
cd monitoring-stack


2. Start the stack:

docker-compose up -d

Start the stack:

docker-compose up -d


3.Open Grafana: http://localhost:3000

Default: admin / admin123

4.Open Prometheus: http://localhost:9090

5.Check node exporter: http://localhost:9100/metrics

6.Import dashboards:

We provision an example dashboard automatically at startup located at /var/lib/grafana/dashboards/simple-node-dashboard.json.

If it doesn't appear, in Grafana go to Dashboards → Manage → Import JSON and paste grafana/dashboards/simple-node-dashboard.json.

7.Alerts:

Alerts will be evaluated by Prometheus and sent to Alertmanager. Alertmanager is at http://localhost:9093

Current alertmanager config is a simple console/webhook placeholder. Replace with Slack/Email config for production.
