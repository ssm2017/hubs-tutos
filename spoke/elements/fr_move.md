## Deplacements

### Spawn point
- transformable : oui
- unique : non

#### Description
Un point où les avatars apparaissent quand ils entrent dans la scene.

#### Utilisation

#### Options
Aucune.

### Way point
- transformable : oui
- unique : non

#### Description
Un point vers lequel les avatars peuvent se téléporter.

#### Utilisation
Une fois entré dans la scene, on peut voir les "way points" en appuyant sur la barre espace. On peut s'y téléporter en cliquant sur l'icone du way point qui apparait.

#### Options
* Spawn Point : les avatars peuvent être téléportés vers ce point quand ils entrent dans la scene.
* Can be occupied : Apres chaque utilisation, ce point sera inactif jusqu'à ce que l'utilisateur précédent quitte ce point.
* Clickable : Ce point sera visible quand on clique sur la barre d'espace et on pourra s'y téléporter.
* Disable Motion : les avatars ne seront pas capables de bouger une fois posé sur le point.
* Disable Teleporting : les avatars ne pourront plus se téléporter une fois posé sur le point.
* Snap to floor plan : les avatars se téléporteront au plus pres du point mais sans quitter le sol.
* Maintain initial orientation : au lieu de pivoter l'avatar dans l'axe du point, l'avatar gardera l'orientation qu'il avait avant d'utiliser ce point.

### Floor plan
- transformable : non
- unique : oui

#### Description
Définit la surface de votre scene sur laquelle les avatars peuvent se déplacer.

#### Utilisation

#### Options
* Auto Cell Size : taille automatique du plafond.
* Cell Height : hauteur du plafond.
* Agent Height : hauteur des avatars.
* Agent Radius : largeur des avatars.
* Maximum Step Height : hauteur maximale des marches d'escaliers.
* Maximum Slope : pente maximale.
* Minimum Region Area : surface minimale de la région.
* Force Trimesh : force la triangulation des meshes.
* Collision Geo Triangulate Treshold : seuil de déclenchement des collisions.
* Regenerate : regénere les reglages apres les modifications de la scene.

### Box collider
- transformable : oui
- unique : non

#### Description
Cet élément permet de mettre des frontières physiques afin de retenir des avatars ou des mouvements d'objets (empecher de passer au travers).

#### Utilisation

#### Options
* Walkable : choisir si un avatar peut marcher dessus
