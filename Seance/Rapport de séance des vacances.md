<h1>Paul</h1>
<h3>Utilisation de la bibliotheque Maplotlib</h3>
Durant les vacances j’ai commencé la représentation des données. <br>
J’ai utilisé la bibliothèque Matplotlib qui permet d’afficher des données tel que des graphes ou des nuages de point. <br>
J’ai rencontré beaucoup de difficulté à installer cette bibliothèque sur mon ordinateur. <br>
Pour installer cette bibliothèque il fallait utiliser l’interprète de commande du terminale Windows et écrire « pip install Matplotlib » <br>
seulement cette commande ne répondait pas. <br>
J’ai fais plusieurs recherche pour régler le problème puis je suis tombé sur une information qui était en lien avec notre cours de Programmation Orienté Objet.<br> 
Le chemin (path) n’était pas le bon, je l’ai donc changé et l’installation de ma bibliothèque s’est faite normalement. <br>
Je me suis documenté sur cette bibliothèque j’ai cherché a savoir comment elle marchait puis j’ai réalisé un code (je l’ai mis dans le dossier). <br>
J’ai crée un graphe avec un nuage de point ou chaque point correspond à un capteur étant placé au même endroit que la semelle (en abscisse et en ordonnée) <br>
puis j’ai fait une échelle de pression allant de 0 à 800 et j’ai choisit des couleurs qui convenait à notre projet. <br>
J’ai utilisé l’arrière-plan d’une semelle que j’ai customisé pour avoir une vision globale du pied.<br>
<h3>Utilisation de la bibliotehque Pandas</h3>
Mon problème était maintenant de mettre les données Excel sur ce fichier python. Pour cela j’ai téléchargé la bibliothèque pandas.<br> 
Je me suis à nouveau documenté sur cette nouvelle bibliothèque puis j’ai fait un code qui me permettait de renvoyer les données du tableau sur python. <br>
J’ai également eu un problème car python ne voulait pas me renvoyer de valeur. <br>
En faisant mes recherches j’ai appris que python ne pouvait lire que les tableau Excel finissant par xls et non xlsx que j’utilisais. <br>
J’ai donc utilisé un convertisseur puis mes données se sont affichées normalement.<br>
Maintenant il me fallait sélectionner seulement la dernière ligne de mes données et les transformer en une liste pour pouvoir affichés ces données sur mon graphique.<br>
J’ai appris par la suite qu’il existait la bibliothèque serial qui permet de faire directement le lien entre Arduino et python. <br>
Je travaille dessus actuellement j’ai réussi à télécharger la bibliothèque.<br>
<h3>Reconstruction du code des capteurs</h3>
De plus, j’ai reconstruit le code des capteurs que j’avais créé précédemment car il n’était pas assez précis. 
Grace à ce code je peux renvoyer la valeur maximale durant une foulée, compter le nombre de foulée te le temps de contact au sol et 
renvoyer une moyenne des valeurs maximale de chaque capteur à chaque foulée.
