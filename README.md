# Autoduino

Arduino DUE shield to interface the I/O modules of A4 Technology // Autoduino est un bouclier pour Arduino DUE qui permet de piloter les maquettes A4 Technology utilisées pour l'enseignement de la technologie. Il permet également d'interefacer des module Grove.

![alt textAutoduino Shield](https://github.com/nbremond77/Autoduino-v4/blob/master/Hardware/rev%204/Output/Images/Autoduino-rev4%20-%20C.png)

Exemples de maquettes A4:


http://www.a4.fr/maquette-motorisee-programmable-portail-1-battant-version-kit.html


http://www.a4.fr/banc-d-essai-eclairage-domestique-autolumi-version-kit.html


http://www.a4.fr/autoalarme-maquette-experimentale-d-un-systeme-d-alarme-kit.html



Vous trouverez sur ce site, les fichiers relatif à la carte électronique, et les développements logiciels associés, dès qu'ils seront disponibles. Cette carte peut être programmée en utilisant l'environnement Arduino. Mais elle peut également en programmée avec Blockly@rDuino, l'excellent projet de Sébastien Canet.

# Introduction
Le bouclier Autoduino permet de piloter les maquettes A4 technology grâce à un Arduino UNO. Pour cela, le bouclier est équipé de 
- 16 connecteurs Jack 2.5mm permettant la connection des capteurs et actionneurs de la maquette, équipé de LED pour indiquer l'état de l'entrée ou de la sortie.
- 2 connecteurs jack 2.5mm pour deux moteurs DC,
- 2 LED RGB adressables (type WS2812B),
- 1 encodeur/push,
- quelques connecteurs supplémentaires permettant de connecter des capteurs/actionneurs plus évolués UEXT (I2C, SPI, Serial...) ou I2C pour un écran LCD (non testé) par exemple,
- 1 connecteur pour un module BlueTooth,
- 1 convertisseur Step/Up permettant d'alimenter la carte et l'Arduino avec deux piles de 1.5V, ou avec un accumulateur 3.7V.


Pour supporter le grand nombre d'entrées/sorties, il a été nécessaire d'utiliser un GPIO Expander (PCA9555). Celà implique l'utilisation d'une bibliothèque logiciel adaptée.
La programmation de l'Arduino peut se faire grâce à blockly@rDuino: http://technologiescollege.github.io/ qui inclus maintenant la bibliothèque adéquate.

A noter: Autoduino utilise des composants CMS et des composants traversants. Le cuircuit imprimé fait 100x100mm et est du type double-face.

# Note importante
Une nouvelle version de cet Autoduino est en préparation. La carte électronique sera plus simple (moins de connecteurs), et surtout, elle sera adaptée à un Arduino Due qui dispose de beaucoup plus d'entrées/sortie. Cela permettra d'éviter l'utilisation du GPIO Explander (PCA9555), ce qui simplifie grandement le logiciel.
De plus, l'Arduino Due fonctionne en 3.3V, ce qui simplifie l'utilisation de périphériques récents (Ecran tactile LCD...). Les moteurs resteront connectés au 5V.
Enfin, c'est un processeur 32 bits beaucoup plus performant que celui de l'Arduino Uno;

De plus, j'ai prévu quelques amélioration:
- Ajout de connecteurs Grove en plus des connecteurs jack 2.5mm, pour permettre une utilisation beaucoup plus polyvalente,
- Possibilité de connecter le module Bluetooth sur un RX/TX différent de celui connecté à l'USB,
- Ajouter une interface permettant de connecter un écran tactile LCD de 2.8 pouces.

