# Compte-rendu TP Ansible

## Objectif du TP

Ce TP vise à introduire Ansible à travers une mise en application pratique, en observant le déploiement automatisé de configurations sur des machines virtuelles. Ce travail est réalisé dans le cadre du cours TLC au département d'Informatique et d'Électronique de l'Université de Rennes 1.

## Enoncé et Réalisation

### Tâche 0: Préparation de l'Environnement

- **Création des VMs** : Deux machines virtuelles ont été créées via le service [vm.istic.univ-rennes1.fr](https://vm.istic.univ-rennes1.fr/), utilisant `ubuntu22` comme image de base. L'accès SSH sur le port 22 a été vérifié suite à la configuration via VPN.

### Tâche 1: Déploiement d'une Application avec Ansible

- **Installation et Configuration**:
  - Ansible a été installé sur la machine locale avec `apt-get install ansible`.
  - Le repository [demoAnsible](https://github.com/barais/demoAnsible) a été cloné, et le playbook `lamp_ubuntu2204_2hosts_withroles` a été utilisé.
  - Modification du fichier `hosts` pour inclure les IP des VMs, ainsi que les informations de connexion.

- **Exécution du Playbook** :
  - Le playbook `site.yml` a été exécuté avec succès, permettant le déploiement de l'application sur les VMs.
  - Accès vérifié à l'application via `http://ADRESSE_IP_DE_VOTRE_VM_WEB/index.php`.

### Tâche 2: Installation de microk8s avec Ansible

- **Création du Playbook** :
  - La structure recommandée par [Ansible documentation](https://docs.ansible.com/ansible/latest/tips_tricks/sample_setup.html) a été suivie pour la création du nouveau playbook destiné à l'installation de microk8s.

- **Développement du Playbook** :
  - Utilisation des modules `apt`, `snap`, et `shell` pour reproduire les étapes d'installation de microk8s, incluant Docker et les services nécessaires à microk8s.
  - Configuration de Docker pour utiliser un registre non sécurisé, conformément aux instructions.

- **Résultat** :
  - Le playbook a été exécuté avec succès, installant microk8s sur la VM désignée. Les services essentiels tels que `dns`, `storage`, `dashboard`, `ingress`, et `registry` ont été activés et vérifiés.

## Conclusion

Ce TP a offert une introduction pratique à Ansible, en démontrant son efficacité pour le déploiement automatisé d'applications et de configurations sur des environnements virtual
