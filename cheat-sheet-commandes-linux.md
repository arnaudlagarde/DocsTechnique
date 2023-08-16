# Cheat Sheet des Commandes Linux

## Navigation dans les Répertoires

- `pwd` : Afficher le répertoire de travail actuel.
- `ls` : Lister les fichiers et répertoires dans le répertoire courant.
- `cd chemin` : Changer de répertoire vers le chemin spécifié.
- `cd ..` : Aller au répertoire parent.
- `cd` : Revenir au répertoire utilisateur.

## Manipulation de Fichiers et Répertoires

- `touch fichier` : Créer un fichier.
- `mkdir dossier` : Créer un répertoire.
- `cp source destination` : Copier un fichier ou répertoire.
- `mv source destination` : Déplacer ou renommer un fichier ou répertoire.
- `rm fichier` : Supprimer un fichier.
- `rm -r dossier` : Supprimer un répertoire et son contenu (attention !).
- `nano fichier` : Ouvrir un fichier dans l'éditeur de texte Nano.
- `chmod permissions fichier` : Changer les permissions d'un fichier (ex: `chmod 755 fichier`).

## Gestion des Utilisateurs et des Permissions

- `whoami` : Afficher le nom d'utilisateur actuel.
- `useradd nom_utilisateur` : Créer un nouvel utilisateur.
- `passwd nom_utilisateur` : Changer le mot de passe d'un utilisateur.
- `sudo commande` : Exécuter une commande avec des privilèges de superutilisateur.
- `chown nouveau_proprio fichier` : Changer le propriétaire d'un fichier.

## Gestion des Processus

- `ps` : Afficher les processus en cours d'exécution.
- `top` : Afficher la liste des processus en temps réel.
- `kill PID` : Terminer le processus avec le PID spécifié.
- `killall nom_processus` : Terminer tous les processus avec le nom spécifié.

## Réseautage

- `ifconfig` : Afficher les informations réseau.
- `ping adresse` : Envoyer des paquets ICMP à l'adresse spécifiée.
- `netstat` : Afficher les connexions réseau.
- `ssh utilisateur@hote` : Se connecter à une machine distante via SSH.

## Gestion des Paquets

- `sudo apt update` : Mettre à jour la liste des paquets disponibles.
- `sudo apt install nom_paquet` : Installer un paquet.
- `sudo apt remove nom_paquet` : Désinstaller un paquet.

## Autres

- `man commande` : Afficher le manuel pour une commande.
- `history` : Afficher l'historique des commandes précédemment exécutées.
- `clear` : Effacer le terminal.
- `exit` : Quitter le terminal.

---

Notez que cette "cheat sheet" ne couvre pas toutes les commandes Linux, mais elle inclut certaines des plus couramment utilisées et importantes. Utilisez `man` pour obtenir plus d'informations sur chaque commande.
