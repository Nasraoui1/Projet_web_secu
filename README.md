# Projet CI/CD : Calculatrice Python avec GitHub Actions

Ce projet contient une application Python simple (une calculatrice) ainsi qu'un pipeline d'intégration continue et de déploiement continu (CI/CD) complet mis en place avec **GitHub Actions**.

L'objectif de ce projet est de démontrer les bonnes pratiques de CI/CD, incluant des tests multi-versions, de l'analyse de vulnérabilités, et la création et publication automatisée d'une image Docker sur le Docker Hub.

## L'Application

L'application est le code du répertoire fourni qui est développé en Python et se trouve dans le dossier `calculator/`.

## Le Pipeline CI/CD

Le pipeline est défini dans le fichier `.github/workflows/cicd.yml`. Il se déclenche automatiquement à chaque `push` sur les branches `main` ou `master`, ou manuellement via un `workflow_dispatch`.

Il est structuré en trois (3) étapes principales (Jobs) :

### 1. Phase de Test (`test`)
Ce job s'assure de la fiabilité et de la qualité du code.

### 2. Analyse de Vulnérabilité (`trivy-scan`)
Ce job gère l'aspect de la sécurité du code source.

### 3. Construction et Déploiement (`build-and-push`)
Ce job assemble l'application et la publie en tant que conteneur Docker.

