[Retour début](/fr_index.md)
# Elements Spoke
Spoke permet de créer des "scenes" pouvant être utilisées dans hubs.

La partie droite de l'ecran principal de spoke contient 2 parties :
- Hierarchy : ce panneau contient la hierarchie des elements de la scene. On peut les faire glisser pour les hierarchiser.
- Properties : ce panneau affiche les propriétés de l'élément sélectionné.

* Certains éléments sont "transformables" (on peut changer leur position, rotation et taille)
* Certains éléments sont "uniques" (on ne peut en mettre qu'un seul sur la scene).

## Outils triés par catégorie
* [Outils](fr_tools.md)
  * [Group](fr_tools.md#group)
  * [Ground Plane](fr_tools.md#ground-plane)

* [Deplacements](fr_move.md)
  * [Spawn point](fr_move.md#spawn-point)
  * [Way point](fr_move.md#way-point)
  * [Floor plan](fr_move.md#floor-plan)
  * [Box collider](fr_move.md#box-collider)

* [Interactions](fr_interactions.md)
  * [Spawner](fr_interactions.md#spawner)
  * [Trigger Volume](fr_interactions.md#trigger-volume)
  * [Link](fr_interactions.md#link)
  * [Media Frame](fr_interactions.md#media-frame)

* [Eclairage](fr_lighting.md)
  * [Skybox](fr_lighting.md#skybox)
  * [Hemisphere light](fr_lighting.md#hemisphere-light)
  * [Ambiant light](fr_lighting.md#ambiant-light)
  * [Directional Light](fr_lighting.md#directional-light)
  * [Spotlight](fr_lighting.md#spotlight)
  * [Point light](fr_lighting.md#point-light)

* [Assets](fr_assets.md)
  * [Model](fr_assets.md#model)
  * [Image](fr_assets.md#image)
  * [Video](fr_assets.md#video)
  * [Audio](fr_assets.md#audio)
  * [Particle Emitter](fr_assets.md#particle-emitter)
  * [Simple Water](fr_assets.md#simple-water)

## Root
- transformable : non
- unique : oui

#### Description
Root est l'élément principal de la scène. Il ne peut ni être déplacé, ni supprimé. On peut cependant le renommer.

#### Options
* Background Color : couleur du fond d'ecran.
* Fog Type : type de brouillard utilisé.
* Override Audio Settings : permet de forcer certains reglages audio prenant la priorité sur les réglages des éléments contenant du son.
