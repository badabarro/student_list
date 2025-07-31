# student-list – POC d'infrastructure Dockerisée

**Auteur :** Badaoudou BARRO  
**Contexte du projet :** Examen pratique – Infrastructure as Code avec Docker  
**Entreprise :** POZOS – Département Innovation  

---

## Présentation du projet

Ce projet est un **proof of concept (POC)** visant à **containeriser une application existante** utilisée par POZOS pour afficher la liste des étudiants avec leur âge. L'application était initialement déployée sur un serveur monolithique sans aucune scalabilité ni automatisation.

L’objectif est d’**améliorer le déploiement**, la **scalabilité** et **l’automatisation** grâce à **Docker**, **Docker Compose** et les **bonnes pratiques DevOps**.

---

## Architecture de l'application

L'application est composée de **deux modules** :

1. **API – Flask (Python)**  
   - Fournit une API REST sécurisée par authentification HTTP Basic  
   - Sert les données étudiants à partir d’un fichier JSON  
   - Exposée sur le port **5000**

2. **Site Web – PHP (Apache)**  
   - Interface utilisateur simple permettant de récupérer les données de l’API  
   - Se connecte à l’API avec identifiants  
   - Exposé sur le port **8080**

---

## Arborescence du projet
student_list/
├── student_api/
│ ├── Dockerfile
│ ├── requirements.txt
│ ├── student_age.json
│ └── student_age.py
├── website/
│ └── index.php
├── docker-compose.yml
├── Vagrantfile
├── install-docker.sh
└── README.md
