[Retour AWS](../aws/Readme.md) | [Retour début](/fr_index.md)
## Supprimer les parametres smtp
 * aws console -> systems manager -> parameter store
 * supprimer tout ce qui a lien à l'email
 * aws console -> ec2
 * terminer l'instance et attendre qu'une nouvelle soit créee
 
## Connaitre son id utilisateur
 * ouvrir la console de developpeur dans le navigateur
 * rejoindre une room
 * regarder le parametre : "Logged into account 883810902967582892" dans la console

## Allumer / Eteindre le stack
 * Aller dans "cloudformation" https://eu-west-1.console.aws.amazon.com/cloudformation/home dans la region où se trouve le stack (Irlande)
 * selectionner le stack "root" (tout en bas) et cliquer sur le bouton "update"
 * cliquer sur "suivant" quand le site demande le template/modele
 * sur la page suivante (details), descendre jusqu'à "offline mode" et choisir "online" pour allumer et "offline" pour éteindre
 * suivant
 * suivant
 * mettre les coches en bas puis valider
 * attendre 5mn que l'update soit terminé

## Temps

### Update du stack
env 5mn

### Deploiement nouvelle version du client
env 7mn
