# Ubuntu Server Setup Guide

## 1. Installer Ubuntu Server
- Télécharger l'image ISO Ubuntu Server depuis le site officiel.
- Graver l'ISO sur une clé USB ou utiliser un outil comme Rufus.
- Démarrer depuis la clé USB et suivre les instructions d'installation.

## 2. Activer SSH
- Pendant l'installation, choisir d'installer OpenSSH Server.
- Sinon, après installation :
```bash
sudo apt update
sudo apt install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh

Vérifier que SSH fonctionne :
sudo systemctl status ssh

3. Configurer le Firewall (UFW)
Installer UFW si nécessaire :
sudo apt install ufw

Autoriser la connexion SSH :
sudo ufw allow OpenSSH
sudo ufw enable

Vérifier le statut du firewall :
sudo ufw status

4. Installer et configurer Nginx
Installer Nginx :
sudo apt install nginx

Autoriser Nginx dans le firewall :
sudo ufw allow 'Nginx HTTP'

Vérifier que Nginx fonctionne : Accéder à l'adresse IP publique du serveur dans un navigateur.

