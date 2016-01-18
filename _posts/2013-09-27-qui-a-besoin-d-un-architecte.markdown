---
layout: post
title : Qui a besoin d'un architecte ?
author: Olivier Lemaitre
categories: Agile
---

Le terme architecte est très utilisé dans le monde du logiciel, mais son rôle est souvent mal défini.
L'objectif ici est de le clarifier en utilisant les meilleurs passages de l'article de Martin Fowler : « Who Needs an Architect ?»<a href='#footnote'>[1]</a>.

#*Qu'est-ce que l'architecture logicielle ?*

RUP, réduisant la définition de l’IEEE, définit l’architecture comme _« le plus haut niveau de concept d’un système dans son environnement. 
L’architecture d’un système logiciel (à un moment donné dans le temps) est son organisation ou la structure des composants majeurs qui interagissent à travers des interfaces. 
Ces composants majeurs se déclinent en des composants et des interfaces plus petits »._

Ralph Johnson <a href='#footnote'>[2]</a> répond à cela : 
_« cette définition est bugée. 
Il n’y a pas de "plus haut concept d’un système". Les clients ont d'ailleurs des concepts différents des développeurs
et se moquent complètement de la structure des composants majeurs. 
Dans ce cas on devrait dire qu’une architecture est le plus haut niveau de concept que les développeurs ont d’un système. 
Si on oublie les développeurs qui comprennent juste que leur petit morceau, 
l’architecture est alors le plus haut niveau de concept des développeurs experts. 
Finalement, qu’est-ce qui rend un composant majeur ? Il est majeur car les développeurs experts le disent._

_Ainsi, une meilleure définition serait : " dans les projets qui réussissent, les développeurs experts 
possèdent une compréhension partagée de la conception du système. 
Cette compréhension partagée s’appelle l’architecture.
Cette compréhension inclut la façon dont le système est divisé en composants et comment ils interagissent à travers des interfaces. 
Ces composants sont habituellement composés de composants plus petits, mais l’architecture inclut uniquement les composants qui sont compris 
par tous les développeurs."_

_Ce serait une meilleure définition parce qu’il est clair que l’architecture est une construction sociale (le logiciel l'est aussi, mais l’architecture l’est bien plus) 
qui ne dépend pas juste du logiciel, mais  de la partie du logiciel qui est considérée comme importante par un consensus de groupe._

_Il y a un autre style de définition de l’architecture du style : « L’architecture est un ensemble de décisions de conception qui doivent être faites tôt 
dans le projet ». Je me plains de celle-ci aussi en répondant que l'architecture est un ensemble de décisions que vous aimeriez être bonnes tôt dans le projet, 
mais que vous ne prendrez  probablement pas mieux que les autres._

_Savoir si quelque chose fait partie de l’architecture est entièrement basée sur ce que les développeurs pensent être important. 
Par exemple, les gens qui construisent des applications d'entreprise tendent à systématiquement penser que la persistance est cruciale.
Quand ils commencent à dessiner leur architecture, ils commencent avec 3 couches. 
Ils vont mentionner : « nous utiliserons Oracle pour notre base de données et nous avons notre propre couche de persistance pour mapper les objets ».
Mais une application d’imagerie médicale par exemple pourrait inclure une base de données Oracle sans faire partie de l’architecture. 
La complexité de ce type d'application c'est d’analyser les images pas de les stocker. 
Récupérer et stocker les images est réalisé par une petite partie de l’application et la plupart des développeurs l’ignorent._

_Avant de décrire une architecture, il faut se demander: "Qu'est ce qui est important ? ", car
l’architecture concerne les choses importantes. Peu importe ce que c’est.»_

#*Rôle de l’architecte.*

Si l’architecture représente les choses importantes, alors l’architecte est la personne (ou les personnes) qui se préoccupent des choses importantes. 
Nous arrivons ici à la différence entre l’architecte de ‘Matrix Reloaded’ et le style d'architecte qu'est David Rice.

L'«Architectus Reloadus» est une personne qui prend toutes les décisions importantes. 
Il fait ça parce qu’il pense qu'il ne faut qu’un seul esprit pour assurer l’intégrité d’un système.
Peut-être aussi parce qu'il pense que les membres de l’équipe n’ont pas suffisamment de compétences pour prendre ces décisions
et qu'elles doivent se prendre tôt pour que chacun ait un plan à suivre.

L'«Architectus Oryzus» est un animal différent <a href='#footnote'>[3]</a>. 
Ce type d’architecte doit être très conscient ce qui se passe sur le projet, dénichant les problèmes importants et les taclant avant qu’ils ne 
deviennent des problèmes sérieux.
Quand je vois un architecte comme celui-là, la partie du travail la plus notable est une intense collaboration. 
Le matin, il programme avec un développeur, essayant de trouver du code à débloquer. 
L’après-midi, il participe à l’expression des besoins, expliquant aux utilisateurs les conséquences techniques de leurs idées 
dans des termes non techniques (comme le cout du développement par exemple).

De plein de façon, l’activité la plus importante d’Architectus Oryzus est de «mentorer» l’équipe de développement  pour élever son niveau de façon 
à ce qu’elle puisse prendre des problèmes plus complexes. 
Améliorer les compétences d’une équipe donne à l’architecte un plus grand levier que d’être 
le seul à décider et ainsi courir le risque d’être un goulet d’étranglement.
Ceci conduit à la règle satisfaisante que la valeur de l’architecte est inversement proportionnelle au nombre de décisions qu’il prend.

Le meilleur nom que l'on puisse lui donner c'est : un guide, comme dans l’alpinisme. 
Un guide est un membre de l’équipe plus expérimenté et compétent. Il enseigne aux autres comment se débrouiller 
par eux-mêmes tout en étant toujours là pour les choses vraiment difficiles.

#*Le but ultime: se débarasser de l'architecture*

Martin fowler ajoute une définition en partant d'une autre citée plus haut : "L’architecture est un ensemble de décisions de conception qui doivent être faites tôt 
dans le projet". Pourquoi est-ce-que les gens ont besoin de faire des choix corrects dès le début d'un projet ? 
La raison c'est qu'ils perçoivent tout simplement ces décisions comme difficiles à changer. 
Ce qui amène à dire qu'on peut aussi définir l'architecture comme "l'ensemble des décisions difficiles à changer".

Or dans le logiciel nous n'avons pas les mêmes contraintes que dans le monde physique. 
Nous pouvons trouver des solutions pour que les choses qui semblent difficiles à changer le soient moins.
L'irréversibilité est le premier facteur de complexité et les méthodes agiles essaient de réduire la complexité en réduisant l'irréversibilité.
Ainsi une des tâches les plus importantes de l'architecte est de trouver des moyens d'éliminer l'irréversibilité dans la conception des logiciels.

<div class = 'footnote-list'>
	<div id = 'footnote'>
	<span>1: </span>
	<a href="http://martinfowler.com/ieeeSoftware/whoNeedsArchitect.pdf">« Who Needs an Architect ?»</a>, par <a href='http://martinfowler.com'>Martin fowler</a> (Juillet/Août 2003)

	<br>
	<span>2: </span>	    
	Ralph Johnson est le co-auteur du livre <a href="http://www.amazon.fr/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612/ref=sr_1_1?ie=UTF8&qid=1392466786&sr=8-1&keywords=design+pattern">"Design Patterns: Elements of Reusable Object-Oriented Software" </a>

	<br>
	<span>3: </span>	    
	Oryzus est un mot latin qui signifie Riz en français. Riz se disant Rice en anglais, c'est un jeu de mot pour catégoriser les architectes comme David Rice.
		    
	</div>
</div>
