Installation de Docker sous Linux
La plateforme de conteneurisation Docker permet de créer, distribuer et exécuter des applications dans des conteneurs légers. Voici comment installer Docker sur un système Linux :

Prérequis
Un accès à une ligne de commande en tant qu'utilisateur avec les privilèges de superutilisateur (ou en ajoutant sudo devant les commandes).
Étape 1 : Mise à jour du Système
Avant d'installer Docker, assurez-vous que votre système est à jour en exécutant les commandes suivantes :
``` bash
sudo apt update
sudo apt upgrade
```
Étape 2 : Installation de Docker
Installez les dépendances nécessaires :
``` bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
Ajoutez la clé GPG officielle de Docker :
``` bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
Ajoutez le repository Docker :
``` bash
echo "deb [signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

Installez Docker :
``` bash
sudo apt update
sudo apt install docker-ce
```
Démarrer et activer le service Docker :
``` bash
sudo systemctl start docker
sudo systemctl enable docker
```
Étape 3 : Vérification de l'Installation
Vérifiez que Docker a été installé correctement en exécutant la commande :
``` bash
docker --version
```

Vous devriez voir la version de Docker installée affichée dans la sortie.