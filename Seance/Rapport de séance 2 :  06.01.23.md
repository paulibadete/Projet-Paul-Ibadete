# Rapport de séance 2 :
On a reçu 2 types de capteurs qui avaient deux forces différentes. On les a branché et codé chacun un type de capteur.<br>
On a remarqué qu’un des deux capteurs était plus convenable pour le talon où une personne va exercer beaucoup plus de force et l’autre capteur était plus 
convenable pour la partie du pied où l’on exerce moins de force lors d’une foulée.
<h2>Paul : </h2>
J’ai dessiné une voute plantaire de pointure 44. J’ai mesuré le nombre de capteurs qu’il faudrait mettre pour avoir un résultat le plus précis possible. <br>
Petit capteur : bout du pied on a une force de 47 lors de light touche monte à 400 lors de forte pression jusqu’à un grand max à 800 dans une position pas naturelle 
où je force au bout du pied. Donc on monte max à 800.<br>
Grand capteur talon : Monte à 840 au début puis diminue pour passer à medium touch 
lors pied plat puis light touch lorsque le poids est sur le bout du pied (fin de foulé).<br>

<h2>Ibadete : </h2>

Je me suis occupée de l’accéléromètre. Pour essayer de trouver la vitesse, j’ai trouvé un code qui pourrait marcher : 
j’intègre l’accélération en fonction du temps.<br> 
Cependant, L’accéléromètre est de bas de gamme donc il y aura beaucoup de bruit qui va donc nous donner des valeurs pas précises et beaucoup d’erreur. <br>
De plus, le pied ne bouge pas de façon linéaire donc il y aura un problème lorsqu’on bouge le pied dans un angle ou un autre. <br>
Il reste à voir si l’on utilise l’accéléromètre ou un gps qui marche que lorsqu’on est dehors. <br>


<h3>DISPOSITION CAPTEUR :</h3>
Capteur de force importante au talon, moins importante au milieu et moyennement importante au bout du pied.<br>

<h4>Explication de la foulée :</h4>
On va faire 8 rangées de 3 de capteurs pour avoir des mesures précises de notre pied.<br>
On doit prendre la valeur maximale de chaque mesure pour avoir une représentation globale de notre foulé.<br>
Pour cela on doit faire un tableau des mesures puis on prend une mesure on la définit comme maximale puis on prend la deuxième mesure si elle est 
plus grande on la garde sinon on reste avec la mesure initiale….<br>
On estime une foulé à 1 seconde donc il faut mettre un delay de 1 milli-seconde voir ne pas en mettre.<br>
Il faut voir le temps que prends arduino pour faire l’ensemble des mesures.<br>
On va mettre nos capteurs sur une semelle puis ajouter un plastique mou (sac poubelle) pour protéger les capteurs sans absorber les chocs.<br>
On met notre dispositif dans la poche composé d’un dispositif (accéléromètre ou gps) pour avoir la vitesse.<br>

