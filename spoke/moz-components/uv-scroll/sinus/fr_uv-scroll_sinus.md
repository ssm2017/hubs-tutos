# Deplacement simple
Une texture peut simplement se déplacer selon les coordonnées U et V (horizontal et vertical).

Ce procédé peut servir à faire des effets visuels comme des cascades d'eau ou autre défilement.

Nous allons prendre un exemple simple en créant une sinusoide avec inkscape puis l'exportant vers du PNG.

## Procédure
* Dans Blender, nous créons un objet "plane" qui est carré par défault (ça tombe bien car notre texture l'est aussi 512x512 pixels).
* Nous passons en mode "edit" afin de lui assigner un "mapping" uv.
* Nous créons un "materiau" dans lequel nous assignons une image de texture à sa couleur principale.
* Dans l'onglet des propriétés de l'objet, nous ajoutons un composant "hubs" "uv-scroll".
* Dans "speed", nous laissons la premiere valeur à zero et mettons 1 à la deuxieme.
* Les valeurs de "increment" restent sur zero.
* Nous exportons le fichier en GLB puis le chargeons dans spoke.

## Fichiers
* sinus.svg : Fichier Inkscape pour créer une sinusoide.
* sinus.png : Fichier exporté depuis Inkscape.
* hubs_uv-scroll_sinus.blend : Fichier Blender final.
* hubs_uv-scroll_sinus.gltf : Fichier GLTF permettant de lire le code source.
* hubs_uv-scroll_sinus.glb : Fichier GLB compilé.
