# [returnfromdeath](richard-fagot.github.io/returnfromdeath)
Trucs, astuces et tutoriels pour se sortir de mauvaises situations 

# Migration sous Hugo

Jekyll c'est bien mais l'installation de tous les outils est fastidieuse et compliquée, d'autant plus qu'il faut que je le fasse sur les différentes machines et différents OS à partir desquels je suis susceptible de mettre à jour le blog.

[Hugo](https://gohugo.io/) c'est un téléchargement et ça marche tout de suite.

Pour le thème, j'ai retenu [Materialize BP][https://github.com/spech66/materialize-bp-hugo-theme#configuration-and-theme-specific-settings]

# Installation de l'environnement de développement

1. [Installer Hugo](https://gohugo.io/getting-started/installing/) ;
1. Cloner le projet ;
1. Récupérer le sous-module pour le thème Materialize BP :
```
git submodule init
git submodule update
```
1. Lancer le server `hugo server -D` ;
1. Fin.


---

OLD

---

#Installer une clé SSH pour github sous ubuntu 14.04
1. Suivre les étapes sans faire la 5 dans https://help.github.com/articles/generating-ssh-keys/ 
2. Faire ssh-keyscan -t rsa github.com > ~/.ssh/known_hosts
3. Faire l'étape 5
4. cloner le projet git en utilisant le clone SSH

#Jekyll - Installer Jekyll pour faire tourner le theme Feeling Responsive
1. apt-add-repository ppa:brightbox/ruby-ng
2. apt-get update
3. apt-get install ruby2.2 ruby2.2-dev
4. apt-get install nodejs npm
5. gem install jekyll
6. 


# Jekyll - Utiliser le paginator ailleurs que dans /blog/ par exemple dans / directement

