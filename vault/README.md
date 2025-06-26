# Déploiement de HashiCorp Vault

Utiliser Helm :
```bash
helm repo add hashicorp https://helm.releases.hashicorp.com
helm install vault hashicorp/vault --namespace vault --create-namespace
```

Configurer les policies, rotation automatique et l'injection de secrets dans les pods.
