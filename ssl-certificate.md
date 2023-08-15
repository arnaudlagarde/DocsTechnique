# Documentation Technique : Mise en Place d'un Certificat SSL sous Linux pour HTTPS

Le protocole HTTPS sécurise les communications entre un client et un serveur en utilisant un certificat SSL/TLS. Voici comment mettre en place un certificat SSL pour activer HTTPS sur un serveur Linux :

## Prérequis

- Un serveur web (par exemple, Apache ou Nginx) déjà installé et configuré.

## Étape 1 : Installation de Certbot

Certbot est un outil qui automatise le processus d'obtention et de renouvellement des certificats SSL. Installez-le en utilisant les commandes suivantes :
```bash
sudo apt update
sudo apt install certbot
```
## Étape 2 : Obtenir un Certificat SSL
Pour obtenir un certificat SSL pour votre domaine, exécutez la commande suivante en remplaçant votre_domaine.com par votre propre nom de domaine :
```bash
sudo certbot certonly --webroot -w /var/www/html -d votre_domaine.com
```

Suivez les instructions pour fournir une adresse e-mail de contact et accepter les termes d'utilisation.

Le certificat sera téléchargé et sauvegardé sur votre serveur.

## Étape 3 : Configuration du Serveur Web
Configurez votre serveur web pour utiliser le certificat SSL fraîchement obtenu. Voici comment le faire pour Apache et Nginx :

### Configuration pour Apache
Ouvrez le fichier de configuration d'Apache (généralement /etc/apache2/sites-available/000-default.conf) et ajoutez les lignes suivantes à l'intérieur de la balise <VirtualHost> correspondant à votre domaine :
```bash
SSLEngine on
SSLCertificateFile /etc/letsencrypt/live/votre_domaine.com/fullchain.pem
SSLCertificateKeyFile /etc/letsencrypt/live/votre_domaine.com/privkey.pem
```

Configuration pour Nginx
Ouvrez le fichier de configuration de Nginx (généralement /etc/nginx/sites-available/default) et ajoutez les lignes suivantes à l'intérieur du bloc de serveur correspondant à votre domaine :

```bash 
ssl_certificate /etc/letsencrypt/live/votre_domaine.com/fullchain.pem;
ssl_certificate_key /etc/letsencrypt/live/votre_domaine.com/privkey.pem;
```

## Étape 4 : Redémarrage du Serveur Web
Après avoir configuré le certificat, redémarrez le serveur web pour appliquer les changements :
```bash
sudo systemctl restart apache2     # Pour Apache
sudo systemctl restart nginx       # Pour Nginx
```

## Étape 5 : Vérification du Certificat

Vérifiez que le certificat SSL est correctement installé en accédant à votre site via HTTPS (https://votre_domaine.com). Vous devriez voir le cadenas vert dans la barre d'adresse.


