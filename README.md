# Projet Kubernetes - Cruise (WordPress + MySQL + Traefik)

## 🌐 Objectif
Déployer un service WordPress connecté à une base MySQL, exposé via Traefik sur un cluster K3S, avec HTTPS automatique via Let's Encrypt.

## 📐 Architecture
```
[ Client ] ---> Traefik Ingress ---> WordPress Pod ---> MySQL Pod
                             |--> Hugo Docs (HTTPS + Auth)
                             |--> Observabilité (Prometheus, Grafana, Loki)
```

## 📦 Déploiement rapide

```bash
kubectl apply -f mysql/namespace.yaml
kubectl apply -f mysql/
kubectl apply -f wordpress/
```

## 🔐 Sécurité
- Secrets stockés dans `Secret` K8s
- Vault disponible pour gestion dynamique (voir dossier `vault/`)

## 📊 Observabilité
- Prometheus + Grafana + Loki + Promtail
- Dashboards : CPU, RAM, HTTP codes, Logs filtrables

## 📚 Documentation
Accessible via Hugo (HTTPS + Auth) : `https://docs.etna.student`

## 📁 Dossiers
- `mysql/` : base de données
- `wordpress/` : service web
- `traefik/` : ConfigMap TLS Let's Encrypt
- `vault/` : déploiement HashiCorp Vault (Helm)
- `observabilite/` : Prometheus, Grafana, Loki, Promtail
- `hugo-docs/` : documentation du projet
