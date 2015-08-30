---
layout: post
title: "Installer une clé SSH pour github sous ubuntu 14.04"
comments: true
category: 
- ubuntu
- github
- ssh
#permalink: installing-apache2-php5-and-mysql-support-on-ubuntu-12-04
#meta_description: 'Installing apache2, php5 and MySQL support on Ubuntu 12.04'
#browser_title: 'Installing apache2, php5 and MySQL support on Ubuntu 12.04'
---

1. Suivre les étapes [indiquées dans Github](https://help.github.com/articles/generating-ssh-keys) sans faire la 5 ;
2. Faire `ssh-keyscan -t rsa github.com > ~/.ssh/known_hosts` ;
3. Faire l'étape 5 ;
4. cloner le projet git en utilisant le clone SSH.