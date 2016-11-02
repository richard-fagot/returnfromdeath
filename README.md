# [returnfromdeath](richard-fagot.github.io/returnfromdeath)
Trucs, astuces et tutoriels pour se sortir de mauvaises situations 

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

