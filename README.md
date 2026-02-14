# Projet Intégré – Systèmes et Réseaux

## 📌 Contexte
Ce projet est réalisé dans le cadre du **module Projet d’Intégration Système et Réseaux** à ESPRIT.  
Il vise la conception et le déploiement d’une **infrastructure réseau d’entreprise multiservice**, simulée sous **GNS3** et intégrant des services systèmes déployés sur des machines virtuelles.

Le projet est mené en **travail de groupe**, chaque membre étant responsable d’un rôle ou d’un département spécifique.

---

## 🎯 Objectifs du projet
- Concevoir et déployer une **topologie réseau distribuée** sous GNS3  
- Mettre en place une **architecture réseau hiérarchisée et segmentée**
- Implémenter le **routage statique et dynamique**
- Déployer et administrer des **services systèmes critiques**
- Assurer la **sécurité, la supervision et la documentation** de l’infrastructure

---

## 🏗️ Architecture réseau
- Backbone réseau interconnectant plusieurs départements
- Segmentation du réseau via **VLSM**
- Plan d’adressage IPv4 structuré
- Routage :
  - Routage statique
  - Routage dynamique (OSPF)
- Accès Internet simulé avec **NAT / PAT**

---

## 🔧 Services implémentés

### 1️⃣ Service NFS (Partage de fichiers)
- Installation et configuration d’un serveur NFS
- Gestion des utilisateurs et des droits d’accès
- Mise en place des permissions (groupes, SGID, Sticky Bit)
- Deux clients capables de partager les mêmes ressources
- Automatisation via **scripts Shell**

### 2️⃣ Supervision (Monitoring)
- Déploiement de **Prometheus / Grafana**
- Collecte des métriques serveur et client
- Mise en place d’alertes
- Installation de Node Exporter avec fichiers unitaires
- Automatisation via scripts Shell

### 3️⃣ Service Web
- Installation d’un serveur Web Apache
- Création d’une base de données associée
- Gestion des droits utilisateurs
- Accès client à une page Web hébergée sur le serveur
- Automatisation de l’installation et de la configuration

### 4️⃣ Base de Données
- Installation d’un SGBD MySQL
- Création d’une base de données et des utilisateurs
- Gestion des privilèges (Administrateur / Utilisateur)
- Accès client à la base de données

---

## 🔐 Sécurité et intégration
- Routage dynamique sécurisé
- Intégration des différentes zones réseau
- Mise en place de mécanismes de sécurité (ACL)
- Vérification de l’accessibilité des services entre zones distinctes

---

## 🧪 Validation et tests
- Tests de connectivité intra-VLAN et inter-VLAN
- Vérification des routes et interfaces réseau
- Tests des services (NFS, Web, Base de données, Monitoring)
- Justification de la faisabilité à l’aide de **captures d’écran**

Les résultats des tests sont disponibles dans le dossier `captures/`.

---

## 📂 Structure du dépôt
```text
Projet-PI-Systeme-Reseau/
├── README.md
├── scripts/
│   └── Annexe_Scripts_NFS.pdf
├── captures/
│   ├── reseau/
│   └── nfs_vm/
├── configuration/
│   └── projet_pi_reseau.gns3project
