## Eclairage

### Skybox
- transformable : non
- unique : oui

#### Description
Crée une visualisation d'un ciel ouvert et une atmosphere autour de la scene. Il est aussi utilisé en tant qu'environment map pour la scene.

#### Utilisation

#### Options
* Time of day : heure du jour.
* Latitude : latitude.
* Luminance : quantité de lumière.
* Scattering amount : quantité de dispersion.
* Scattering distance : distance de dispersion.
* Horizon start : debut de l'horizon.
* Horizon end : fin de l'horizon.

### Hemisphere light
- transformable : non
- unique : oui

#### Description
Cet élément ajoute une lumière unique éclairant depuis le dessus. La lumière n'emet pas d'ombres donc elle traverse les objets.

#### Utilisation

#### Options
* Sky color : couleur du ciel.
* Ground color : couleur du sol.
* Intensity : intensité de la lumière.

### Ambiant light
- tranformable : non
- unique : oui

#### Description
Une lumière qui illumine tous les objets dans votre scene.

#### Utilisation

#### Options
* Color : couleur de la lumière.
* Intensity : intensité de la lumière.

### Directional Light
- transformable : oui
- unique : non

#### Description
Cet élément ajoute une lumière directionnelle. Peu importe sa position, la lumière viendre toujours du même endroit. Seul son angle est pris en compte.

#### Utilisation

#### Options
* Color : couleur de la lumière.
* Intensity : intensité de la lumière.
* Cast shadows : choisir si la lumière émet des ombres.
* Shadow map resolution : choisir la précision des ombres.
* Shadow bias : reglage de la quantité d'ombre.
* Shadow radius : reglage du diametre de l'ombre (flou ou net).

### Spotlight
- transformable : oui
- unique : non

#### Description
Cet élément ajoute une lumière directionnelle mais permettant de regler son faisceau.

#### Utilisation

#### Options
* Color: couleur de la lumiere.
* Intensity : intensité de la lumiere.
* Inner cone angle : angle intérieur du faisceau.
* Outer cone angle : angle extérieur du faisceau.
* Range : distance de réaction de la lumière.
* Cast shadows : choisir si la lumière émet des ombres.
* Shadow map resolution : choisir la précision des ombres.
* Shadow bias : reglage de la quantité d'ombre.
* Shadow radius : reglage du diametre de l'ombre (flou ou net).

### Point light
- transformable : oui
- unique : non

#### Description
Cet élément ajoute une lumière omnidirectionnelle (emet tout autour d'un point).

#### Utilisation

#### Options
* Color: couleur de la lumiere.
* Intensity : intensité de la lumiere.
* Range : distance de réaction de la lumière.
* Cast shadows : choisir si la lumière émet des ombres.
* Shadow map resolution : choisir la précision des ombres.
* Shadow bias : reglage de la quantité d'ombre.
* Shadow radius : reglage du diametre de l'ombre (flou ou net).
