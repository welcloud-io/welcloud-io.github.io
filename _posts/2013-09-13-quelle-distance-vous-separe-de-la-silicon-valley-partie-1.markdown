---
layout: post
title : Quelle distance vous sépare de la Silicon Valley ? (Partie 1)
author: Olivier Lemaitre
categories: Agile
---

Personne ne peut contester la suprématie des géants de la Silicon Valley (Google, Amazon, Facebook, etc). 
Un succès qui est fortement lié à la maitrise qu'ils ont de l'outil informatique.
Mais comment font-ils pour atteindre cette efficacité ? Quelles méthodes utilisent-ils ? Nos entreprises en sont-elles si éloignées  ?
Vous trouverez ici des pistes de réponses inspirées du livre : « Les Géants du Web »<a href='#footnote'>[1]</a>.

Pour commencer les géants du web construisent eux-même leurs logiciels pour les raisons suivantes :

- c'est leur cœur de métier, ils ne peuvent donc pas laisser à des tiers ce qui permet de les distinguer de la concurrence.

- le trafic qu’ils doivent absorber (i.e. le volume de transactions à exécuter en simultané) est énorme. 
Or les logiciels vendus sur étagère (les progiciels) sont souvent « hyper-génériques » pour pouvoir s’adapter à différents contextes, donc peu performants. 
En fabriquant leurs logiciels ils peuvent optimiser les performances dont l'expérience utilisateur dépend. Quelques dixièmes de seconde de latence 
dans le chargement des pages peuvent réduire significativement leur chiffre d'affaires.

- le coût des progiciels augmente avec la puissance nécessaire à leur exécution (certains progiciels sont facturés au cœur de processeur par exemple). 
Avec des logiciels « faits maison » ou open source le problème ne se pose pas. Les géants du web contribuent d'ailleurs beaucoup au logiciel libre.

      
      
Néanmoins, construire des logiciels est un art difficile. 
Pour cette raison ils recrutent des développeurs d'un très bon niveau. 
Ils les forment, leur donnent une grande autonomie, un cadre de travail agréable et une forte rémunération. 
En contrepartie on leur demande une qualité extrême du code, gage de souplesse et de fiabilité.
      
Pour constituer les équipes, les géants de la silicon valley combinent trois principes d'organisation :
        
- l'organisation en « pizza team » ou « équipe pizza ». C'est une équipe qui ne  doit pas dépasser le nombre de personnes que l’on peut nourrir avec 2 pizzas (ce qui correspond à 8 personnes pour des pizzas au format américain). Il est en effet prouvé qu’une équipe est  efficace entre 5 et 12 personnes, en dehors de ces limites des problèmes apparaissent.

- l'organisation en  « feature team »  ou « équipe fonctionnelle » qui, plutôt que de regrouper les équipes par couches technologiques (e.g.  tous les experts html en front office, tous les experts java en back office, etc), on les regroupe par ensembles fonctionnels cohérents avec un expert de chaque couche dans l’équipe. On évite ainsi de passer du temps à coordonner les couches. Régulièrement les experts des différentes équipes se réunissent pour échanger sur leurs pratiques.

- l'organisation « devops » qui regroupe les développeurs (qui ont pour objectif d’innover) et les opérationnels (qui ont pour objectif de rationnaliser les coûts). Le but est de les fédérer autour d’un but commun. Il y a donc au moins un opérationnel dans chaque « feature team ».
        
On obtient alors des petites équipes pluridisciplinaires entièrement responsables du bon fonctionnement du service à fournir au client.
      
      
Pour faire émerger les meilleures idées ils utilisent :
        
- le « Lean Startup » qui permet de mettre rapidement en route un projet ou plutôt un « business ». Il est basé sur la boucle « Build – Mesure – Learn » (Construire – Mesurer – Apprendre). Pour que cela fonctionne il faut une « obsession de la mesure » et savoir collecter toutes les données qui guideront efficacement les décisions.

- le MVP (« Mininum Viable Product » ou « Produit Minimum Viable »), qui est une technique du « lean startup ». Il doit permettre de valider 
au plus tôt les hypothèses. Ceci évite de les faire dans une salle de réunion et de se rendre compte après des mois qu’elles sont fausses. 
En résumé le MVP est une version du produit qui permet à une équipe de collecter à propos du client un maximum d'enseignements validés avec le minimum d’efforts.
        
Pour supporter ces cycles très courts d’amélioration continue ils utilisent des pratiques techniques :
        
- le déploiement continu (une extension de l’intégration continue) se fait en production de manière automatisée ou semi-automatisée au 
minimum 1 fois par jour. Ceci a un double avantage : un « feed back » rapide sur les 
nouvelles fonctionnalités (donc en phase avec le  « lean startup ») et une correction plus 
rapide et facile des anomalies. En effet, les petits changements créent de bien plus petits problèmes 
que les gros changements. A noter que cette pratique nécessite l’automatisation des tests à tous les niveaux (unitaires, intégration, performance, …).

- le « feature flipping » quant à lui permet de limiter les risques du déploiement continu en permettant d’activer ou de désactiver des fonctionnalités directement en production sans avoir à relivrer du code.

- Enfin, l’« A/B testing » permet lui aussi d'activer ou désactiver des fonctionnalités pour un groupe d’utilisateurs. Ceci permet d’expérimenter une fonctionnalité en production sans la rendre visible à tous et d’étudier les différents comportements.
  
La société la plus représentative des pratiques ci-dessus est Facebook. 
Elle automatise énormément ses tests et effectue deux déploiements par jour. 
Les fonctionnalités qui vont sortir dans plusieurs mois sont déjà en production mais pas toujours visibles 
par l’utilisateur grâce au « feature flipping » ou l'« A/B testing ».
      
Enfin l’infrastructure qui supporte leurs logiciels joue un rôle important. Cette thématique fera l’objet d’un <a href="/cloud/2013/09/20/quelle-distance-vous-separe-de-la-silicon-valley-partie-2">autre article</a>.
      
      
Les géants du web ont donc choisi d’avoir la main sur leurs logiciels, de recruter de bons développeurs et de les organiser en petites équipes autonomes qui valident rapidement leurs idées en livrant souvent en production. 
La conséquence c'est tout simplement un meilleur « time to market ».
Pour savoir si votre entreprise s'en approche, essayez simplement de répondre à cette question : 
« combien de temps met aujourd’hui votre organisation pour mettre en production la modification d’une seule ligne de code ?», 
plus la réponse s'éloigne d’une journée plus vous vous éloignez de l’efficacité des géants de la Silicon Valley.
      

<div class = 'footnote-list'>
  <div id = 'footnote'>
    <span>1: </span>
      <a href="http://www.octo.com/fr/publications/11-les-geants-du-web">« Les géants du web »</a>, par <a href='http://www.octo.com/fr'>Octo Technology</a> (Novembre 2012)
    
  </div>
</div>


