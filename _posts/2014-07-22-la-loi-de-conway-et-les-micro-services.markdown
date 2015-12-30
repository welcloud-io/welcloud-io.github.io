---
layout: post
title : La loi de Conway et les Micro-Services
author: Olivier Lemaitre
categories: Agile
---

Il y a des évènements dans l’année que l’on attend avec plus d’impatience que d’autres. 
Un de ceux que je préfère c’est la sortie des radars technologiques de chez ThoughtWorks. 
Cette société est une des plus visionnaires que je connaisse et leur radar vaut vraiment la peine 
d’être lu si on s’intéresse à ce qui se passe dans l’univers du logiciel. Vous trouverez ici ce que 
j’ai préféré dans le dernier radar sorti ce mois de juillet<a href='#footnote'>[1]</a>.

#*La loi de Conway*  

La loi de Conway stipule qu' “une organisation qui conçoit un système concevra un système dont 
la structure est une copie de la structure de communication de l'organisation”. 
En d’autres termes "La structure d'un système est à l'image de la structure de communication de l'organisation qui l'a conçu".
Ou encore autrement dit, si l’organisation communique mal alors le système communiquera mal.

La loi de Conway renforce une des  idées clés du manifeste agile “Les individus et leurs interactions plus que les processus et les outils”. 
Par conséquent, des entreprises sont aujourd’hui embourbées dans des structures en silos et ajoutent ainsi des frictions inutiles au travail des employés. 
D’un autre côté des entreprises plus éclairées utilisent l’organisation des équipes pour piloter le type d’architecture 
qu’elles veulent. On peut donc penser qu’ignorer la loi de Conway peut être néfaste et que s’appuyer sur elle peut être un véritable avantage.

La ‘Manoeuvre inverse de Conway’ recommande donc de faire évoluer vos équipes et votre organisation 
pour avoir des systèmes mieux structurés. Ainsi l’architecture du système s’adaptera à l’architecture métier.

Par exemple, des sociétés crée avec de bonnes intentions une équipe DevOps séparée, ce qui est une interprétation erronée de la définition de DevOps. 
Plutôt qu’un rôle, DevOps est un mouvement culturel qui encourage la collaboration entre les spécialistes des opérations et les développeurs. 
Plutôt que de créer un autre silo et souffrir des conséquences de la loie de Conway, il est conseillé d’intégrer ces compétences dans toutes les équipes. 
En retirant les frictions, vous améliorez ainsi la boucle de feedback et la communication ce qui profite au système.

De la même façon, beaucoup d’organisations créent des équipes séparées pour le développement et le test (ou Q.A. : Quality Assurance). 
Seulement, le feedback rapide est un principe au coeur de l’agilité et il est critique pour le succès des projets. 
Utiliser des équipes de qualification séparées ralenti ce feed back, crée un mentalité de “eux et nous”. Il est alors plus 
difficile de faire de la qualité logicielle. Le test doit être une activité fortement intégrée aux équipes 
de développement et n’est pas quelque chose que l’on peut externaliser.

#*Les Micro-Services*

Tout comme pour les API, qui sont des interfaces de communication 
au sein des organisations et avec le monde extérieur, il y a actuellement un fort intérêt 
autour des architectures de micro-services.

Dans une architecture de micro-services un grand nombre de très petits services sont déployés et agrégés 
pour constituer le système. Ces services sont très proches des concepts métier. Néanmoins, pour que cette approche fonctionne
les équipes ont besoin d’une grande discipline autour du “build”, du test, de l’intégration et de la gestion des services.

En effet, une architecture de micro-services par sa nature augmente de manière significative le nombre d’applications, 
de services et d'interactions dans les environnements de production. 
Une bonne pratique est la construction d’un “Annuaire Humain” (Humane Registry) 
(<a href="http://martinfowler.com/bliki/HumaneRegistry.html">martinfowler.com/bliki/HumaneRegistry.html</a>) 
qui agrège les informations sur les services qui sont déployés en s’appuyant sur l’environnement de production.
Cet annuaire les présente alors dans un format qu’un humain peut comprendre. 
Avec cette approche, les informations sur les services sont plus à jour que dans une documentation écrite à la main.    

<div class = 'footnote-list'>
	<div id = 'footnote'>
	<span>1: </span>
	<a href="http://assets.thoughtworks.com/assets/technology-radar-july-2014-en.pdf">
	Technology Radar </a> (Juillet 2014), 
	par <a href="http://www.thoughtworks.com/">
	ThoughtWorks</a>
	
	</div>
</div>	    

