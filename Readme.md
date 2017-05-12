# Develophp-mysql

Ce document a pour but de déterminer les configurations et la mise en place d'un environnement de développement web avec Docker.

## Configuration Production

- Noyau GNU/Linux 
- PHP Version 7.0
- MySQL 5.5
- PHPMyAdmin
- Apache2
-- mysqli
-- pdo_mysql
-- mod_rewrite

## Installation Environnement

### Prérequis

- Docker
- Docker-Compose
- Fichier **docker-compose.yml**
- Fichier **Dockerfile**

### Installation

Installer *Docker* et *Docker-Compose*

Dans le dossier contenant le fichier **Dockerfile** :
```docker build -t kunzisoft/php-mysql:7.0-apache .```
pour construire l'image *kunzisoft/php-mysql:7.0-apache* avec la bonne version et les plugins.
(Voir https://hub.docker.com/_/php/)

Placer les fichiers de votre application dans le dossier *www*

### Lancement

Dans le dossier contenant le fichier **docker-compose.yml**, lancer les 3 plateformes avec :
```docker-compose up```

### Connexion

Votre application est accessible à l'url "http://localhost/"
PHPMyAdmin qui permet la gestion graphique de la base de données est disponible à l'url "http://phpmyadmin/"

### Configuration
Les fichiers .conf d'apache2 sont présents dans `config/apache2/`
Le fichier php.ini de configuration du PHP est présent dans `config/php/`
Le dossier mysql contient les fichiers plats correspondants à la base de données (A ne pas modifier, la suppression réinitialise la base)
