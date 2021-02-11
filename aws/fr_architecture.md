[Retour AWS](../aws/Readme.md) | [Retour début](/fr_index.md)
## Bases aws
Si on veut monter un serveur "on premise" (hebergé sur une machine virtuelle ou bare metal), il faut installer tout ce qu'il faut et le gérer soi même.

Aws permet de monter un serveur mais en le découpant en morceaux et les reliant entre eux. Par exemple, le mail est géré par un service amazon, le stockage disque un autre service, etc...

Un serveur sur aws est l'ensemble de la mise en relation de plusieurs services.

Les services sont gérés par "region" donc on peut tres bien avoir une base de données en Irlande et une autre en Virginie du nord.

la gestion des services se fait depuis la [console aws](https://eu-west-1.console.aws.amazon.com/console)

## Hubs cloud aws architecture
Voici l'architecture de hubs cloud selon leur doc :

![hubs cloud aws architecture](https://hubs.mozilla.com/docs/img/hubs-cloud-aws-architecture.jpeg)

Nous allons tenter de voir les significations de chaque service.

Selon leur doc :

Quand vous créez un stack(pile), un nouveau VPC est créé avec deux sous réseaux public.

Hubs cloud sur AWS met en place deux groupe d'auto-scaling, un pour les serveurs d'application et un pour (optionnel) les serveurs de stream.
Les serveurs sont autobalancés entre deux AZ.
Les serveurs d'application fournissent les fonctionnalités de l'application centrale et des serveurs de stream peuvent être ajoutés pour augmenter les ressources pour la voix et le streaming de vidéo.

AWS Cloudfront est configuré pour la mise en cache du contenu et AWS lambda est utilisé pour plusieur fonctions comme le redimentionnement d'images, l'encodage video et les miniatures sur le site web.

Quand vous configurez votre stack, vous pouvez aussi optionnellement activer une application de répartition de charge pour basculer entre plusieurs serveurs. Si vous n'utilisez pas un ALB, une repartition de charge DNS round robin est alors utilisée.

AWS simple email service est utilisé pour les emails tant que vous ne configurez pas un serveur SMTP personnalisé.

Les assets uploadés sont stockés sur un Elastic FIle Store et les assets statiques (JS/CSS/Images) sont stockés sur S3. La base de données est du PosgreSQL compatible avec AWS aurora serverless qui sera mise en pause si non utilisée sauf si vous le désactivez dans les reglages de configuration.

Les mots secrets de la configuration sont stockés dans AWS secrets manager tant que les parametres de AWS Parameter store sont des chaines chiffrées.

Les données dans EFS et RDS sont stockées chiffrées (encrypted-at-rest)

### cloudfront
Amazon CloudFront est un réseau rapide de diffusion de contenu (CDN) qui distribue en toute sécurité des données, des vidéos, des applications et des API à vos utilisateurs, avec une faible latence et des vitesses de transfert élevées, le tout dans un environnement convivial pour les développeurs.
 * [Page de présentation](https://aws.amazon.com/fr/cloudfront/)
 * [Page d'administration](https://console.aws.amazon.com/cloudfront)

### API gateway
Amazon API Gateway est un service entièrement opéré, qui permet aux développeurs de créer, publier, gérer, surveiller et sécuriser facilement des API à n'importe quelle échelle.
 * [Page de présentation](https://aws.amazon.com/fr/api-gateway/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/apigateway)

### Lambda
AWS Lambda est un service de calcul sans serveur qui vous permet d'exécuter du code sans provisionner ou gérer des serveurs, créer une logique de dimensionnement de cluster prenant en charge la charge de travail, maintenir les intégrations d'événements ou gérer les environnements d'exécution.
 * [Page de présentation](https://aws.amazon.com/fr/lambda/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/lambda)
 
### Certificate
AWS Certificate Manager est un service qui vous permet de mettre en service, de gérer et de déployer facilement des certificats Secure Sockets Layer/Transport Layer Security (SSL/TLS) afin de les utiliser avec les services AWS et vos ressources internes connectées.
 * [Page de présentation](https://aws.amazon.com/fr/certificate-manager/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/acm)

### Secrets
AWS Secrets Manager vous aide à protéger l'accès à vos applications, services et ressources informatiques. Ce service vous permet de facilement gérer, récupérer et faire alterner des informations d'identification de base de données, des clés d'API et d'autres secrets au cours de leur cycle de vie.
 * [Page de présentation](https://aws.amazon.com/fr/secrets-manager/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/secretsmanager)

### Budgets
AWS Budgets vous permet de définir des budgets personnalisés afin d'être alerté lorsque votre utilisation ou vos coûts dépassent (ou sont sur le point de dépasser) le montant prévu.
 * [Page de présentation](https://aws.amazon.com/fr/aws-cost-management/aws-budgets/)
 * [Page d'administration](https://console.aws.amazon.com/billing/home#/budgets)
 
### Application load balancer
Elastic Load Balancing répartit automatiquement le trafic entrant d'application sur plusieurs cibles, comme les instances Amazon EC2, les conteneurs, les adresses IP, les fonctions Lambda et les appliances virtuelles.
 * [Pagde de présentation](https://aws.amazon.com/fr/elasticloadbalancing)
 * Page d'administration non trouvée

### Simple email service
Amazon Simple Email Service (SES) est un service de messagerie électronique rentable, flexible et évolutif qui permet aux développeurs d'envoyer des messages à partir de n'importe quelle application.
 * [Page de présentation](https://aws.amazon.com/fr/ses/)
 * [Page d'administration](https://console.aws.amazon.com/ses)

### Efs
Amazon Elastic File System (Amazon EFS) est un système de stockage de fichiers NFS simple, évolutif, élastique et entièrement géré qui s’utilise avec AWS Cloud Services et les ressources sur site.
 * [Page de présentation](https://aws.amazon.com/fr/efs/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/efs)
 
### S3
Amazon Simple Storage Service (Amazon S3) est un service de stockage d'objet offrant une évolutivité, une disponibilité des données, une sécurité et des performances de pointe.
 * [Page de préseentation](https://aws.amazon.com/fr/s3/)
 * [Page d'administration](https://s3.console.aws.amazon.com/s3)

### Rds
Amazon Relational Database Service (Amazon RDS) vous permet d'installer, de gérer et de mettre à l'échelle facilement une base de données relationnelle dans le cloud.
 * [Page de présentation](https://aws.amazon.com/fr/rds/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/rds)

## Autres services
Ces autres services sont utilisé mais non listés sur le schema.

### Ec2
Amazon Elastic Compute Cloud (Amazon EC2) est un service Web qui fournit une capacité de calcul sécurisée et redimensionnable dans le cloud.
 * [Page de présentation](https://aws.amazon.com/fr/ec2)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/ec2)

### Iam
AWS Identity and Access Management (IAM) vous permet de contrôler de façon sécurisée l'accès aux services et ressources AWS.
 * [Page de présentation](https://aws.amazon.com/fr/iam)
 * [Page d'administration](https://console.aws.amazon.com/iam)

### Licence
AWS License Manager facilite la gestion des licences sur AWS et sur les serveurs sur site pour des fournisseurs de logiciels comme Microsoft, SAP, Oracle et IBM. AWS License Manager permet aux administrateurs de créer des règles de licence personnalisées qui imitent les termes de leurs accords de licence, et puis d’appliquer ces règles lors du lancement d'une instance d'EC2.
 * [Page de présentation](https://aws.amazon.com/fr/license-manager/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/license-manager)

### Marketplace
AWS Marketplace est un catalogue numérique contenant des milliers de listes de logiciels créés par des prestataires indépendants.
 * [Page de présentation](https://aws.amazon.com/marketplace)
 * [Page d'administration](https://console.aws.amazon.com/marketplace)

### Organizations
AWS Organizations vous aide à gérer et à contrôler votre environnement de manière centralisée à mesure que vous développez et mettez à l'échelle vos ressources AWS.
 * [Page de présentation](https://aws.amazon.com/fr/organizations/)
 * [Page d'administration](https://console.aws.amazon.com/organizations)

### Route 53
Amazon Route 53 est un service Web de système de noms de domaine (DNS) dans le cloud hautement disponible et évolutif.
 * [Page de présentation](https://aws.amazon.com/fr/route53/)
 * [Page d'administration](https://console.aws.amazon.com/route53)

### VPC
Amazon Virtual Private Cloud (Amazon VPC) vous permet de mettre en service une section du cloud AWS qui a été isolée de manière logique et dans laquelle vous pouvez lancer des ressources AWS dans un réseau virtuel que vous définissez.
 * [Page de présentation](https://aws.amazon.com/fr/vpc/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/vpc)

### Cloud formation
AWS CloudFormation est un moyen simple de modéliser une collection de ressources AWS et tierces, de les allouer rapidement et de manière cohérente, et de les gérer tout au long de leur cycle de vie grâce au traitement de l'infrastructure en tant que code (Infrastructure as Code).
 * [Page de présentation](https://aws.amazon.com/fr/cloudformation/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/cloudformation)

### Systems
Avec AWS Systems Manager, vous bénéficiez d'un maximum de visibilité et de contrôle sur votre infrastructure sur AWS. Systems Manager fournit une interface utilisateur unifiée qui vous permet d'afficher les données opérationnelles de plusieurs services AWS et d'automatiser les tâches opérationnelles pour vos ressources AWS.
 * [Page de présentation](https://aws.amazon.com/fr/systems-manager/)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/systems-manager)

### Quotas
Votre compte AWS dispose de quotas par défaut, anciennement appelés limites, pour chaque service AWS. Sauf indication contraire, chaque quota est spécifique à la région. Vous pouvez demander des augmentations pour certains quotas, et d'autres quotas ne peuvent pas être augmentés.
 * [Page de présentation](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html)
 * [Page d'administration](https://eu-west-1.console.aws.amazon.com/servicequotas)

### Workmail
Amazon WorkMail est un service de messagerie et de calendrier professionnel, sécurisé et géré, qui prend en charge les applications clientes de messagerie de bureau et mobile existantes.
/!\ Gratuit 30 jours pour 25 utilisateurs puis payant (4€/utilisateur/mois)
 * [Page de présentation](https://aws.amazon.com/fr/workmail)
 * [Page d'administration](https://console.aws.amazon.com/workmail/)

### Support
[Page de support](https://console.aws.amazon.com/support)
