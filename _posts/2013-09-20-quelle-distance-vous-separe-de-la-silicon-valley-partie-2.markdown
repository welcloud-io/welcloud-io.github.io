---
layout: post
title : Quelle distance vous sépare de la Silicon Valley ? (Partie 2)
author: Olivier Lemaitre
categories: Cloud
---

Pour supporter un très gros volume de requêtes sur le web une seule machine ne suffit pas. 
Les sociétés de la Silicon Valley comme Google ou Facebook  possèdent donc une infrastructure adaptée à ce très fort trafic. 
Mais comment est elle construite ? Comment et par qui est elle gérée ? Peut on nous-même en disposer ?
Nous apporterons ici des éléments de réponse inspirés des livres : « Les géants du web »<a href='#footnote'>[1]</a>, et 
« What is DevOps ?»<a href='#footnote'>[2]</a>.

Les géants du web ont parfaitement séparé la partie logicielle de la partie matérielle au point qu’ils ont intégré 
une catégorie d'opérationnels (les ops) dans les équipes de développement. Ce qui, il faut le souligner, est une pratique très rare dans la majorité 
des entreprises.

Il y a deux catégories d’opérationnels :
ceux qui, par exemple, remplacent les disques durs défectueux ou installent un nouveau firewal et ceux qui construisent 
les environnements de développement. Ces derniers vont par exemple créer l’instance d’une machine virtuelle, la provisionner 
(en mémoire, en espace disque, ...) et y installer les conteneurs 
nécessaires (serveurs d'aplications, bases de données, ...) pour que les développeurs y déposent leur code.
C’est cette seconde catégorie qui se retrouve dans l’équipe de développement 
et qui automatise au maximum ses tâches, on parlera alors d’Infrastructure as Code (IaC). 
Les opérationnels qui gèrent le matériel se trouvent quant à eux dans un « datacenter ».

Dans la Silicon Valley on a donc d'un côté une équipe responsable de l’application (ou d’un pan fonctionnel de l’application) 
et de son bon fonctionnement;
De l'autre une équipe responsable du datacenter (processeurs, disques durs, cables réseau, …).

Les datacenters sont physiquement d’immenses bâtiments qui abritent des milliers de machines. Elles sont construites avec du matériel produit 
en grande série (des microprocesseurs de la marque intel par exemple), c’est ce qu’on appelle du « commodity hardware » ou matériel du marché.  
De cette manière, pour augmenter la capacité de traitement et de stockage du datacenter on ajoute des machines à bas coût. 
C’est le principe de la croissance horizontale (scale-out en anglais). Ceci s’oppose à la croissance verticale (scale-up en anglais) qui nécessite 
l’achat une plus grosse machine quand on atteint les limites physiques de celle qui est en place.

La raison c'est que le coût à la transaction (1 transaction = 1 recherche google par exemple) est 3 fois moins élevé pour un serveur 
d’entrée de gamme que pour un serveur haut de gamme. En utilisant ces « PC du marché » le ratio puissance/prix devient alors très avantageux 
comparé aux machines centralisées comme le mainframe. Il faut toutefois penser à faire des investissements importants en puissance électrique, 
climatisation, surface, … moins onéreux avec une machine centralisée.

Les datacenters regroupent donc des ressources informatiques (processeurs et disques durs principalement).
Ces ressources étant accessibles sur le réseau internet, les géants du web proposent à tout à chacun de les louer 
et de payer à la consommation.
C’est ce que fait Amazon avec AWS (Amazon Web Service). 
Ce service permet à d'autres sociétés de disposer de l'infrastructure (i.e. des datacenters) d'Amazon. 
On parlera alors d'IAAS (Infrastructure As A Service). 

La société DropBox par exemple utilise AWS pour stocker les données de ses clients.

Sur les IAAS apparaissent des PAAS (Plateforme As A Service). Heroku est un bon exemple. 
Ces plateformes allègent le travail des opérationnels du côté développement en ajoutant des services à l'IAAS. 

Apparaissent enfin les SAAS (Software as a service). Google apps, par exemple, vous donne accès à des applications (tableur, traitement de texte, ...)
sans avoir à installer quoi que ce soit sur votre ordinateur à part un navigateur. 

En comparaison avec un service interne à l’entreprise, ces plateformes ont certains avantages : 

- elles offrent tout d’abord une plus grande tranquillité d’esprit. On se pose moins de questions en effet sur 
le rythme des évolutions, le coût des licences, l’hébergement, etc.
- elles permettent de réduire les coûts en ne payant qu’à la consommation. 
On peut  même démarrer une activité en ligne avec un coût quasi nul. Ceci favorise l’innovation.


Mais des questions se posent encore :

- en premier lieu, la sécurité des données. En particulier pour les sociétés qui manipulent des informations sensibles comme les banques 
qui souvent n’ont pas le droit de stocker leurs données en dehors d’organismes certifiés. 
Les réglementations de la CNIL ne sont pas non plus toujours respectées sur ces plateformes. 
A noter que ce problème devrait être résolu avec les projets de cloud français ou européen comme Andromède.

- la dépendance à un service de type « cloud » peut aussi apparaitre comme  un risque.Si celui-ci subi
une panne votre système ne fonctionne plus. Cela est arrivé chez Amazon Web Service par exemple qui a subit une panne en avril et juillet 2012. 
A noter que ces pannes sont forcément très médiatisées, ce qui n’est pas le cas quand cela arrive dans d’autres entreprises. 
Le taux de disponibilité chez amazon EC2 est tout de même de 99.95 %.

- la complexité est un aspect qui peut rendre l’approche difficile. 
En effet un serveur centralisé présente au développeur une architecture théorique avec 
un seul processeur, une mémoire centrale et un système de fichiers (la machine de Von Neumann). 
Ce paradigme change quand on a une architecture basée sur des milliers de machines. 
Il devient donc plus difficile pour le développeur « traditionnel » de l’appréhender car il faut raisonner avec une répartition 
des traitements et des données. Il faut aussi se préoccuper de choses dont on ne se préoccupait pas avant dans l’applicatif 
(la scalabilibité et la tolérance aux pannes en particulier) d’où l’importance des opérationnels dans l’équipe.

- enfin, il faut prendre en compte la résistance au changement des équipes déjà en place.


Une équipe soudée autour d’un but commun sera dans les meilleures conditions pour créer des produits innovants. 
C’est ce que font les géants du web. Encore faut-il que le produit puisse être déployé sur des infrastructures solides qui supporteront 
la taille de l’internet. Ils l'ont fait en créant des datacenters qui peuvent traiter des milliers de transactions par seconde. 
Même s'il y a quelques barrières à franchir, cette infrastructure est accessible dès aujourd’hui et n’attend qu’une chose : 
que vous veniez y déposer vos innovations pour, qui sait, devenir vous-même un « géant du web ».
      

<div class = 'footnote-list'>
	<div id = 'footnote'>
	<span>1: </span>
	  <a href="http://www.octo.com/fr/publications/11-les-geants-du-web">« Les géants du web »</a>, par <a href='http://www.octo.com/fr'>Octo Technology</a> (Novembre 2012)

	<span>2: </span>
	  <a href="http://shop.oreilly.com/product/0636920026822.do?sortby=publicationDate">« What is DevOps ?»</a>, édité chez O'Reilly (Juin 2012)
	</div>
</div>	  

  





