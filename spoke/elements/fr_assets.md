## Assets

### Model
- transformable : oui
- unique : non

#### Description
Cet élément permet d'ajouter un modèle 3D à la scène.

#### Utilisation

#### Options
* Model url : chemin vers le modele 3d.
* Loop animation : choisir une ou des animation(s) à exécuter sur le modèle qui en possède.
* Collidable : choisir si le modèle réagit physiquement aux autres objets (collision).
* Walkable : choisir si un avatar peut marcher dessus.
* Cast shadow : choisir si le modèle émét des ombres si une lumière l'atteint.
* Receive shadow : choisir si le modèle reçoit les ombres des autres objets.
* Combine :

### Image
- transformable : oui
- unique : non

#### Description
Affiche une image.

#### Utilisation

#### Options
* Image Url : chemin vers l'image.
* Controls : affiche les options de media dans la scene.
* Transparency mode : type de transparence si besoin.
* Projection : type de projection de l'image.

#### Astuce
En utilisant la projection "360-equirectangular" et en rendant l'image énorme avec le "scale", il est possible de faire une image d'environnement (HDRI).

### Video
- transformable : oui
- unique : non

#### Description
Affiche une video.

#### Utilisation

#### Options
* Video : chemin vers la video.
* Projection : type de projection de la video.
* Controls : affiche les options de media dans la scene.
* AutoPlay : si actif, lit automatiquement la video lors de l'entrée dans la scene.
* Loop : lecture en boucle de la video.
* Audio Type : systeme de reaction de l'audio.
* Volume : volume de l'audio.
* Distance Model : attenuation de l'audio.
* Rolloff Factor : facteur de l'attenuation de l'audio.
* RefDistance : distance de declenchement de l'audio.
* Max Distance : distance maximale de reduction de l'audio.
* Cone Inner Angle : rayon interne de la directivité de l'audio.
* Cone Outer Angle : rayon externe de la directivité de l'audio.
* Cone Outer Gain : reduction du gain proportionnellement au rayon externe de la directivité de l'audio.

### Audio
- transformable : oui
- unique : non

#### Description
Diffuse un son.

#### Utilisation

#### Options
* Audio Url : chemin vers le son.
* Controls : affiche les options de media dans la scene.
* AutoPlay : si actif, lit automatiquement le son lors de l'entrée dans la scene.
* Loop : lecture en boucle du son.
* Audio Type : systeme de reaction de l'audio.
* Volume : volume de l'audio.
* Distance Model : attenuation de l'audio.
* Rolloff Factor : facteur de l'attenuation de l'audio.
* RefDistance : distance de declenchement de l'audio.
* Max Distance : distance maximale de reduction de l'audio.
* Cone Inner Angle : rayon interne de la directivité de l'audio.
* Cone Outer Angle : rayon externe de la directivité de l'audio.
* Cone Outer Gain : reduction du gain proportionnellement au rayon externe de la directivité de l'audio.


### Particle Emitter
- transformable : oui
- unique : non

#### Description
Emetteur de particules.

#### Utilisation

#### Options
* Particle Count : Nombre de particules emises.
* Image : chemin vers une image emise en particules.
* Age Randomness : temps aleatoire de generation des particules.
* Lifetime : duree de vie d'une particule.
* Lifetime Randomness : duree de vie aleatoire d'une particule.
* Size Curve : courbe de variation de la taille.
* Start Particle Size : taille de depart.
* End Particle Size : taille de fin.
* Size Randomness : taille aleatoire.
* Color Curve : courbe de variation de la couleur.
* Start Color : couleur de depart.
* Start Opacity : opacité de depart.
* Middle Color : couleur intermediaire.
* Middle Opacity : opacité intermediaire.
* End Color : couleur de fin.
* End Opacity : opacité de fin.
* Velocity Curve : courbe de vélocité.
* Start Velocity : vélocité de depart.
* End Velocity : vélocité de fin.
* Angular Velocity : angle de vélocité.

#### Astuce
En emettant une seule particule à vie infinie, il est possible de faire afficher une image etant toujours orientée vers la personne qui la regarde...

### Simple Water
- transformable : oui
- unique : non

#### Description
Génère un plan d'eau.

#### Utilisation

#### Options
* Color : couleur de l'eau.
* Opacity : opacité de l'eau.
* Tide Height : hauteur de la marée.
* Tide Scale : taille de la marée.
* Tide Speed : vitesse de la marée.
* Wave Height : hauteur des vagues.
* Wave Speed : vitesse des vagues.
* Ripples Speed : vitesse des ondulations.
* Ripples Scale : taille des ondulations.
