# Animation
Une texture peut afficher seulement une partie apres l'autre.

Le principe est basé sur les "sprite sheets" qui sont utilisés depuis tres longtemps dans des jeux video.

Ce procédé peut servir à créer une animation de flammes ou personnage animé ou bien faire clignotter un projecteur ou autre sans avoir à charger une vidéo.

Nous allons prendre un exemple simple en créant un damier coloré avec inkscape puis l'exportant vers du PNG.

## Procédure
* Dans Blender, nous créons un objet "plane" qui est carré par défault (ça tombe bien car notre texture l'est aussi 512x512 pixels).
* Nous passons en mode "edit" afin de lui assigner un "mapping" uv.
* Nous créons un "materiau" dans lequel nous assignons une image de texture à sa couleur principale.
* Nous redimentionnons la map uv dans l'editeur uv afin que seul le carré rouge soit pris en compte (a, s 0.5, n puis x=0.250 et y=0.750) 
* Dans l'onglet des propriétés de l'objet, nous ajoutons un composant "hubs" "uv-scroll".
* Dans "speed", nous mettons 1 à la premiere valeur puis 0.5 à la deuxieme.
* Dans "increment", nous mettons 0.5 aux deux valeurs.
* Nous exportons le fichier en GLB puis le chargeons dans spoke.
Le résultat va faire changer la couleur du carré de rouge, vert, bleu, blanc... Jouer avec les valeurs de speed pour accelerer ou ralentir et en changeant le ratio entre les valeurs, on peut afficher que deux couleurs.

## Fichiers
* checkboard.svg : Fichier Inkscape permettant de créer un damier.
* checkboard.png : Fichier exporté depuis Inkscape.
* hubs_uv-scroll_checkboard.blend : Fichier Blender final.
* hubs_uv-scroll_checkboard.gltf : Fichier GLTF permettant de lire le code source.
* hubs_uv-scroll_checkboard.glb : Fichier GLB compilé.
