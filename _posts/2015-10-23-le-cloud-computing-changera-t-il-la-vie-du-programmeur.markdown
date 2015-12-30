---
layout: post
title : Le Cloud Computing changera-t-il la vie des programmeurs ?
author: Olivier Lemaitre
categories: Cloud
---

On pourrait penser que l’émergence du cloud computing ne devrait pas réellement avoir d’impact sur les développeurs.
En effet, cela n’a pas d’importance que le serveur d’applications soit sur un serveur au sein de l'entreprise ou dans le datacenter d'un opérateur cloud. Quand les tests passent, peu importe où et comment l’application est déployée. Pourtant nous allons voir que le cloud computing va affecter de manière très significative le développement logiciel.
Voici quelques impacts tirés du livre "Cloud Computing for Programmers"<a href='#footnote'>[1]</a> de Daniele Casal.

#**Plus besoin d'attendre**

Tout d'abord grace à la virtualisation, les programmeurs n’ont pas besoin d’attendre qu’un serveur physique soit configuré ou qu’il devienne libre. 
À la place, ils peuvent provisionner les serveurs dont ils ont besoin eux-même et rapidement.

Ils sont alors capables de créer autant d'instances que nécessaires et ainsi augmenter leur capacité à innover. Si une caractéristique ou un scénario a l’air intéressant, une équipe peut produire un environnement de développement rapidement pour coder et tester. Cette approche est très “agile” et encourage l’expérimentation.Il n’y a pas besoin d’attendre le prochain “build” ou la prochaine version comme c’est le cas quand un nombre limité de serveurs physiques sont disponibles.

De ce fait le développeur se sentira plus efficace. Et avec le logiciel qui augmente en importance et qui tend à dominer l'économie, l’efficacité du développeur deviendra bientôt un facteur déterminant pour la compétitivité de l’entreprise.

#**Moins de configurations, plus de création de valeur**

Les outils de gestion du code source, d’intégration continue, d'automatisation des tests, etc, existaient bien avant l’émergence du cloud. Ils suppriment beaucoup des tâches routinières des développeurs. Seulement ces outils sont souvent difficiles à configurer et à gérer au quotidien. Sur le cloud, ils sont disponibles comme des offres SaaS (Software as a Service) et sont beaucoup plus simples à configurer et à utiliser. Bien souvent, il n'y rien à installer, un ordinateur et une connexion internet suffit pour démarrer.

Pourquoi alors gaspiller du temps à configurer un outil d’intégration continue ou des serveurs, alors que vous pourriez passer ce temps à produire de la valeur en écrivant du code pour le livrer à l'utilisateur ?  Voici une liste non exhaustive de services dont peut disposer un développeur dans le cloud :

- L'IDE (environnements de développement intégré). Il permet aux développeurs d’éditer et coder. Avec la version SaaS c'est possible depuis n’importe quel ordinateur connecté à internet. On trouve par exemple : Koding, Cloud9 IDE, Codeanywhere, Codenvy, ShiftEdit.

- Le contrôle de version / gestion de code source. Il permet entre autres de partager son code et de gérer les différentes versions, on trouve aujourd'hui : GitHub, CloudForge, BitBucket, Mercurial, Fossil, Kiln, Jira Studio, Dev@Cloud, Code2Cloud, Google Code

- L'intégration continue. Avec ce type de plateforme, le programmeur peut detecter les bugs plus tot dans l'ensemble de l'application. On trouve : TeamCity, Travis CI, Shining Panda, CircleCI, FaZend, Hosted CI.

- Les tests fonctionnels souvent complexes à mettre en place, peuvent etre assurés par des plateformes qui vont par exemple tester des scénarios utilisateurs sur des interfaces graphiques. Les bons exemples sont: SauceLabs, uTest, Mob4Hire.

- Les tests de stress/Performance. Quand une application doit supporter un fort trafic, ces plateformes vont le simuler et apporter les metrics qui permettront son optimisation. On trouve par exemple : LoadStorm, BlazeMeter, HP Load Runner in the Cloud, Neustar

- La collaboration. Les développeurs travaillent rarement seuls sur un produit. Pour communiquer avec les autres développeurs parfois répartis à différents endroits sur la planète, il existe des outils en ligne comme : Confluence, Green hopper, Crucible, VMware Zimbra, 

- La supervision qui est un outil de plus en plus indispensable pour détecter, voire anticiper des bugs sur l'application. On trouvera entre autres Pingdom, Monitor.us.

#**Des nouveaux langages de programmation**

On constate une prolifération des nouveaux langages de programmation (Clojure, Go, Dart, Scala, F#, Ceylon, X10, etc) et certains sont en train de rapidement gagner en popularité dans la communauté des développeurs. Est-ce que le cloud a quelque chose à voir avec ça ? Oui très certainement.

Programmer pour le cloud signifie programmer dans un environnement distribué (multimachines). Dans ces environnements le flux des programmes est parallèle, asynchrone et doit réagir aux évènements extérieurs. Les développeurs ont alors besoin de basculer du modèle de la programmation séquentielle à celui de la programmation distribuée et asynchrone. L'arrivée du cloud computing force cette transformation. 

Ecrire, debugger et maintenir du code parallèle et asynchrone est très difficile. C''est pour cette raison qu'il existe des nouveaux outils, des bibliothèques et des nouveaux langages de programmation pour le faciliter.

Le langage idéal pour l’air du cloud doit être orienté objet et embrasser la programmation fonctionnelle. L’avantage de la programmation orientée objet est bien connue et établie, c’est la manière dont nous comprenons et modélisons le monde. Le bénéfice de la programmation fonctionnelle quant à lui peut être résumé en une phrase : ce style de programmation permet d’écrire du code sans effet de bord, idéal pour les systèmes concurrents, hautement disponibles, critiques et distribués.

Toutefois, les langages de programmation “purement” fonctionnels n’ont pas beaucoup de succès, parce qu’ils sont considérés comme impraticables pour le développement logiciel au quotidien. En réalité, beaucoup de langages incorporent des éléments fonctionnels sans vraiment adhérer au dogme fonctionnel dans sa forme la plus pure.
Par exemple C# a des closures et des lambdas depuis la version 3.0 tout comme Javascript et Python. Cette approche consistant à combiner les éléments de l’orienté objet et de la programmation fonctionnelle est appelée multiparadigme. Le programmeur cloud devra donc bien connaitre les deux mondes.


#**Des nouvelles architectures applicatives**

Apprendre de nouveaux langages ne suffira peut-être pas. Le fait que les applications vont changer d’échelle (scale) de manière élastique (ajouter ou enlever des machines) va changer la façon que les développeurs ont de résoudre les problèmes de programmation les plus complexes. Ils devront “grandir” acquérir les compétences nécessaires pour écrire des logiciels pour des systèmes parallèles, multi-CPU et asynchrones que le cloud apporte et sortir des architectures monolithiques. 

D'un autre côté les réseaux sociaux, l'internet des objets, etc feront augmenter les données de manière exponentielle. Ils devront aussi être à l’aise avec le BigData, les bases non relationnelles (NoSQL), et apprendre les plateformes de traitement distribué des données comme Hadoop.


#**Adoption de la culture DevOps**

Typiquement, en particulier dans les grandes entreprises, le processus de déploiement prend beaucoup trop de temps. Quand vous avez une bureaucratie interne qui demande des signatures, vous avez de nombreuses fonctions entre le développement et les opérations qui créent une inertie. En fait, dans les grandes entreprises, le cloud computing est vu en partie comme une manière de “soudoyer” cette bureaucracie dit Rod Johnson, fondateur de SpringSource, qui a sa propre PAAS (CloudFoundry).

Le terme “DevOps” remet en cause la séparation entre le développement du logiciel et son exploitation. D'un côté les développeurs désireux d’implémenter et de livrer leur produit. D'un autre côté du personnel informatique concentré pour garder le système en état de marche (“up and running”). Cette focalisation pour maintenir la disponibilité et éviter les pannes a créé des équipes opérationnelles par tradition réticente au changement. Il devient vital pour l'entreprise d'avoir des développeurs et des opérationnels qui travaillent ensemble dans un but commun et le cloud computing va accentuer cette vision de l'organisation. A noter que certaines organisations peuvent de jamais faire la transition et auront probablement de sérieux problèmes.

Plus de 90% des gens, dans une enquête du Forrester Research en 2012, ont dit que le cloud était la façon la plus rapide d’avoir un projet abouti et déployé.


**Conclusion**

Quand on parle de cloud computing on pense souvent aux compétences opérationnelles : machines virtuelles, réseau, disque, etc. 
En réalité, le cloud est avant tout un outil formidable pour les programmeurs. Un outil qui leur changera la vie et qui leur permettra, moyennant quelques investissements, de créer les applications de demain. Il leur donne le pouvoir de mettre rapidement des applications en production et dimensionnables ("scalables") à la demande. Ceci va mécaniquement créer de nombreuses opportunités d'emploi. On peut s'attendre d'ailleurs à ce que, dans une entreprise orientée cloud, la demande pour des développeurs restera élevée et qu'inversement un développeur orienté cloud aura certainement plus de demandes que les autres. N'hésitez donc pas à vous y préparez dès maintenant.




<div class = 'footnote-list'>
  <div id = 'footnote'>
    <span>1: </span>
      <a href="http://www.amazon.com/Cloud-Computing-Programmers-Daniele-Casal-ebook/dp/B00CH9QG8C">Cloud computing for programmers</a> de Daniele Casal
  </div>
</div>