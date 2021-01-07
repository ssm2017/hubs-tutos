# Elements Spoke
Spoke permet de créer des "scenes" pouvant être utilisées dans hubs.

La partie droite de l'ecran principal de spoke contient 2 parties :
- Hierarchy : ce panneau contient la hierarchie des elements de la scene. On peut les faire glisser pour les hierarchiser.
- Properties : ce panneau affiche les propriétés de l'élément sélectionné.

* Certains éléments sont "transformables" (on peut changer leur position, rotation et taille)
* Certains éléments sont "uniques" (on ne peut en mettre qu'un seul sur la scene).

## Outils triés par catégorie
* [Outils](fr_tools.md)
* [Deplacements](/spoke/elements/fr_move.md)
* [Interactions](/spoke/elements/fr_interactions.md)
* [Eclairage](/spoke/elements/fr_lighting.md)
* [Assets](/spoke/elements/fr_assets.md)

## Root
- transformable : non
- unique : oui

#### Description
Root est l'élément principal de la scène. Il ne peut ni être déplacé, ni supprimé. On peut cependant le renommer.

#### Options
* Background Color : couleur du fond d'ecran.
* Fog Type : type de brouillard utilisé.
* Override Audio Settings : permet de forcer certains reglages audio prenant la priorité sur les réglages des éléments contenant du son.
