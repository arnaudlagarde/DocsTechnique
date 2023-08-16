# Documentation Technique : Communication Automatisée entre Serveur 1 et Serveur 2 avec OpenSSH

Cette documentation explique comment établir une communication automatisée entre un Serveur 1 et un Serveur 2 en utilisant OpenSSH.

## Prérequis

- Les serveurs 1 et 2 sont accessibles via SSH.
- Les clés SSH sont générées et les clés publiques sont échangées entre les serveurs pour permettre une authentification sans mot de passe.

## Configuration des Clés SSH

1. Si ce n'est pas déjà fait, générez une paire de clés SSH sur le Serveur 1 en utilisant la commande :
   ```bash
   ssh-keygen
    ```

Copiez la clé publique du Serveur 1 vers le Serveur 2 pour permettre une authentification sans mot de passe :
```bash
ssh-copy-id utilisateur@serveur2
```

Automatisation de la Communication
Créez un script sur le Serveur 1 pour exécuter des commandes sur le Serveur 2 sans intervention :

```bash
nano script.sh
```

Ajoutez les commandes que vous souhaitez exécuter sur le Serveur 2 :
```bash
#!/bin/bash
ssh utilisateur@serveur2 "commande1"
ssh utilisateur@serveur2 "commande2"
```
Rendez le script exécutable :

```bash
chmod +x script.sh
```

Exécutez le script sur le Serveur 1 pour automatiser les commandes sur le Serveur 2 :
```bash
./script.sh
```

### Utilisation de sshpass (en option)
Si vous devez automatiser l'entrée du mot de passe SSH, installez sshpass et utilisez-le pour exécuter les commandes avec le mot de passe :

Installez sshpass :

```bash
sudo apt update
sudo apt install sshpass
```

Utilisez sshpass pour exécuter les commandes avec le mot de passe :
```bash
sshpass -p 'votre_mot_de_passe' ssh utilisateur@serveur2 "commande1"
```

### Note
Utilisez ces méthodes avec prudence et uniquement pour des tâches sécurisées.
Assurez-vous que les autorisations et les clés SSH sont correctement gérées pour éviter les vulnérabilités.