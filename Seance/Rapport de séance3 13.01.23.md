# Rapport de séance 3:
<h1>Ibadete :</h1>
 
On a eu l’idée, pour avoir quelque chose d’encore plus avancé, d’intégrer dans la semelle un podomètre qui va calculer le nombre de pas que l’on fait. 
On va intégrer un écran LCD où le nombre de pas sera afficher. <br>
J’ai fait le code pour le compteur de pas qui est réalisé avec un accéléromètre ADXL 335 parce que c’est un accéléromètre sensible de très petite taille de 3-axes 
qui convient donc à notre projet.<br>
J’ai aussi relié l’écran LCD I2C ; je vais essayer pour la prochaine séance d’écrire un code reliant finalement la distance 
et la vitesse en utilisant le nombre de pas que l’on fait en 100 mètres et en divisant par le temps et enfin afficher la vitesse aussi sur l’écran LCD.<br>
 
La prochaine séance, je vais me concentrer sur le code pour les capteurs et l’affichage sur ordinateur.

<h1>Paul :</h1>

Durant la séance, je me suis concentré sur le prototype de notre semelle.<br>
J'ai récupéré une semelle qui correspondait pratiquement à ma pointure puis je l'ai decoupé pour qu'elle soit parfaitement adaptée à ma chaussure.<br>
J'ai poncé le dessous de la semelle avec du papier de verre jusqu'à ce que le dos de la semelle soit lisse. <br>
Puis je me suis lancé dans la construction de notre semelle. On a opté pour une semelle correspondant au pied gauche.<br>
J'ai rassemblé nos capteurs. <br>

<h3>Problèmes:</h3>
Lors ce que j'ai fais une cartographie de la semelle. Je l'ai dessiné avec 20 capteurs. <br>
Seulement on ne dispose que d'une carte arduino de 6 ou 12 entrées donc pour simplifier la chose j'ai utilisé seulement 6 capteurs que l'on avait à notre disposition.<br>
J'ai relié ces 6 capteurs en faisant de la soudure. Ainsi chaque capteur est relié a une masse et une entrée ce qui signifie qu'il y a 12 soudures à réaliser.<br>
J'ai collé ces 6 capteurs avec du ruban adhésif ainsi on pourra transvaser nos capteurs sur une semelle en taille 44 
et ajouter une semelle fine ou alors utiliser la semelle fabriqué avec l'imprimante 3D pour protéger les capteurs lors des chocs.

  <h3>Objectifs lors de la prochaine séance</h3>
Lors de la prochaine sénace l'objectif sera de lié tous ces capteurs pour verifier si ils marchent bien puis étudier la foulée pour avoir la variation de la pression lorsque l'on marche.
<h3>Achats </h3>
- deux semelles en taille 44 assez fines si possible
