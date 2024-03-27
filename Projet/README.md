# Compte-rendu du Projet 

## Objectif du Projet

Le but de ce projet est d'explorer Docker pour le déploiement d'applications, en utilisant un serveur web en reverse proxy avec Nginx, et en dockerisant une application existante.

## Déroulement et Réalisation du Projet

### Tâche 0 : Préparation de l'Environnement

- Création d'une machine virtuelle via le service fourni par l'ISTIC, avec Ubuntu 20 comme image de base.
- Demande faite pour l'accès externe vers les ports 80 et 443, et configuration de l'accès SSH via VPN.

### Tâche 1 : Déploiement et Configuration de l'Application

- Installation d'Ansible sur la machine locale et configuration des Dockerfiles et Docker Compose basés sur les indications fournies.
- Malgré une mise en place initiale réussie, des difficultés sont survenues dues à la gestion des requêtes CORS par le front-end, empêchant une exécution correcte de cette étape.

### Tâche 2 : Configuration du Serveur Web Front-end

- Une tentative a été faite pour configurer le serveur NGINX afin de router correctement les requêtes `/api` vers le service backend approprié.
- **Obstacle** : Cette tâche n'a pas été achevée en raison de multiples problèmes sur ma machine, ce qui a empêché l'exécution réussie de cette partie du projet.

### Tâche 3 : Déploiement Avancé

- En raison des problèmes techniques non résolus rencontrés lors de la tâche 2, le déploiement complet, la configuration du DNS, Letsencrypt pour les certificats SSL, et UFW pour le firewall n'ont pas pu être réalisés.

### Tâche 4 : Documentation et Diagramme de Déploiement

- Cette tâche n'a pas été réalisée dû aux obstacles techniques mentionnés précédemment.

## Conclusion

Ce projet a offert une opportunité d'approfondir les connaissances et les compétences autour de Docker, Nginx, et la gestion des conteneurs pour le déploiement d'applications. Malgré les difficultés techniques qui ont empêché la réalisation complète de toutes les tâches, les premières étapes ont été fructueuses et ont posé les bases pour de futures explorations et améliorations.

## Prochaines Étapes

- Résolution des problèmes techniques pour compléter les tâches 3 et 4.
