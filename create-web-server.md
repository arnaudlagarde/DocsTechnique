# Documentation Technique : Création d'un Serveur Web sous Linux

La création d'un serveur web permet d'héberger des sites, applications et contenus en ligne. Voici comment créer un serveur web sur un système Linux :

## Prérequis

- Un système Linux installé (par exemple, Ubuntu).
- Accès à une ligne de commande en tant qu'utilisateur avec les privilèges nécessaires.

## Étape 1 : Installation d'un Serveur Web

1. Installez le serveur web Apache en utilisant les commandes suivantes :
```bash
sudo apt update
sudo apt install apache2
```

Le serveur Apache sera installé et automatiquement démarré. Vous pouvez vérifier son état avec la commande :
```bash
sudo systemctl status apache2
```

## Étape 2 : Configuration du Pare-feu
Si un pare-feu est activé, autorisez le trafic HTTP en utilisant la commande suivante :
```bash
sudo ufw allow 'Apache'
```

## Étape 3 : Accès au Serveur Web
Ouvrez un navigateur web et accédez à l'adresse IP de votre serveur (par exemple, http://adresse_ip_du_serveur). Vous devriez voir la page par défaut d'Apache, indiquant que le serveur fonctionne correctement.

## Étape 4 : Gestion des Fichiers Web
Les fichiers de votre site web sont stockés dans le répertoire /var/www/html. Placez vos fichiers HTML, CSS, JavaScript, etc. dans ce répertoire pour les rendre accessibles via le serveur web.

## Étape 5 : Configuration de Domaines Virtuels (Facultatif)
Si vous prévoyez d'héberger plusieurs sites sur le même serveur, configurez des domaines virtuels. Consultez la documentation d'Apache pour plus d'informations sur la configuration des hôtes virtuels.

