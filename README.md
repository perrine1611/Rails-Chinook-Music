# README
<h1> Exo 2 : Chinook Music </h1>
<br>
Versions: ruby '2.7.1' avec gem 'rails', '~> 6.1.1' <br>
<br>
+ utilisation des gem 'table_print' et 'faker'
<br>
Création de 2 models : Album et Track
<br>
<h2> Niveau facile </h2>
<br>
Quel est le nombre total d'objets Album contenus dans la base (sans regarder les id bien sûr) ? <br>
--> 347 (Album.count) <br>
<br>
Qui est l'auteur de la chanson "White Room" ? <br>
--> Eric Clapton (Track.find_by(title: "White Room")) <br>
<br>
Quelle chanson dure exactement 188133 milliseconds ? <br>
--> "Perfect" par Alanis Morrissette (Track.find_by(duration: "188133"))<br>
<br>
Quel groupe a sorti l'album "Use Your Illusion II" ? <br>
--> Guns N Roses (Album.find_by(title: "Use Your Illusion II")) <br>

<h2> Niveau moyen </h2>
<br>
Combien y a t'il d'albums dont le titre contient "Great" ? (indice) <br>
--> 13 (great = Album.where("title like ?", '%great%').count)
<br>
Supprime tous les albums dont le nom contient "music". <br>
<br>
Combien y a t'il d'albums écrits par AC/DC ? <br>
--> 2 <br>
<br>
Combien de chanson durent exactement 158589 millisecondes ? <br>
--> 0 (Track.find_by(duration: "158589"))