---
layout: post
title: "Configurer OVH pour Github Pages et s'en sortir vivant !"
category: 
- OVH
- Github Pages
- DNS
browser_title: "Configurer OVH pour Github Pages"
meta_description: "Comment configurer sa zone DNS sous OVH pour pointer vers votre belle page hébergée sur GitHub"
---
J'ai créé un site sur la *Savate Boxe Française* hébergé par un projet sous Github. Pour que se soit plus joli j'ai voulu lui associer un beau nom de domaine [www.esprit-savate.fr](http://www.esprit-savate.fr) et là, malgrè l'apparente facilité à le faire, ce fut le drame de ma semaine.

Comme indiqué sur les nombreux sites sur le net, effectuer les actions suivantes :

## Sur Github
Je suppose que vous disposez déjà d'un compte Github et que vous êtes familier avec Git.

1. Aller dans la branche `gh-pages` de votre projet ;
1. Ajouter un fichier CNAME à la racine de la branche ;
1. &Eacute;crire dans ce fichier votre nom de domaine `www.mondomaine.fr` sans mettre de retour à la ligne à la fin ;
1. Valider la modification.

## Sur OVH

1. Aller dans zone DNS et ajouter une entrée de type `CNAME`, nom de domaine en `www` et cible 'votre-repo.github.io.'. *Attention* le point à la fin de la cible est obligatoire !! ;
1. Valider ;
1. C'est fini.

Facile, traaannnquile... Oui mais... &Agrave; ce moment la propagation DNS doit se produire (certains disent dans les minutes à heures qui viennent mais en fait c'est quasi instantané). Sauf que dans mon cas rien ne s'est passé. Après moults tests et échanges avec le support il se trouve que l'entrée CNAME ajoutée à la console OVH n'était pas prise en compte.