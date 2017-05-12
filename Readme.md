# Develophp-mysql

Ce document a pour but de déterminer les configurations et la mise en place d'un environnement de développement web avec Docker.

## Configuration Production

- Noyau GNU/Linux 
- PHP Version 7.0
- MySQL 5.5
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

Placer les fichiers de votre projet dans le dossier www

### Lancement

Dans le dossier contenant le fichier **docker-compose.yml** :
```docker-compose up```
