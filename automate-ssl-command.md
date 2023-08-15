# Documentation Technique : Automatisation de la Commande SSL sous Linux

L'automatisation de la commande SSL avec Let's Encrypt permet d'obtenir et de renouveler automatiquement des certificats SSL pour sécuriser vos sites web. Voici comment automatiser la commande SSL sous Linux :

## Prérequis

- Un serveur web (par exemple, Apache ou Nginx) déjà installé et configuré.
- Le système d'exploitation doit être pris en charge par Certbot (Let's Encrypt).

## Étape 1 : Installation de Certbot

Certbot est un outil permettant d'automatiser l'obtention et le renouvellement des certificats SSL Let's Encrypt. Installez-le en utilisant les commandes suivantes :
```bash
sudo apt update
sudo apt install certbot
```
## Étape 2 : Automatisation de la Commande SSL
Utilisez Certbot pour automatiser l'obtention d'un certificat SSL. La commande ci-dessous lancera le processus interactif pour configurer le certificat :
```bash
sudo certbot --apache
```
Suivez les instructions pour choisir les domaines à sécuriser et configurez les options de redirection et de préférences.

Certbot configurera automatiquement les fichiers de configuration de votre serveur web et renouvellera les certificats avant leur expiration.

## Étape 3 : Validation et Test
Après l'automatisation, testez la renouvellement automatique en exécutant la commande :
```bash
sudo certbot renew --dry-run
```

Cette commande simule le renouvellement et permet de s'assurer que le processus fonctionne correctement.