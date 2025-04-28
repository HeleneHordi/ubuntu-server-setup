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
