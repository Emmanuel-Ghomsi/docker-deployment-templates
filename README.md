# 🚀 Docker Deployment Templates - PostgreSQL, MongoDB, Keycloak, Odoo & Grafana + Prometheus + Loki + Promtail

![Docker](https://img.shields.io/badge/Docker-Supported-blue?logo=docker)
![Status](https://img.shields.io/badge/Status-Production%20Ready-green)
![License](https://img.shields.io/github/license/emmanuel-ghomsi/docker-deployment-templates)

📌 Ce repository contient **plusieurs templates Docker Compose** permettant de déployer rapidement des services essentiels sur un serveur **VPS ou local** :

- 🛢️ **PostgreSQL + PGAdmin**
- 📦 **MongoDB + Mongo Express**
- 🔐 **Keycloak - Gestion des identités et authentification**
- 📊 **Odoo – ERP open-source**
- 📈 **Grafana + Prometheus + Loki + Promtail**

### 🚀 **Pourquoi utiliser ce repo ?**

✅ Déploiement **simplifié** et **rapide**  
✅ Facilité d'utilisation sur **n'importe quel VPS**  
✅ Centralisation des configurations **dans un seul repo**  
✅ **Variables d’environnement** bien structurées via `.env.example`  
✅ **Extensible** pour ajouter d'autres services  

---

## 📂 **Structure du Repository**

```yaml
📦 docker-deployment-templates
┣ 📜 .env.example                   # Variables d’environnement
┣ 📜 LICENSE                        # Licence MIT
┣ 📜 README.md                      # Documentation
┣ 📜 docker-compose.keycloak.yml    # Déploiement de Keycloak
┣ 📜 docker-compose.postgres.yml    # Déploiement de PostgreSQL + PGAdmin
┣ 📜 docker-compose.mongo.yml       # Déploiement de MongoDB + Mongo Express
┣ 📜 docker-compose.odoo.yml        # Déploiement d'Odoo ERP
┣ 📜 docker-compose.monitoring.yml  # Déploiement de Grafana + Prometheus + Loki + Promtail
┣ 📂 config                         # Configuration des services
┃   ┣ 📂 odoo/
┃   ┃   ┣ 📜 odoo.conf
┃   ┃   ┗ 📂 addons/ 
┃   ┗ 📂 loki/
┃   ┃   ┣ 📜 daemon.json            # à placer dans /etc/docker
┃   ┃   ┣ 📜 loki-config.yml
┃   ┃   ┣ 📜 promtail-config.yml
┃   ┗ 📂 prometheus/
┃       ┣ 📜 prometheus.yml
┃       ┗ 📂 file_sd/ 
```

## 🚀 **Instructions d'Utilisation**

### 1️⃣ **Cloner le repository**

```bash
git clone https://github.com/Emmanuel-Ghomsi/docker-deployment-templates.git

cd docker-deployment-templates
```

### 2️⃣ **Configurer les variables d’environnement**

Renomme le fichier .env.example en .env et configure les valeurs nécessaires :
```bash
cp .env.example .env
```

### 3️⃣ **Déployer un service avec Docker Compose**

➡️ Lancer PostgreSQL + PGAdmin :
```bash
docker-compose -f docker-compose.postgres.yml up -d
```

➡️ Lancer MongoDB + Mongo Express :
```bash
docker-compose -f docker-compose.mongo.yml up -d
```

➡️ Lancer Keycloak :
```bash
docker-compose -f docker-compose.keycloak.yml up -d
```

➡️ Lancer Odoo (connecté à PostgreSQL sur shared-network) :
```bash
docker-compose -f docker-compose.odoo.yml up -d
```

➡️ Lancer Grafana + Prometheus + Loki + Promtail :
```bash
docker-compose -f docker-compose.monitoring.yml up -d
```