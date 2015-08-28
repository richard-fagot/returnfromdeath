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
---
La documentation de *Drools* est vraiment pauvre et la communauté autour de cette technologie des *moteurs de règles* (BRMS) assez marginale. 

La résolution des problèmes que l'on rencontre au cours des développement se heurte à cette absence de connaissance sur le sujet et devient vite un vrai calvaire.

## Ce qu'il faut savoir avant de commencer
*Drools* évolue beaucoup entre deux versions et il ne faut pas compter sur la retrocompatibilité. Ce qui marche dans une version peut ne plus fonctioner dans la version suivante et je ne parle même pas des versions SNAPSHOT.

Dans ce petit tutoriel il faudra utiliser la version *Drools 6.2.0.Final*.

## Le problème
Pour le développement d'un prototype, le client souhaitait un module avec des règles métiers, si possible pas cher. Ça tombe bien, *Drools* est un BRMS open source gratuit.

