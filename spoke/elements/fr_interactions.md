[Retour elements](/spoke/elements/fr_elements.md) | [Retour début](/fr_index.md)
## Interaction

### Spawner
- transformable : oui
- unique : non

#### Description
Point de génération d'un objet avec lequel les avatars peuvent interagir.

#### Utilisation

#### Options
* Model Url : chemin vers le modèle à générer.
* Apply gravity to spawned object : rend l'objet généré physique (peut chuter au sol).

### Trigger Volume
- transformable : oui
- unique : non

#### Description
Change une propriété sur l'objet cible quand on entre et sort de l'element. (les options possibles à se jour sont seulement le départ ou l'arret d'une animation d'un modele 3d et lecture ou arret d'une video).

#### Utilisation

#### Options
* Target : objet cible
* Enter Component : composant concerné de la cible lors de l'entrée dans le volume.
* Enter property : propriété concernée du composant de la cible lors de l'entrée dans le volume.
* Enter value : valeur de la propriété lors de l'entrée dans la volume.
* Leave Component : composant concerné de la cible lors de la sortie du volume.
* Leave property : propriété concernée du composant de la cible lors de la sortie du volume.
* Leave value : valeur de la propriété lors de de la sortie du volume.

### Link
- transformable : oui
- unique : non

#### Description
Panneau cliquable permettant de déclencher un lien vers une autre scene ou bien un site web.

#### Utilisation

#### Options
* Url : url de la destination.

### Media frame
- transformable : oui
- unique : non

#### Description
Cadre permettant de capturer un objet.

#### Utilisation
Une fois le cadre en place sur la scene, on peut y faire glisser un media ou bien un objet et ce cadre devient un écran de projection.

#### Options
* Media Types : limite le type de media que ce cadre peut capturer.
