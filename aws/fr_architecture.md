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

### cloudfront
Cloudfront est un systeme permettant la mise en cache de données statiques.
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
