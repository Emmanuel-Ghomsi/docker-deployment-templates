# 🚀 Docker Deployment Templates - PostgreSQL, MongoDB & Keycloak  

![Docker](https://img.shields.io/badge/Docker-Supported-blue?logo=docker)
![Status](https://img.shields.io/badge/Status-Production%20Ready-green)
![License](https://img.shields.io/github/license/emmanuel-ghomsi/docker-deployment-templates)

📌 Ce repository contient **trois templates Docker Compose** permettant de déployer rapidement des services essentiels sur un serveur **VPS ou local** :

- 🛢️ **PostgreSQL + PGAdmin**
- 📦 **MongoDB + Mongo Express**
- 🔐 **Keycloak - Gestion des identités et authentification**

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
┣ 📜 .env.example # Variables d’environnement
┣ 📜 LICENSE # Licence MIT
┣ 📜 README.md # Documentation
┣ 📜 docker-compose.keycloak.yml # Déploiement de Keycloak
┣ 📜 docker-compose.postgres.yml # Déploiement de PostgreSQL + PGAdmin
┣ 📜 docker-compose.mongo.yml # Déploiement de MongoDB + Mongo Express
```

---

## 🚀 **Instructions d'Utilisation**
### 1️⃣ **Cloner le repository**
```bash
git clone https://github.com/emmanuel-ghomsi/docker-deployment-templates.git
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