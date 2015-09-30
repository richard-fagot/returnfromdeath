---
layout: post
title: "Installer Jekyll sous Mac OS"
comments: true
category: 
- Jekyll
- Ruby
- gem
- RVM
- Python
- Mac OS
- Homebrew
- NodeJS
browser_title: "Installer Jekyll sous Mac OS"
meta_description: "Comment installer facilement un environnement Jekyll complet."
banner_image: Jekyll-mac/jekyll-mac.png
comments: true
---

*Jekyll* est un moteur de blog statique, c'est-à-dire qu'il génère un ensemble de pages *HTML* classiques, pas de base de données, pas de back-office, pas de faille de sécurité. C'est la technologie employée dans *Github Pages*. 

Le site généré est directement employable derrière un serveur *HTTP* tel que *Apache* ou *Nginx*.


*Jekyll* est un moteur de blog que j'apprécie tout particulièrement pour sa simplicité de mise en oeuvre, rédactionnelle et la sécurité offerte par son aspect statique.

Les billets sont écrits en *Markdown*, réutilisables facilement sous différents environnements et même dans des moteurs de blog plus complexes, moyennant une petite migration. De plus, comme il s'agit de fichiers texte pur, il est facile de les versionner dans un système de control de version tel que *Git* ou *svn*.

## Installation

*Jekyll* repose sur *Ruby*. Malgré la présence par défaut de *Ruby* sur *Mac*, ce dernier est utilisé pour les besoins internes de *Mac* et dès que vous avez besoin de faire un `sudo gem ...` c'est que l'installation système ne suffit plus et qu'il vous faut installer une version indépendante plus classique.

### Homebrew

Si ce n'est déjà fait, je vous recommande d'installer [*Homebrew*](http://brew.sh/index_fr.html) qui est un gestionnaire de paquets pour *Mac*.

{% highlight bash %} 
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
{% endhighlight %}

Vous remarquerez qu'ici, on utilise le *Ruby* installé par défaut sur le *Mac*.

### Ruby

Pour pouvoir gérer l'installation de *Ruby* et, en particulier, de plusieurs versions en même temps, je vous recommande d'installer *RVM*. 

L'installation de *Ruby* et *RVM* se fera en une seule fois. Mais il faut commencer par enregistrer une clé GPG :

{% highlight bash %} 
brew install gnupg
gpg --keyserver hkp://keys.gnupg.net
    --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
{% endhighlight %}

Et enfin, réaliser l'installation de *Ruby* et *RVM* :

{% highlight bash %} 
\curl -sSL https://get.rvm.io | bash -s stable --ruby
{% endhighlight %}

Une fois l'installation terminée, fermez le terminal et ouvrez en un autre pour prendre en compte les nouvelles variables d'environnement.

### NodeJS

*NodeJS* est nécessaire en particulier pour des templates *Jekyll* comme [*Feeling Responsive*](https://phlow.github.io/feeling-responsive/).

{% highlight bash %} 
brew install nodejs
{% endhighlight %}

Il est possible d'installer un autre runtime *JavaScript* si on le souhaite.

### Python

*Python* est utilisé par le moteur de *Jekyll* pour la coloration syntaxique avec *Pygments*.

{% highlight bash %} 
brew install python
{% endhighlight %}

### Jekyll 

Et enfin, *Jekyll* :

{% highlight bash %} 
gem install jekyll
{% endhighlight %}

## Conclusion

Vous voilà avec un bel environnement *Jekyll* avec, en prime, un gestionnnaire de paquet bien pratique. Le tout sans être obligé de manger la Pomme Ténébreuse.

## Références

* [*Jekyll*](http://jekyllrb.com/docs/installation/)
* [*Homebrew*](http://brew.sh/index_fr.html)
* [*Ruby*](http://usabilityetc.com/articles/ruby-on-mac-os-x-with-rvm/)
* [*NodeJS*](https://nodejs.org/en/)
* [*Python*](https://www.python.org/)