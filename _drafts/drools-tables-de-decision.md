---
layout: post
title: "Drools, Tables de décision et Ruleflow"
category: 
- drools
- jboss
- ruleflow
- "Table de décision"
- BRMS
- "Moteur de règles métiers"
browser_title: "Drools, Tables de décision et Ruleflow"
meta_description: "Comment faire marcher les tables de décision de Drools avec un ruleflow"
banner_image: drools-dt-ruleflow.png
---
La documentation de *Drools* est vraiment pauvre et la communauté autour de cette technologie des *moteurs de règles* (BRMS) assez marginale. 

La résolution des problèmes que l'on rencontre au cours des développements se heurte à cette absence de connaissance sur le sujet et devient vite un vrai calvaire.

# Ce qu'il faut savoir avant de commencer
*Drools* évolue beaucoup entre deux versions et il ne faut pas compter sur la retrocompatibilité. Ce qui marche dans une version peut ne plus fonctioner dans la version suivante et je ne parle même pas des versions SNAPSHOT.

Dans ce petit tutoriel il faudra utiliser la version *Drools 6.2.0.Final*.

# Le problème
Pour le développement d'un prototype, le client souhaitait un module avec des règles métier, si possible pas cher. Ça tombe bien, *Drools* est un BRMS open source gratuit.

Pour montrer qu'il est possible de personnaliser certaines règles facilement, nous avons ajouté une table de décision, simple, mais pour le prototype c'était suffisant et serait du plus bel effet.

*Drools* propose deux façons de faire des tables de décisions avec des fichiers Excel. Dans les deux cas, chaque ligne du fichier donnera une règle basée sur un template que nous définissons.

La première, pas très sexy, consiste à faire précéder les lignes de données par le template de la règle à exécuter. Cela fait apparaître dans le fichier Excel des informations de nature technique, modifiable par quiconque édite le fichier avec les séances de débogage obscures que cela implique.

La seconde, attirante celle-ci, sépare les données du template de règle. On a un fichier Excel d'un coté qui contient uniquement les données, la table de décision elle-même telle qu'une personne lambda peut l'imaginer. Et un template de règle de l'autre coté qui servira de patron pour créer les règles à exécuter sur la base de la table de décision.

On s'est naturellement jeté sur la seconde solution comme un junky sur un paquet de cocaïne. Et là, ce fut le drame...
Étude 
La version *6.2.0* de *Drools* (la version stable officielle au moment du développement du prototype) nécessite de compiler la table de décision en passant par le code, au contraire de la version *6.4* qui, elle, permet de simplement déclarer le fichier Excel et le template dans le fichier de configuration `kmodule.xml`. La façon de faire, documentée, ne permet pas d'utiliser cette méthode dans le cadre d'un *Ruleflow*.

# La solution
Avec *Drools 6.2.0.Final*, pour pouvoir utiliser des tables de décision dans le cadre d'un *Ruleflow* il faut utiliser la première façon proposée par la documentation. À savoir, un fichier Excel unique, contenant à la fois les données et le template. La construction de ce fichier est basée sur la convention plutôt que sur la configuration alors il faut bien respecter les libellés et la position des cellules contenant les données et le template. 

L'avantage de cette solution, parce qu'il y en a quand même un, c'est que une fois que la table de décision est bien formée il suffit de la placer à côté des autres règles et c'est tout. Pas de configuration supplémentaire, par de code, rien. Le système compile tout seul la table de décision pour générer l'ensemble de règles qui s'y rapporte.

Un projet d'exemple se trouve sur https://github.com/richard-fagot/drools-6.2.0-dt-jbpmn
