# 🐧 FICHE DE RAPPEL LINUX : COMMANDES & CONCEPTS INDISPENSABLES

---

## 1. L’arborescence Linux (structure des dossiers)

| Répertoire     | Description                             |
|----------------|---------------------------------------|
| `/`            | Racine du système                      |
| `/bin`         | Binaries essentiels (commandes de base)|
| `/sbin`        | Binaries système (admin)               |
| `/etc`         | Fichiers de configuration système     |
| `/home`        | Répertoires personnels des utilisateurs|
| `/root`        | Home de l’administrateur (root)       |
| `/var`         | Fichiers variables (logs, spools…)    |
| `/usr`         | Logiciels, librairies, docs, binaires |
| `/tmp`         | Fichiers temporaires                   |
| `/lib`         | Librairies partagées essentielles     |
| `/dev`         | Fichiers spéciaux (périphériques)     |
| `/proc`        | Informations système en mémoire (pseudo-fs)|
| `/sys`         | Interface vers le noyau (pseudo-fs)   |

---

## 2. Commandes de base

| Commande         | Description                                 | Exemple                                |
|------------------|---------------------------------------------|--------------------------------------|
| `ls`             | Lister le contenu d’un dossier              | `ls -l`                              |
| `cd`             | Changer de dossier                           | `cd /etc`                           |
| `pwd`            | Afficher le chemin courant                   | `pwd`                              |
| `cp`             | Copier fichiers/dossiers                     | `cp source.txt destination.txt`    |
| `mv`             | Déplacer/renommer                           | `mv ancien.txt nouveau.txt`         |
| `rm`             | Supprimer fichiers                           | `rm fichier.txt`                    |
| `mkdir`          | Créer un dossier                             | `mkdir mon_dossier`                 |
| `rmdir`          | Supprimer un dossier vide                     | `rmdir mon_dossier`                 |
| `touch`          | Créer un fichier vide ou mettre à jour date | `touch fichier.txt`                 |
| `cat`            | Afficher le contenu d’un fichier             | `cat fichier.txt`                   |
| `head`           | Afficher les premières lignes d’un fichier   | `head -n 10 fichier.txt`            |
| `tail`           | Afficher les dernières lignes                 | `tail -n 10 fichier.txt`            |
| `find`           | Rechercher fichiers/dossiers                  | `find /home -name "*.txt"`          |
| `grep`           | Rechercher du texte dans un fichier           | `grep "mot" fichier.txt`            |
| `df`             | Afficher l’espace disque                        | `df -h`                           |
| `du`             | Taille des fichiers/dossiers                   | `du -sh dossier/`                  |
| `chmod`          | Modifier les permissions                        | `chmod 755 script.sh`               |
| `chown`          | Modifier propriétaire et groupe                | `chown user:group fichier.txt`     |
| `ps`             | Afficher les processus actifs                   | `ps aux`                          |
| `kill`           | Terminer un processus                           | `kill PID`                        |
| `top`            | Afficher les processus en temps réel            | `top`                            |
| `sudo`           | Exécuter une commande en tant qu’administrateur| `sudo apt update`                 |
| `man`            | Afficher le manuel d’une commande               | `man ls`                         |
| `echo`           | Afficher une chaîne ou variable                  | `echo "Hello"`                   |
| `history`        | Afficher l’historique des commandes              | `history`                       |
| `alias`          | Créer un raccourci de commande                   | `alias ll='ls -l'`               |

---

## 3. Gestion des fichiers et permissions

### Permissions Linux

Un fichier/dossier a 3 types de droits pour 3 catégories d’utilisateurs :

| Catégorie | Description             |
|-----------|-------------------------|
| u         | utilisateur (owner)      |
| g         | groupe                  |
| o         | autres (world)          |

### Droits possibles :

| Lettre | Description           |
|--------|-----------------------|
| r      | lecture (read)        |
| w      | écriture (write)      |
| x      | exécution (execute)   |

### Exemple de permissions


- `rwx` pour l’utilisateur (lecture, écriture, exécution)
- `r-x` pour le groupe (lecture, exécution)
- `r--` pour les autres (lecture)

---

### Modifier permissions

- **Symbolique :**

```bash
chmod u+x fichier.sh       # ajoute exécution à owner
chmod go-r fichier.txt     # enlève lecture à groupe et autres
````
## 4. Gestion des processus

| Commande       | Description                         |
|----------------|-----------------------------------|
| `ps aux`       | Voir tous les processus            |
| `top`          | Moniteur en temps réel             |
| `htop`         | Version améliorée de top (optionnel)|
| `kill PID`     | Terminer un processus              |
| `kill -9 PID`  | Forcer l’arrêt                    |
| `jobs`         | Afficher tâches en arrière-plan   |
| `fg`           | Ramener une tâche en avant-plan   |
| `bg`           | Envoyer tâche en arrière-plan     |


## 5. Réseau

| Commande           | Usage                          |
|--------------------|-------------------------------|
| `ip a`             | Affiche les interfaces réseau  |
| `ifconfig`         | Ancienne commande similaire    |
| `ping`             | Tester la connectivité réseau  |
| `netstat -tulnp`   | Voir les ports ouverts et services |
| `ss -tulnp`        | Alternative moderne à netstat  |
| `curl`             | Faire une requête HTTP         |
| `wget`             | Télécharger un fichier         |
| `traceroute`       | Tracer le chemin réseau        |
| `nslookup` / `dig` | Résolution DNS                 |

## 6. Disques & systèmes de fichiers

| Commande           | Usage                          |
|--------------------|-------------------------------|
| `df -h`            | Affiche l’espace disque disponible |
| `du -sh dossier/`  | Affiche la taille d’un dossier       |
| `mount`            | Liste les systèmes montés            |
| `umount /point`    | Démonte un système de fichiers       |
| `fsck`             | Vérifie un système de fichiers       |
| `blkid`            | Identifie les partitions              |

## 7. Éditeurs de texte essentiels

- `nano` : simple, facile à utiliser, idéal pour débutants  
- `vim` ou `vi` : puissant, avec une courbe d’apprentissage plus élevée  
- `cat`, `less`, `more` : afficher des fichiers en lecture seule

### Commandes de base pour vim

- `i` : passer en mode insertion  
- `Esc` : revenir en mode normal  
- `:w` : sauvegarder  
- `:q` : quitter  
- `:wq` ou `ZZ` : sauvegarder et quitter  
- `:q!` : quitter sans sauvegarder  

Si tu veux, je peux t’envoyer un petit guide vim aussi !

## 8. Applications / outils incontournables

| Outil         | Usage principal                      |
|---------------|------------------------------------|
| `ssh`         | Connexion sécurisée à un serveur   |
| `scp`         | Copier des fichiers via SSH        |
| `rsync`       | Synchroniser fichiers/dossiers     |
| `tar`         | Archiver/désarchiver fichiers      |
| `gzip`/`gunzip` | Compression/décompression          |
| `cron`        | Planifier des tâches automatisées  |
| `systemctl`   | Gestion des services systemd        |
| `journalctl`  | Consulter les logs systemd          |

## 9. Serveurs courants

| Serveur           | Usage principal                      | Commande de base                   |
|-------------------|------------------------------------|----------------------------------|
| **Apache**        | Serveur web HTTP                   | `sudo systemctl start apache2` (Debian/Ubuntu)<br>`sudo systemctl start httpd` (RedHat/CentOS) |
| **Nginx**         | Serveur web léger, reverse proxy   | `sudo systemctl start nginx`      |
| **MySQL / MariaDB**| Base de données relationnelle      | `sudo systemctl start mysql` ou `mariadb` |
| **PostgreSQL**    | Base de données relationnelle      | `sudo systemctl start postgresql` |
| **SSH (OpenSSH)** | Serveur de connexion sécurisée     | `sudo systemctl start ssh` ou `sshd` |
| **FTP (vsftpd)**  | Serveur FTP                       | `sudo systemctl start vsftpd`     |
| **Docker**        | Conteneurisation                   | `sudo systemctl start docker`     |

---

### Commandes utiles pour gérer les serveurs

- Démarrer un service :

```bash
sudo systemctl start nom_du_service

## Sécurité Linux

---

### 1. Gestion des utilisateurs et permissions

- Créer un utilisateur : sudo adduser nom_utilisateur
- Supprimer un utilisateur : sudo deluser nom_utilisateur
- Modifier les permissions d’un fichier : chmod 700 fichier (accès complet uniquement au propriétaire), chmod 755 dossier (rwx pour owner, rx pour groupe et autres)
- Changer propriétaire : chown user:group fichier

---

### 2. Firewall (pare-feu)

Outils courants : iptables (plus ancien, puissant mais complexe), firewalld (front-end dynamique pour iptables, courant sur RedHat/CentOS), ufw (Uncomplicated Firewall, simple à utiliser, courant sur Ubuntu)

Commandes ufw (Ubuntu/Debian) :

- Activer le firewall : sudo ufw enable
- Désactiver le firewall : sudo ufw disable
- Voir le statut et règles : sudo ufw status verbose
- Autoriser un port (exemple SSH port 22) : sudo ufw allow 22
- Bloquer un port : sudo ufw deny 23

Commandes firewalld (RedHat/CentOS/Fedora) :

- Démarrer firewalld : sudo systemctl start firewalld et sudo systemctl enable firewalld
- Ajouter une règle permanente (exemple HTTP) : sudo firewall-cmd --permanent --add-service=http puis sudo firewall-cmd --reload
- Lister les règles actives : sudo firewall-cmd --list-all

---

### 3. Gestion des accès SSH

Modifier le fichier /etc/ssh/sshd_config pour :

- Changer le port par défaut (22)
- Désactiver la connexion root directe (PermitRootLogin no)
- Autoriser uniquement certains utilisateurs (AllowUsers user1 user2)
- Utiliser des clés SSH au lieu des mots de passe

Redémarrer SSH après modification : sudo systemctl restart sshd

---

### 4. Audit et surveillance

- Journal système (avec systemd) : journalctl -xe
- Auditd : outil d’audit avancé (installation et configuration selon besoins)
- Fail2ban : protège contre les tentatives de brute force (sudo apt install fail2ban, sudo systemctl enable fail2ban, sudo systemctl start fail2ban)

---

### 5. Bonnes pratiques générales

- Garder le système à jour : sudo apt update && sudo apt upgrade
- Restreindre les accès réseau (firewall, SSH)
- Sauvegarder régulièrement les données
- Utiliser des mots de passe forts ou clés SSH

---

### 6. Outils complémentaires de sécurité

- chkrootkit : détecter rootkits
- rkhunter : scanner de rootkits et vulnérabilités
- AppArmor : contrôle d’accès obligatoire
- SELinux : sécurité renforcée (RedHat, CentOS)
```