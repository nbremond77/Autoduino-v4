# Autoduino

Arduino DUE shield to interface the I/O modules of A4 Technology // Autoduino est un bouclier pour Arduino DUE qui permet de piloter les maquettes A4 Technology utilisées pour l'enseignement de la technologie. Il permet également d'interefacer des module Grove.

![alt textAutoduino Shield](https://github.com/nbremond77/Autoduino-v4/blob/master/Hardware/rev%204/Output/Images/Autoduino-rev4%20-%20C.png)

Exemples de maquettes A4:


http://www.a4.fr/maquette-motorisee-programmable-portail-1-battant-version-kit.html


http://www.a4.fr/banc-d-essai-eclairage-domestique-autolumi-version-kit.html


http://www.a4.fr/autoalarme-maquette-experimentale-d-un-systeme-d-alarme-kit.html



Vous trouverez sur ce site, les fichiers relatif à la carte électronique, et les développements logiciels associés, dès qu'ils seront disponibles. Cette carte peut être programmée en utilisant l'environnement Arduino. Mais elle peut également en programmée avec Blockly@rDuino, l'excellent projet de Sébastien Canet:

http://technologiescollege.github.io/Blockly-at-rduino/

https://github.com/technologiescollege/Blockly-at-rduino



# Introduction
Le bouclier Autoduino permet de piloter les maquettes A4 technology grâce à un Arduino DUE. Pour cela, le bouclier est équipé de 
- 14 connecteurs Jack 2.5mm permettant la connection des capteurs et actionneurs des maquette A4, équipé de LED pour indiquer l'état de l'entrée ou de la sortie. Des connecteurs Grove (4 broches) sont également prévus, et connectés aux mêmes entrées sorties (voir le schéma pour les détails). Les entrées sont équipées de résistances "Pull-Up" c'est à dire reliées à l'alimentation positive. Les entrées et sorties sont universelles (les schémas sont identiques), les 14 connections peuvent entre utilisées en entrée ou en sortie.
- 2 connecteurs jack 2.5mm pour deux moteurs DC, également complétés par des connecteurs Grove.
- 2 LED RGB adressables (type WS2812B),
- 1 encodeur/push,
- quelques connecteurs supplémentaires permettant de connecter des capteurs/actionneurs plus évolués (I2C, SPI, CAN, Serial...),
- 1 connecteur pour un module BlueTooth,
- 1 convertisseur Step/Up permettant d'alimenter la carte et l'Arduino avec deux piles de 1.5V, ou avec un accumulateur 3.7V,
- 1 connecteur pour un écran graphique couleur tactile de 2.8".


Pour supporter le grand nombre d'entrées/sorties, il a été nécessaire d'utiliser un Arduino plus complet que le UNO. Nous avons choisi le Arduino DUE qui est équipé d'un processeur 32 bits permettant d'héberger des programmes trés complexes.

# Spécificités de l'Arduino DUE

L'Arduino DUE fonctionne en 3.3V, et n'est pas compatible avec des périphériques fonctionnant en 5V. Assurez vous que les périphériques utilisés fonctionnent bien en 3.3V. Les deux interface moteur prévues sur la carte Autoduino sont quant-à-elles alimentées en 5V.


# Fabrication

Autoduino utilise des composants CMS et des composants traversants. Le cuircuit imprimé fait 100x100mm et est du type double-face à trous métalisés. Nous l'avons fait fariqué chez PCBWay.com à un prix trés compétitif. Tous les fichiers nécessaires à sa fabrication sont dans le répertoire Output/Manufacturing (voir le fichier .Zip dans ce répertoire). Pensez également à commander un "Stencyl" pour la face "Bottom". Le Stencyl est un feuille de métal performée au laser au niveau des pastilles de soudure, et qui permet de grandement faciliter l'application de la pate à braser utilisée pour souder les  composants CMS.

Pour l'assemblage, de nombreux composants sont "montés en surface (CMS) sur la face "Bottom". Nous avons utilisé le Stencyl pour appliquer la pate à braser, positionné les composants CMS sur la carte, et passé la carte aisni équipé dans un four à refusion fait "maison" (plusieurs projets sont disponibles sur le web...).
Le montage des composants traversants, et des 2 LED sur la face "Top" se fait manuellement, aprés la refusion et le refroidissement de la carte. Cette méthode permet de réaliser plusieurs exemplaires de la carte en un temps raisonnable.

# Programmation
La programmation de l'Arduino peut se faire grâce à blockly@rDuino: http://technologiescollege.github.io/ qui inclus maintenant la bibliothèque adéquate.

http://technologiescollege.github.io/Blockly-at-rduino/

https://github.com/technologiescollege/Blockly-at-rduino


