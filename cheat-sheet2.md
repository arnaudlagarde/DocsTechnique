# Cheat Sheet des Commandes Linux Avancées

## Manipulation de Texte

- `grep motif fichier` : Rechercher un motif dans un fichier.
- `sed 's/motif/remplacement/' fichier` : Remplacer un motif par un autre dans un fichier.
- `awk '{action}' fichier` : Traiter et manipuler des données dans un fichier.

## Gestion des Disques et du Stockage

- `df` : Afficher l'utilisation de l'espace disque.
- `du -h` : Afficher la taille des fichiers et répertoires.
- `fdisk -l` : Afficher les informations sur les disques et partitions.
- `mount point_montage` : Monter un système de fichiers.

## Compression et Décompression

- `tar -czvf archive.tar.gz dossier` : Créer une archive compressée.
- `tar -xzvf archive.tar.gz` : Extraire une archive.
- `zip archive.zip fichier` : Créer une archive zip.
- `unzip archive.zip` : Extraire une archive zip.

## Gestion des Services

- `systemctl status service` : Afficher l'état d'un service.
- `systemctl start service` : Démarrer un service.
- `systemctl stop service` : Arrêter un service.
- `systemctl restart service` : Redémarrer un service.

## Surveillance Système

- `htop` : Moniteur de processus en temps réel avec interface utilisateur.
- `iotop` : Moniteur d'entrées/sorties en temps réel.
- `free -h` : Afficher l'utilisation de la mémoire.

## Programmation de Tâches

- `cron` : Planificateur de tâches automatisées.
- `crontab -e` : Modifier les tâches cron de l'utilisateur.
- `at` : Planifier une tâche unique à un moment précis.

## Gestion des Utilisateurs et des Groupes

- `usermod -aG groupe utilisateur` : Ajouter un utilisateur à un groupe.
- `groupadd nom_groupe` : Créer un nouveau groupe.

## Gestion des Droits d'Accès

- `chmod` : Modifier les permissions d'accès aux fichiers.
- `chown` : Modifier le propriétaire et le groupe d'un fichier.

## Réseau Avancé

- `netcat` : Utilitaire pour lire ou écrire sur des connexions réseau.
- `tcpdump` : Capturer et afficher le trafic réseau en temps réel.
- `nmap` : Scanner de ports pour découvrir des informations sur les hôtes.
