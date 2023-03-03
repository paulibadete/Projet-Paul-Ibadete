<h1>PAUL</h1>
J’ai continué le code que j’ai fait pendant les vacances (voir dans les séances). <br>
J’ai amélioré le schéma de la répartition des forces en ajoutant une légende à la barre de couleur.<br>
J’ai fait un graphique de la pression maximale pour les 6 capteurs en fonction de la foulée. <br>
Dans ce graphique j’ai utilisé la bibliothèque pandas pour extraire les données des valeurs maximales des 6 capteurs. <br>
J’ai créé une liste à partir de ces valeurs. Ainsi j’ai 7 listes en ajoutant la liste contenant les foulées. <br>
J’ai utilisé Matplotlib et la fonction … pour afficher les valeurs maximales des 6 capteurs en fonction du nombre de foulée. <br>
Ensuite j’ai voulu représenter la vitesse, la distance, le nombre de pas, le temps de contact au sol. <br>
Pour faire cela j’ai créé un graphique, j’ai choisi la couleur du graphique en valeur RGB. <br>
Puis j’ai importé une police que je trouvais adapté à notre projet qui est la police similaire à un réveil. <br>
Ensuite j’ai joué avec les coordonnées, la taille du texte, la couleur du texte qui répond à un ordre logique des couleurs pour paraitre le plus esthétique possible. <br>
Apres j’ai ajouté une image sur ce graphique. Puis j’ai commencé un autre graphique qui devait représenter les 6 valeurs moyennes des capteurs. <br>
Pour faire cela j’ai fait de la même façon et j’ai ajouté une photo pour rendre plus beau le graphique. Une fois que chacun de mes 4 graphiques était créé. <br>
J’ai créé un graphique qui devait contenir ces 4 graphiques. J’ai eu énormément de mal et j’ai passé plusieurs heures à comprendre comment faire cela. <br>
Finalement j’ai réussi à crée une disposition personnalisée de ce que je voulais faire. <br>
J’ai créé chaque graphique de chaque axe du graphique et j’ai ajouté des légendes pour mes graphiques. <br>
Ensuite, j’ai essayé de faire marcher mon code, seulement j’avais un problème car rien ne s’affichait pour résoudre cela <br>
j’ai fait plusieurs tests pour vérifier mon code, j’ai créé pleins de mini codes puis je me suis rendu compte que le problème venait de la valeur seuil. <br>
J’ai donc augmenté ma valeur seuil puis le problème était résolu. Maintenant il me restait à tester chaque capteur pour mettre une valeur seuil à chacun des capteurs.<br> 
Un fois cela fait mes branchements n’était pas bon, j’ai refait mes branchements car j’avais inversé des entrées. <br>
Puis j’ai essayé mon code il marchait correctement seulement il m’affichait parfois des valeurs qui ne sont pas intéressantes. <br>
J’ai essayé de trouver des solutions. Puis j’ai eu l’idée suivante : je vais utiliser ma macro plx-daq pour mettre les valeurs Arduino sur Excel puis <br>
je vais filtrer moi-même les données. J’ai cherché comment supprimer les lignes qi ne sont pas intéressante c’est-à-dire des lignes qui comprenne des nombres <br>
plus petits que 100 car cela va fausser les résultats de la moyenne puis J’ai cherché comment calculer une moyenne avec des valeurs sur une colonne. <br>
J’utilise donc la fonction MOYENNE de Excel puis la fonction ARRONDI pour arrondir à l’entier correspondant. <br>
Je trouvais cela hyper intéressant et je me suis renseigné sur une façon pour automatiser tous cela. <br>
Il faut utiliser une macro mais je pense que cela n’est pas de mon niveau. <br>
Une fois que j’aurai la fonction pour calculer le nombre de pas et la vitesse il me restera plus qu’a l’afficher sur mon tableau Excel puis à obtenir <br>
la valeur moyenne de la vitesse et le nombre totale de pas que je vais ajouter à mon code pour pouvoir l’afficher sur mon interface graphique.<br>
