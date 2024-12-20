# Connexion à Distance sur Debian 12

<img src="https://github.com/user-attachments/assets/35ea3507-9d63-4a5d-ab85-d4342968476e" alt="SSH" width="100">

## Introduction

Ce guide explique comment configurer et utiliser une connexion à distance sécurisée via SSH sur Debian 12. Il inclut des instructions pour PuTTY et MobaXterm.

---

## Prérequis

- Accès à une machine Debian 12 avec des droits d'administration.
- Connaitre l'adresse IP de votre serveur Debian.
- Installer un client SSH (MobaXterm).

---

## Installation de SSH

```bash
sudo apt update
sudo apt install ssh
```
Vérifiez le statut :

```bash
sudo systemctl status ssh
```

Si le statut est <span style="color:red">**"inactive" ou rouge** :</span>

```bash
sudo systemctl start ssh
```

## Configuration de SSH

Passez en root :

```bash
su
```

Modifiez le fichier de configuration :

```bash
nano /etc/ssh/sshd_config
```

Ajoutez/modifiez les lignes suivantes 

<span style="color:lightblue"> **Changer le port (optionnel) :** </span>

```bash
Port 22117
```
Sauvegardez, puis redémarrez SSH :

```bash
sudo systemctl restart ssh
```

## Trouver l'adresse IP

```bash
ip a
```
Notez l'adresse IPv4 sous l'interface active (**eth0** ou **ens33**).

<img src="https://github.com/user-attachments/assets/4773b5cc-2681-4bd6-ba5d-b9ec6be27277" alt="SSH" width="150">

## Utiliser MobaXterm
1. Téléchargez et installez MobaXterm.
2. Cliquez sur **Session > SSH et configurez l'IP, le port et le nom d'utilisateur.**
3. Validez et connectez-vous. 



