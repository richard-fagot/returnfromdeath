Comment décoder les images transmises en SSTV depuis l'ISS avec presque rien.

## TL;DR
- Procurez-vous un récepteur Baofeng UV-5R ;
- Installez [Virtual Audio Cable](https://www.vb-audio.com/Cable/) ;
- Installez [MMSSTV](https://hamsoft.ca/pages/mmsstv.php) ;
- Trouvez à quel moment l'ISS passe au-dessus de vous [https://spotthestation.nasa.gov/](https://spotthestation.nasa.gov/) ;
- Installez-vous à l'extérieur dans un espace dégagé un peu avant l'heure de passage de l'ISS ;
- Sélectionnez la fréquence 145.800 MHz ;
- Désactivez le silencieux (squelch) ;
- Démarrez l'application dictaphone de votre téléphone ;
- Copiez l'enregistrement sur votre PC ;
- Lancez MMSSTV et redirigez le son vers le cable audio virtuel ;
- Appréciez l'image qui apparaît sur votre écran.

## La station radioamateur de l'ISS
À bord de la *Station Spatiale Internationale* (ISS), dans le module *Service ISS Russe* il y a un émetteur-récepteur radio de 25 watts (un Kenwood TM-D710) que les astronautes peuvent utiliser occasionnellement pour communiquer avec des écoles, par exemple, dans le cadre du programme [*ARISS*](http://www.ariss.org/) (Amateur Radio on International Space Station).

Cet émetteur est également utilisé en automatique comme répéteur FM mais, aussi, pour transmettre des images en SSTV (Slow Scan Television) lors d'événements organisés par ARISS.

Ces émissions sont faites sur la fréquence 145.800 MHz et sont recevables chaque fois que la station passe au-dessus de l'horizon de votre zone géographique.

Et pour les recevoir, un simple récepteur à 30€ suffit !

## Qu'est-ce que la SSTV ?
La SSTV (Slow Scan Television) est la transmission d'images fixes au travers de la phonie, c'est-à-dire dans les mêmes fréquences que celles de la voix.

Lorsqu'on écoute une émission SSTV en cours, on "entend" l'image. Il suffit donc de disposer d'un dictaphone pour enregistrer cette image et d'ensuite la décoder avec un logiciel approprié.

[Exemple de son que l'on entend lors de la transmission d'une image SSTV](https://soundcloud.com/richard-fagot/iss-sstv-signal-of-the-6th-image)

Et l'image correspondante.

![ss](20190216HHMM06of12.jpg)

## Comment capter le signal
### Le matériel
Pour capter ce signal venu de l'espace c'est très simple en fait. Il vous suffit d'un petit récepteur radio qu'on trouve aux alentours de 30€ sur un site de vente en ligne bien connu : le Baofeng UV-5R. Mais n'importe quel récepteur radio pouvant écouter en FM sur 145.800 MHz conviendra.

![Baofeng UV-5R]()

Cet appareil vous permettra aussi bien de capter les transmissions SSTV que les échanges avec les astronautes à bord de l'ISS (au moins ce que eux répondent, l'autre correspondant peut ne pas être audible s'il n'est pas à la portée de votre antenne).

### Configurer le UV-5R
Par défaut l'UV-5R est en mode talkie walkie. Il est préparamétré sur les fréquences qu'on utilise habituellement sur ce genre d'appareil.

Pour écouter la station internationnale il faut paramétrer la fréquence d'écoute sur 145.800 MHz.

Pour cela on passe l'UV-5R en mode fréquence en appuyant une fois sur le bouton *VFO*. Deux lignes de fréquences sont affichées. Celle qui nous intéresse est la première. Si à gauche de cette première ligne il n'y a pas de petit triangle, utiliser les touches haut/bas pour sélectionner la première ligne de fréquence puis taper 145800 sur le clavier numérique du récepteur.

Dans cette configuration on peut déjà écouter la station lorsqu'elle passe au-dessus de l'horizon et qu'elle émet un signal. En l'absence de signal on entend rien, même pas de bruit blanc. C'est bien parce qu'en l'absence de signal cela évite d'avoir ce bruit blanc désagréable et ça ne l'est pas parce que lorsque le signal est faible on risque de passer à côter et de créer des interruptions dans le signal SSTV et donc d'en dégrader la qualité.

Ce filtre s'appelle le silencieux (squelch en anglais, SQL dans le menu de l'UV-5R). Pour le désactiver on appuie deux fois sur *menu* et on utilise la flêche bas pour amener le niveau du filtre à 0. On valide en appuyant sur *menu* et on revient à la fréquence en appuyant sur *exit*. Maintenant on entend ce bruit blanc caractéristique de l'absence de signal. Ce n'est pas très agréable mais on ne loupera rien des émissions.

### Enregistrer les signaux
Dans cette configuration vous êtes prêts à écouter les signaux provenant de l'ISS. 

## Comment décoder les images
