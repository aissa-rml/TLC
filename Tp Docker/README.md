# Compte-rendu TP Docker

## Objectifs

Explorer Docker pour le déploiement d'applications, l'utilisation d'un serveur web en reverse proxy avec Nginx, et la dockerisation d'une application existante.

## Étapes et Observations

### Installation de Docker

- Installation réussie, vérifiée avec `docker run hello-world`.

### Test avec Ubuntu

- Exécution d'un conteneur Ubuntu : différences notées dans les interfaces réseau entre le conteneur et la machine hôte.

### Mise en Place d'un Reverse Proxy

- Utilisation de l'image `jwilder/nginx-proxy` pour déployer un reverse proxy.
- Le proxy simplifie la gestion du trafic réseau vers les conteneurs dynamiques.

### Utilisation de Docker Compose

- Automatisation du déploiement des services Nginx et du load balancer via Docker Compose.
- Facilite considérablement la mise en place et la gestion des conteneurs.

### Dockerisation d'une Application

- Dockerisation réussie d'une application Web de détection de visage.
- L'application est déployée efficacement à l'aide de Docker, démontrant sa flexibilité.

## Conclusion

Ce TP a permis une compréhension approfondie de Docker, démontrant son potentiel pour simplifier le déploiement d'applications et la gestion de l'infrastructure.
