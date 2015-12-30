---
layout: post
title : Qu'est ce que le "cloud computing" ?
author: Olivier Lemaitre
categories: Agile
---

Le nuage informatique réduit drastiquement le coût de stockage, d’échange et de traitement de l'information. 
Avec lui il devient facile de partager les données, de travailler en commun et à distance. 
Il permet aussi à de petites sociétés d’accéder à une puissance jusque-là inaccessible pour elles. 
Certains le voient comme une révolution, un vecteur énorme pour l’innovation. 
Mais comment le définir ? Y a-t-il des risques à l'utiliser ? Qui peut en tirer profit ? 
Pour y répondre cet article reprend des idées du livre “Cloud Computing”<a href='#footnote'>[1]</a> de Guillaume Plouin.

#*Les prémisses du cloud computing*

A la fin des années 1990, les ASP (Application Services Providers), ont proposé aux entreprises de louer des applications hébergées dans leurs centres serveurs. Mais une interface web basique était inadaptée pour un usage quotidien. Cette problématique d'interface utilisateur est la raison principale de leur échec.

Aujourd’hui, les solutions à base de HTML5 (concurrent de Flash d’Adobe et Silverlight de Microsoft) permettent de créer des pages avec une ergonomie qui se rapproche beaucoup de l'interface graphique des applications classiques tout en restant facile à déployer (i.e. Google Docs). C'est ce qu'on appelle le RIA (Riche Internet Application) et c'est ce qui a permis l'émergence des Software as a Service (Saas).

Le cloud ne s’arrête pas à la mise à disposition d’applications. Avec le web est arrivé une nouvelle génération d'hébergeurs qui proposent des plateformes techniques génériques comme OVH, Nexen ou Amen. Ils font partie de la génération des hébergeurs en Self Service qui mettent à disposition une infrastructure pour développer et héberger ses propres applications. Leurs offres ont précédé les environnements d'exécution actuel du Cloud qui sont composés d'Iaas (Infrastructure as a Service) et de PaaS (Plateforme as a Service) dont nous parlerons plus bas. 

#*Une définition du cloud computing*

Il n'existe pas une définition du terme "cloud computing" qui soit admise par tous. Néanmoins les caractéristiques ci-dessous nous permettent de s'en approcher :

- **_La mutualisation des ressources_** : les ressources d'une même machine peut être affectée à plusieurs applications.

- **_L’abstraction sur la localisation_** : l'application est « quelque part » sur l'une des machines constitutives de la plateforme. 

- **_L’élasticité_** : il est possible d'allouer des ressources supplémentaires à une application ou en retirer selon les besoins. 

- **_Le Pay As You Go_** : les utilisateurs paient les ressources qu'ils utilisent en fonction de leur consommation réelle et précise.

- **_Le Self Service_** : l'équipe de développement peut demander l'allocation de ressources via un portail web. Ces ressources seront mises à sa disposition de manière automatique quelques minutes, voire quelques secondes, plus tard.

- **_Les API ouvertes_**: les plateformes ont des interfaces techniques qui permettent de les intégrer au système d'information ou de manipuler les services à distances.

Avec cette définition on voit que le cloud fera évoluer notre mode de consommation de l'informatique : de la possession vers l'usage.

#*Les différents niveaux de services du cloud*

On divise le cloud en trois niveaux de services :

- **_Le SaaS (Software as a Service)_** est un logiciel est fourni sous la forme de service accessible depuis un navigateur. On n'achète pas un logiciel à installer sur une machine mais on loue une application (i.e. Sales Force est un des leader du domaine). Les SaaS s'adressent aux utilisateurs finaux. On y trouve par exemple : Gmail, Google Drive, Drop Box, Salesforce.


- **_La PaaS (Platform as a Service)_**, est une plateforme technique de développement. Les PaaS s'adressent aux développeurs, qui se focalisent sur le code et ne mobilise pas de temps pour installer du matériel et configurer des composants logiciels (i.e. Bases de données distribuées, système de cache, etc). Dans les PaaS on trouve par exemple Google App Engine, Heroku, Engine Yard.


- **_L’IaaS (Infrastructure as a Service)_**. Il s'agit de location de machines virtuelles, permettant d'accueillir base de donnés, serveur d'application, etc. Les IaaS s'adressent donc aux équipes d'exploitation. L'IaaS n'a pas un aussi bon "Time to market" que la PaaS, mais elle permet de mettre en place des architectures qui ne sont pas forcément disponibles sur les plateformes PaaS. Dans la catégorie des IaaS on trouve par exemple Amazon EC2, Google Compute Engine, Windows Azure.

#*La promesse du cloud : la réduction des coûts*

Les clouds arrivent à baisser les coûts grâce à la mutualisation de leur plateforme entre de nombreuses entreprises.

Dans son livre “The Big Switch”, Nicolas Carr explique que de nombreuses entreprises américaines produisaient elles-mêmes leur électricité au début du XXe siècle. Cela leur coûtait cher et elles se sont mises à acheter leur électricité et à se recentrer sur leur cœur de métier (production de voitures et autres biens de consommation). Selon, Nicolas Carr, la même histoire va se reproduire prochainement dans le monde informatique avec le Cloud Computing. 

Même si l’analogie est discutable, le choix du cloud deviendra inévitable pour des raisons de coût.

Pour illuster cela prenons le cas de l'hébergement. Un hébergement de qualité nécessite au moins deux centres de données ains que des salles blanches équipées de climatisation; des armoires de serveurs, des dispositifs de redémarrage à distance ; un système de badges pour sécuriser l'accès; Une redondant pour l'accès à Internet ; une redondance pour l'alimentation éléctrique ; un groupe électrogène et/ou des batteries de secours pour prévenir les coupures d'électricité ; un batiment qui réponde à des normes antisysmiques ; etc. La mutualisation évite aux entreprises de faire cet investissement.

Pour les machines, IBM a montré que beaucoup de serveurs sont utilisés à 20 %, c'est-à-dire que 80 % des factures partent en fumée. Même si les techniques de virtualisation peuvent réduire ces pertes,  elles sont complexes à maîtriser. La mutualisation évite donc d’avoir à rechercher des compétences pointues.

Pour l’exploitation, la réduction des coûts se fait aussi sur sa mutualisation mais aussi par une automatisation accrue des tâches qui sont faites sur les plateformes cloud. 

Enfin pour les logiciels, on constate que dans la pratique l'exploitation d'un logiciel propriétaire (déploiement, monté de version, …) multiplie par quatre son prix d'achat (coût de la licence). C’est le cas des logiciels de la suite bureautique de Microsoft par exemple. Et même si les logiciels Open Source n'ont pas de coût de licence il reste le coût lié à leur exploitation ce qui n’est pas négligeable. En mutualisant ces coûts, le cloud les réduits donc fortement.

#*Est-on en sécurité dans le nuage ?*

Lorsqu'on présente le modèle cloud, on pense tout de suite à la confidentialité des données. Le monde de l'entreprise est encore persuadé que l'on doit conserver ses données dans ses locaux, tout comme on pouvait penser qu'au début du siècle dernier qu’il était plus sûr de garder son argent sous son matelas plutôt que de le mettre à la banque. Même si cette méfiance n'est pas totalement injustifiée (en raison du Patriot Act en particulier), il faut savoir que (comme à l'image des banques), les opérateurs dépensent des fortunes pour assurer la sécurité de leur plateforme.

Avec le  cloud, c’est qu’il existe un unique scénario de sécurité, ce qui est un avantage. En effet, peu importe le lieu d'accès (bureau, domicile,etc), le système de sécurité est le même. Les mesures de sécurité sont donc plus simples gérer. 

Pour la qualité de service, elle est souvent supérieure à celles des entreprises.Les opérateurs garantissent généralement une disponibilité de 99,9 % voire plus.
Si certains acteurs du Cloud (Microsoft et Amazon, par exemple) ont subi des pannes en 2012, on peut les relativiser. Tout comme les catastrophes aériennes, elles sont hypermédiatisées mais l'avion reste le moyen transport le plus sûr. De la même manière, les incidents sur le cloud sont hypermédiatisés mais quand on fait le bilan sur les cinq dernières années, le Cloud est très sûr.


#*Qui peut profiter du nuage ?*

Certains secteurs d'activité sont plus adaptés que d'autres vis-à-vis du cloud :

- La banque a de fortes contraintes réglementaires, le recours au cloud public (Amazon, Google, ...) est donc difficile. Elles ont d'autre part développé de fortes compétences informatiques car c'est dans leur coeur de métier. Passer au cloud signifierait un changement de culture important et poserait des problèmes de reclassement.

- Dans les télécommunications les grands opérateurs (Orange, SFR, ...) se trouvent parfois en concurrence avec les clouds publics. Leurs services informatiques pourraient d'ailleurs devenir les premiers clients de leur offre publique. 

- Dans l'industrie et la distribution, l'informatique est plus vue comme une commodité. Il faut réduire les coûts au maximum. Utiliser le cloud est donc une tendance qui sera plus à l'honneur.

- Dans le secteur du web, utiliser le nuage informatique est naturel, on se pose même pas la question.

On peut aussi découper l'usage selon le type d'entreprise :

- Les PME et les start-up se dirigent naturellement vers le cloud computing. Cela leur évite avant tout un investissement dans des infrastructures informatiques. En particulier quand elles démarrent une activité. Elles bénéficient d'ailleurs beaucoup plus de la mutualisation qu'une grande entreprise, ce qui est très intéressant financièrement.         

Enfin les directions métier au sein d’une entreprise peuvent y voir un intérêt :

Le cloud permet aux utilisateurs de bénéficier de nouvelles applications sans passer par un cycle projet souvent trop long : le cycle projet en V, qui comporte des phases d'étude du besoin, de spécification, de réalisation, de test en enfin de mise production.

Ceci n'est pas adapté à tous les projets. Le cloud permet quant à lui de mettre en oeuvre rapidement des solutions sans passer par ces processus et sans même passer par la direction informatique. Il est en effet fréquent que les services d'exploitation des DSI demandent plusieurs mois pour mettre à disposition de nouvelles machines et les configurer. Avec le cloud, les plateformes sont disponibles en quelques minutes. Les équipes de développement peuvent mettre en production sans attendre plusieurs mois. Ceci améliore le TTM (Time To Market).


#*Pour aller plus loin avec le nuage*

Le nuage informatique permet d’héberger tout ou partie de son informatique, et d’y déployer des applications pour des utilisateurs ou des clients. Mais il peut avoir beaucoup d’autres usages.

Le cloud peut héberger une usine de développement. Si on choisit une PaaS, on dispose d'un environnement opérationnel en seulement quelques minutes, traditionnellement c'est plusieurs semaines.

Le cloud peut héberger des environnements de développement, de test et de recette. Généralement il se passe beaucoup de temps entre leur commande et leur installation dans une organisation classique. Les déployer sur le cloud permet de gagner du temps, d'autant plus que ces environnements ne sont généralement pas pérennes et ne manipulent pas des données critiques.

Le cloud peut servir l'innovation. On peut créer un environnement pour y incuber un projet, réaliser un POC (Proof Of Concept), ou tester de nouvelles fonctionnalités sur une populations réduite d'utilisateurs. Il est intéressant dans ce cas de pouvoir rapidement déployer et facilement suprimer un environnement en utilisant :


- Une plateforme IaaS : dans ce cas, l'infrastructure (machines virtuelles, stockage, réseau) est construite en quelques minutes, mais toutes les étapes d'installation des services, la sauvegarde des bases de données, etc, reste à faire. Ceci ne permet donc pas une mise en ligne immédiate.

- Une plateforme PaaS : dans ce cas, non seulement l'infrastructure est disponible en quelques minutes mais l'installation des services, la sauvegarde régulière de la base, etc, peut se faire automatiquement. Avec une Paas le travail des équipes de production et d'exploitation est réduit au minimum, l'inconvénient c'est qu'il faut entrer dans le standard de la plateforme.

Vous avez maintenant de nombreux éléments sur le nuage informatique. J’espère qu'ils vous permettront de décider si oui ou non vous devez choisir la voie du cloud computing et vous inscrire dans cette révolution.


<div class = 'footnote-list'>
	<div id = 'footnote'>
	<span>1: </span>
	<a href="http://www.amazon.fr/Cloud-Computing-S%C3%A9curit%C3%A9-strat%C3%A9gie-dentreprise/dp/2100598759/ref=sr_1_1?s=books&ie=UTF8&qid=1411145325&sr=1-1&keywords=cloud+computing">
	Cloud Computing - 3e éd. : Sécurité, stratégie d'entreprise et panorama du marché </a> (Juin 2013), 
	par Guillaume Plouin
	       
	</div>
</div>