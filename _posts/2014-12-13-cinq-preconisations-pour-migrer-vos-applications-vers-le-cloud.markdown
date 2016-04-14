---
layout: post
title: Cinq préconisations pour migrer vos applications vers le cloud
author: Olivier Lemaitre
categories: Cloud
---

Les entreprises hésitent encore à migrer leurs applications dans le nuage informatique. 
Elles ont certainement raison car ce n'est pas un simple déplacement d'une machine vers une autre. 
Vous trouverez dans cet article ce qu'il est important de savoir avant de franchir le pas. 
Ces informations sont extraites du livre : “Architecting the Cloud”. <a href='#footnote'>[1]</a>

#1 - Prévoyez de réarchitecturer vos applications

Très peu d’applications sont de bonnes candidates au déplacement vers le nuage informatique avec leur architecture actuelle. 
Même si le modèle de "pay-as-you-go" promet la réduction des coûts d'infrastructure IT, c’est seulement vrai si le logiciel 
est architecturé pour optimiser l’utilisation des services cloud.

Pour comprendre, il faut saisir une composante clé du cloud computing : l’élasticité. 
Cette propriété permet d'augmenter ou de réduire le nombre de ressources informatiques (e.g. le nombre de serveurs) dont à besoin l'application. 
C'est très pratique pour gérer des piques de charge.

Seulement pour qu’un logiciel soit vraiment élastique, c’est à dire capable de changer d’échelle vers le haut comme vers 
le bas il doit être architecturé avec un couplage lâche. Ainsi les "services cloud" doivent être des services "stateless". 
Ceci favorise l'utilisation des principes REST et en particulier l'utilisation des services hypermédia qui stockent l'état 
de l'application côté client plutôt que côté serveur.

Assurez-vous donc que les architectes ont une bonne compréhension des différences entre des services 
avec état (statefull) et sans état (stateless). Pour certaines applications, l’hébergement ou la réécriture et parfois une meilleure option 
que le déplacement vers le nuage. Apprenez à les identifier.

Un autre point souvent méconnu, les architectures cloud reposent sur des transactions 
BASE (Basically Available, Soft State, Eventually Consistent - Basiquement Disponible, Etat Souple, Finalement cohérent) par opposition aux transactions 
ACID (Atomique, Cohérente, Isolée, Durable).
Beaucoup d’applications légataires n’ont pas été conçues pour gérer une cohérence finale et cela peut potentiellement frustrer l’utilisateur 
si son application est simplement portée sur le cloud sans adresser ce problème.    


#2 - Mettez la sécurité au coeur des applications

Les opérateurs du nuage informatique fournissent typiquement un haut niveau de sécurité sur leur périmètre. 
Néanmoins, il revient à l’entreprise utilisatrice de construire le niveau approprié de sécurité pour ses applications. 

Par exemple, une fournisseur d’Infrastructure as a Service (IaaS) comme Amazon Web Service (AWS) possède des datacenters 
avec une sécurité de classe internationale, des livres blancs sur comment construire des services très sécurisés sur sa plateforme, 
et des interfaces programmatiques (API) qui facilitent la conception pour la sécurité. 
Toutefois, c’est à l’architecte qui construit le logiciel sur AWS de chiffrer les données, gérer les clés, 
implémenter la bonne politique pour les mots de passe, etc.

Commencez par vous assurer que les architectes, l’équipe produit, et les professionnels de la sécurité ont une large compréhension de la sécurité 
dans le cloud. Si nécessaire, faire appel à un tiers indépendant pour procéder à une évaluation et effectuer des vérifications avant et après le déploiement.  

Il y a un mythe commun, celui que les données critiques ne peuvent pas être en sécurité dans le cloud. 
La réalité c’est que la sécurité doit être architecturée dans le système, que les données soient dans le cloud ou ailleurs.


#3 - Criptez vos données

Même si l'application est sécurisée, on craint souvent le Patriot Act. Ce dernier permet aux Américains, en cas de soupçon de terrorisme, 
d'avoir accès aux données qui se trouvent dans les datacenters des entreprises américaines partout dans le monde et ce sans prévenir leur propriétaire.

Toutefois, si une société crypte ses données, le gouvernement devra demander à l’entreprise de les décrypter pour les inspecter. 
Crypter ses données est le meilleur moyen pour réduire le risque qu'on vous les demande et invalide complètement le mythe que les données 
critiques ne peuvent pas vivre dans le nuage.

L’encryptage est donc le meilleur moyen pour se protéger du patriot act et des autres politiques de surveillance gouvernementales présentent 
dans beaucoup de pays.
    
#4 - Ne surestimez pas votre propre SLA (Service Level Agreement)

Les sociétés comme Amazon Web Services ont investi des millions de dollars dans leurs datacenters. 
Ils ont recruté parmi les meilleures personnes du monde pour y travailler. 
En choisissant de construire son propre cloud privé dans son propre datacenter pour satisfaire un désir de contrôle, 
les consommateurs parient qu’ils peuvent fournir des meilleurs SLA que les fournisseurs de cloud.

Sachez que, même s'il arrive que les datacenters des fournisseurs de cloud comme Amazon connaissent des pannes, elles sont très rares. 
De plus, ces pannes sont arrivées jusqu'à présent dans une unique zone de disponibilité. 
Ainsi, les entreprises qui ont construit leurs applications avec une redondance sur de multiples zones sont restées disponibles.


#5 - Ne négligez pas les besoins métier

Ayez des attentes réalistes. Découper les projets en petits livrables pour délivrer de la valeur métier le plus tôt possible et permettre 
à l’équipe d’apprendre au fur et à mesure. 
N’essayez pas l’approche big-bang où l’équipe s’engage pour plusieurs mois ou pour une année avec l’espoir de livrer un grand nombre de nouveaux services dans le cloud.

Comprenez la différence entre les 3 modèles de service cloud : SaaS, PaaS et IaaS. Sachez dire quels cas métier sont les mieux adaptés pour chaque modèle de service.
Comprenez les besoins du métier et les attentes des clients avant de sélectionner le modèle de service cloud et le type de cloud. 
Les besoins guident les décisions; les décisions ne doivent pas piloter les besoins.         


<div class = 'footnote-list'>
  <div id = 'footnote'>
    <span>1: </span>
      <a href="http://www.amazon.fr/Architecting-Cloud-Decisions-Computing-Service/dp/1118617614/ref=sr_1_sc_1?ie=UTF8&qid=1414685962&sr=8-1-spell&keywords=architeting+the+cloud">
      Architecting the Cloud: Design Decisions for Cloud Computing Service Models (SaaS, PaaS, and IaaS) 
      </a>
      par Michael J. Kavis 
           
  </div>
</div>       


    		