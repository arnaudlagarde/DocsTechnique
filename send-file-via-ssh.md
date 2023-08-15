# Documentation Technique : Envoi d'un Fichier via SSH sous Linux

L'envoi de fichiers via SSH permet de transférer des fichiers de manière sécurisée entre des machines distantes. Voici comment envoyer un fichier via SSH sur un système Linux :

## Prérequis

- Accès à une ligne de commande en tant qu'utilisateur avec les privilèges nécessaires.

## Étape 1 : Utilisation de la Commande `scp`

La commande `scp` (Secure Copy Protocol) permet de copier des fichiers de ou vers un serveur distant en utilisant SSH pour le chiffrement. Voici comment l'utiliser :

```bash
scp /chemin/vers/le/fichier utilisateur@hote:/chemin/de/destination
```

Remplacez /chemin/vers/le/fichier par le chemin absolu du fichier que vous souhaitez envoyer.
Remplacez utilisateur par votre nom d'utilisateur sur l'hôte distant.
Remplacez hote par l'adresse IP ou le nom d'hôte de l'ordinateur distant.
Remplacez /chemin/de/destination par le chemin absolu où vous souhaitez placer le fichier sur l'ordinateur distant.
Par exemple, pour envoyer un fichier nommé "mon_fichier.txt" depuis votre ordinateur local vers le répertoire "/home/utilisateur/documents" sur un ordinateur distant avec l'adresse IP "192.168.1.100" et le nom d'utilisateur "remoteuser", la commande serait la suivante :
```bash
scp mon_fichier.txt remoteuser@192.168.1.100:/home/utilisateur/documents/
```

Vous devrez saisir le mot de passe de l'utilisateur distant pour que le transfert ait lieu. Assurez-vous également que l'utilisateur distant a les autorisations appropriées pour accéder au chemin de destination et y écrire.