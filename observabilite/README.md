# Observabilité

Inclut :
- Prometheus (monitoring)
- Grafana (visualisation)
- Loki (logs)
- Promtail (collecte de logs)

Déploiement recommandé via Helm :
```bash
helm repo add grafana https://grafana.github.io/helm-charts
helm install monitoring grafana/k8s-monitoring --namespace observability --create-namespace
```
