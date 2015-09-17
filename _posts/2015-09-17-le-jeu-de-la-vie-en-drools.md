---
layout: post
title: "Drools, Le jeu de la vie"
comments: true
category: 
- drools
- jboss
- BRMS
- "Moteur de règles métiers"
- "Le jeu de la vie"
- "Conway's Game Of Life"
browser_title: "Le jeu de la vie"
meta_description: "Implémenter le jeu de la vie en guise d'exercice Drools"
banner_image: drools-dt-jbpmn/drools-cercueil.png
comments: true
---

Un collègue m'a montré son implémentation du jeu de la vie suite à son autoformation en *Haskell*. Simple et élégante comme on peut s'y attendre en *Haskell* cela m'a donné l'idée de le faire en *Drools*. 



##TL;DR
1. [Téléchargez l'exemple](https://github.com/richard-fagot/drools-6.2.0-ConwaysGameOfLife) ;
2. Suivez les instructions indiquées dans le *README.md*.

## Le contexte
Lorsqu'on suit les tutoriaux pour apprendre à faire du *Drools* (ou du *JRules* aussi d'ailleurs) il y a un exemple qui est systématiquement présenté pour illustrer ce qu'on peut faire avec un *BRMS* : la suite de Fibonacci. 

Bien que permettant d'illustrer la récursivité, j'ai toujours trouvé cet exemple peu ludique et peu motivant.

Au contraire, le jeu de la vie est un exemple ludique et motivant car le résultat de l'exécution du moteur de règle peut se voir sous la forme d'une animation bien sympathique.

## Le jeu de la vie
Le jeu de la vie est un automate cellulaire inventé en 1970 par *John H. Conway*. Ce dernier essaya de simplifier un machine qui pourrait s'auto-reproduire inventée par *John Von Neumann*. Il y parvint avec un certain succès vu que le jeu de la vie est probablement l'automate cellulaire le plus connu au monde !

Son travail déboucha sur deux règles simples :
* une cellule morte qui possède exactement 3 voisines devient vivante ;
* une cellule vivante qui possède moins de 2 ou plus de 3 voisines meurt.

Pour plus d'information, je vous invite à consulter [l'article wikipedia](https://fr.wikipedia.org/wiki/Jeu_de_la_vie).


## L'implémentation
Le jeu de la vie se résume en deux règles, ça tombe bien *Drools* est un moteur de règles et il ne nous faudra pas plus que ces deux règles exactement pour implémenter notre solution.



## L'exécution

![Le jeu de la vie]({{site.imagebaseurl}}/assets/images/drools-jeu-de-la-vie/LeJeuDeLaVie.gif){:.img-center}

Pour rendre la chose plus ludique et attrayante j'ai ajouté une visualisation graphique des différents calculs portés par *Drools*.

Exécutez la classe `Main.java` comme projet java et émerveillez-vous devant le miracle des multiples résurrections !


Le projet d'exemple se trouve sur <https://github.com/richard-fagot/drools-6.2.0-ConwaysGameOfLife>
