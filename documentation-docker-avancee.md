# Documentation Technique : Utilisation Avancée de Docker

Cette documentation vise à vous aider à maîtriser Docker et à en tirer pleinement parti pour gérer et manipuler des conteneurs.

## Prérequis

- Docker doit être installé sur votre système.

## Commandes Docker Utiles

- `docker --version` : Afficher la version de Docker.
- `docker info` : Afficher des informations sur l'environnement Docker.

## Gestion des Images Docker

- `docker pull image:tag` : Télécharger une image depuis Docker Hub.
- `docker build -t image:tag chemin` : Construire une image à partir d'un Dockerfile.
- `docker images` : Afficher la liste des images locales.
- `docker rmi image` : Supprimer une image.
- `docker system prune` : Nettoyer les images non utilisées.

## Gestion des Conteneurs

- `docker run -it --name nom_conteneur image:tag` : Créer et démarrer un conteneur interactif.
- `docker ps` : Afficher la liste des conteneurs en cours d'exécution.
- `docker ps -a` : Afficher la liste de tous les conteneurs (y compris inactifs).
- `docker start nom_conteneur` : Démarrer un conteneur existant.
- `docker stop nom_conteneur` : Arrêter un conteneur en cours d'exécution.
- `docker restart nom_conteneur` : Redémarrer un conteneur.
- `docker exec -it nom_conteneur commande` : Exécuter une commande dans un conteneur en cours d'exécution.
- `docker rm nom_conteneur` : Supprimer un conteneur.
- `docker logs nom_conteneur` : Afficher les journaux d'un conteneur.

## Gestion du Réseau Docker

- `docker network create nom_reseau` : Créer un réseau personnalisé.
- `docker network ls` : Afficher la liste des réseaux.
- `docker network connect nom_reseau nom_conteneur` : Connecter un conteneur à un réseau.
- `docker network disconnect nom_reseau nom_conteneur` : Déconnecter un conteneur d'un réseau.

## Gestion des Volumes

- `docker volume create nom_volume` : Créer un volume.
- `docker volume ls` : Afficher la liste des volumes.
- `docker volume inspect nom_volume` : Afficher les détails d'un volume.
- `docker run -v nom_volume:chemin_conteneur image` : Utiliser un volume dans un conteneur.

## Utilisation de Docker Compose

- `docker-compose up -d` : Démarrer des services définis dans un fichier `docker-compose.yml`.
- `docker-compose down` : Arrêter et supprimer les services définis dans `docker-compose.yml`.

## Astuces Avancées

- Utilisez les options `-e` et `--env-file` pour gérer les variables d'environnement.
- Explorez les commandes `docker exec`, `docker commit`, `docker cp` pour plus de contrôle.
- Utilisez les balises et étiquettes pour organiser et gérer vos images.

## Contribution

Si vous souhaitez contribuer à cette documentation en ajoutant des astuces, des exemples ou des commandes avancées, n'hésitez pas à ouvrir une demande d'extraction (Pull Request). Votre contribution sera grandement appréciée !

---

**Note :** Veillez à toujours comprendre les actions que vous effectuez avec Docker, car elles peuvent avoir un impact significatif sur votre environnement.

