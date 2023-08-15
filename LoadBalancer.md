# Documentation Technique : Mise en Place d'un Load Balancer sous Linux

Un load balancer distribue le trafic entrant entre plusieurs serveurs pour améliorer la disponibilité, la redondance et les performances. Voici comment mettre en place un load balancer sur un système Linux :

## Prérequis

- Plusieurs serveurs applicatifs configurés et opérationnels.

## Étape 1 : Installation de HAProxy

HAProxy est un logiciel de load balancing et de proxy TCP/HTTP. Installez-le en utilisant les commandes suivantes :
```bash
sudo apt update
sudo apt install haproxy
```
## Étape 2 : Configuration de HAProxy
Ouvrez le fichier de configuration de HAProxy (généralement /etc/haproxy/haproxy.cfg) avec un éditeur de texte :
```bash
sudo nano /etc/haproxy/haproxy.cfg
```

Configurez HAProxy pour répartir le trafic en éditant le fichier de configuration. Voici un exemple minimal de configuration pour équilibrer le trafic sur deux serveurs :

```bash
global
    daemon
    maxconn 256

defaults
    mode http
    timeout connect 5000ms
    timeout client 50000ms
    timeout server 50000ms

frontend http_front
    bind *:80
    default_backend http_back

backend http_back
    balance roundrobin
    server server1 IP_DU_SERVEUR_1:PORT check
    server server2 IP_DU_SERVEUR_2:PORT check
```

Assurez-vous de remplacer IP_DU_SERVEUR_1 et PORT par les informations appropriées pour votre premier serveur, et faites de même pour IP_DU_SERVEUR_2 et le deuxième serveur.

## Étape 3 : Redémarrage de HAProxy
Après avoir configuré HAProxy, redémarrez-le pour appliquer les changements :
```bash
sudo systemctl restart haproxy
```

## Étape 4 : Test du Load Balancer
Accédez au domaine ou à l'adresse IP de votre serveur HAProxy dans un navigateur web pour tester le load balancer en action. Vous devriez voir que le trafic est distribué entre les serveurs configurés.

