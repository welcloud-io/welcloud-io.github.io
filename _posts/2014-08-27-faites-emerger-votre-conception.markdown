---
layout: post
title : Faites émerger votre conception
author: Olivier Lemaitre
categories: Agile
---

Nous savons intuitivement qu’un programme informatique bien conçu possède de nombreux avantages. En particulier la stabilité et le coût réduit des évolutions. 
Seulement la manière d’atteindre « la » bonne conception n’est pas du tout intuitive. Nos programmes informatiques sont souvent peu fiables et difficiles à faire évoluer
Neal Ford s’est penché sur cette question. « Emergent design and Evolutionnary Architecture » <a href='#footnote'>[1]</a> est un ensemble de dix-neuf articles 
qui expliquent comment faire émerger une conception et rendre une achitecture évolutive. Je résume ici son introduction qui est déjà très riche en enseignements.

#*Qu'est ce que la conception émergente ?*

La plupart des développeurs ont une idée de ce qu’est la conception, il n’est pas nécessaire de passer beaucoup de temps à la définir. Nous dirons qu’elle représente les principes de fonctionnement d’un composant  logiciel. La conception émergente, quant à elle, se situe entre le BDUF (Big Design Up Front - Grande Conception en Amont) et le CowBoy Hacking (Le bidouillage en mode CowBoy) comme le montre la figure ci-dessous :

![](/images/spectrum-of-design.png)

Le côté gauche du spectre suggère que vous pouvez anticiper tous les problèmes qui surviennent quand vous développez un logiciel. Par opposition, les principes de la conception émergente couvrent les aspects qui permettent à la conception d'émerger au moment où vous développez plutôt que de la fixer dans le marbre avant d'écrire la première ligne de code.

La conception émergente vise à réduire *la dette technique*, *la complexité accidentelle* et *l'hypergénéricité*. Ce sont les termes que nous allons définir maintenant.

#*La dette technique*

Chaque développeur prend conscience de la notion de dette technique quand il doit faire des compromis dans sa conception à cause de forces extérieures comme la pression des délais par exemple. Cette dette technique ressemble à la dette que l’on contracte à la banque : si vous n'avez pas suffisamment d’argent à un moment donné, vous empruntez sur le futur. De la même façon dans un projet, quand vous n’avez pas le temps de faire les choses bien, vous construisez une solution « juste-à-temps »  avec l'espoir d’en avoir dans le futur pour y revenir et l’améliorer. Malheureusement de nombreux managers ne semblent pas comprendre la dette technique et résistent quand il faut réviser des travaux antérieurs.

Seulement, construire un logiciel ce n'est pas comme creuser un fossé. Si vous faites des compromis lorsque vous creusez un fossé, ce dernier aura surement une largeur ou profondeur inégale. Mais, un fossé avec des inégalités aujourd'hui ne vous empêchera pas de creuser un bon fossé demain. Pour un logiciel, c’est différent, ce que vous construisez aujourd'hui est le fondement de ce que vous construirez demain. Un compromis qui est fait maintenant par opportunité augmente l'entropie de votre logiciel. L'entropie est une mesure de la complexité. Si vous ajoutez de la complexité avec des solutions de « juste-à-temps » pour respecter les délais vous devrez les payer dans le reste du projet.
C’est ce que montre la figure ci-dessous. La différence entre l'effort nécessaire pour ajouter une nouvelle fonctionnalité dans un système proprement conçu (avec pas ou peu de dette technique) et l’effort nécessaire pour ajouter une fonctionnalité à un système qui contient beaucoup de dette technique.

![](/images/technical-debt.png)

#*La complexité accidentelle et la complexité essentielle*

Chaque problème dans un logiciel possède une complexité inhérente (ce qu’on appellera aussi la complexité essentielle). La complexité qui découle des compromis et qui génère de la dette technique est différente. Elle ne devrait pas exister dans un monde parfait mais est induite par les forces extérieures. C'est ce qu’on appelle la complexité accidentelle. Ces termes ne sont généralement pas très tranchés. Ils possèdent un spectre comme pour la conception. 

Quelques exemples aideront à clarifier cette distinction.

Premier exemple, dans une entreprise le syndicat a réussi à négocier pour ses membres un jour de congé au début de la saison de chasse. Cet avantage ne concernait qu’une seule des usines de l’entreprise mais il devait être intégré au système de paie de l’ensemble des usines. Ce changement a ajouté beaucoup de complexité au logiciel, mais c’était une complexité essentielle. Elle faisait partie du problème que l'entreprise voulait résoudre.

Deuxième exemple, à un niveau intermédiaire du spectre. Beaucoup de gens du métier pensent qu'il faut un contrôle très fin des champs de saisie dans les formulaires. En réalité, quand on le met en œuvre, ils détestent ça car ils doivent définir et maintenir beaucoup de métadonnées. C’est arrivé sur un projet et quand les utilisateurs ont vu l'effort qui était nécessaire pour le faire fonctionner, ils ont décidé qu’ils pouvaient s’accommoder d’une sécurité moins fine. En effet, l'application se trouvait sur un seul ordinateur dans un bureau fermé à clé. Voilà un exemple de décision de conception qui a émergé quand le métier a pris conscience de la réalité de ce qu'il pensait vouloir.

A l'autre bout du spectre vers la complexité accidentelle on trouve par exemple les deux premières versions de la technologie des Enterprise JavaBeans (EJB) et des outils comme BizTalk (un outil d’intégration de données en temps réel). Seuls quelques projets ont besoin de la complexité supplémentaire introduite par ces outils. Pour les autres ils n’apportent rien à part ajouter inutilement de la complexité.

Trois choses ont tendance à introduire de la complexité accidentelle      

- Nous avons déjà parlé de la première : les actions de « juste-à-temps » dans le code.

- La deuxième est la duplication, ce que les « Pragmatic Programmers » <a href='#footnote'>[2]</a> appellent la violation du principe DRY (Dont Repeat Yourself – ne vous répétez pas). La duplication est la force la plus insidieuse dans le développement logiciel. Elle se glisse à de nombreux endroits, sans même que le développeur s'en rende compte. Les exemples sont évidemment le copier-coller de code, mais des exemples plus sophistiqués abondent. Par exemple, les projets qui utilisent un outil de mapping objet-relationnel (comme Hibernate ou iBatis) comprennent beaucoup de duplication. Le schéma de base de données, le fichier de mappage XML, et les POJOs. Ils ont tous des informations légèrement différentes mais qui se chevauchent. La duplication nuit aux projets car elle résiste aux tentatives d'apporter des modifications structurelles ou de remanier le code pour l’améliorer. Si vous savez que vous avez besoin de changer quelque chose à trois endroits différents, vous éviterez de le faire même si cela peut améliorer le code sur le long terme.

- Le troisième catalyseur de la complexité accidentelle est l’irréversibilité. Toute décision que vous faites ne pouvant pas être inversée mènera finalement à un certain niveau de complexité accidentelle. Pour cela attendez le « dernier moment responsable » pour prendre des décisions irréversibles.  Ca ne signifie pas que vous devriez retarder vos décisions trop longtemps, mais juste assez longtemps. Demandez-vous: "Ai-je besoin de prendre cette décision maintenant?" et "Qu'est-ce que je peux faire pour me permettre de reporter cette décision?". Vous serez surpris des choses que vous pouvez reporter à plus tard si vous appliquez juste un peu d'ingéniosité à votre processus de décision. Supposons par exemple que vous vouliez faire une séparation Modèle- vue-Présentation. Trop souvent, vous ferez le saut de cette architecture logique vers une architecture physique en choisissant un framework qui couvre tout ou partie de cette exigence. Essayez de reporter cette décision car une fois que l'implémentation physique est en place, elle contraint toutes les autres décisions. Repousser la décision du framework vous laissera une ouverture vers de meilleures options.        

#*L'hypergénéricité*

La dernière des préoccupations majeures pour l'architecture et la conception est la généricité. Cette généricité est d’ailleurs souvent effrénée. En effet, il semble y avoir une maladie dans le monde de la programmation (Java en particulier): la sur-conception (l’« overengineering ») des solutions. Ces solutions essaient de rendre les choses aussi génériques que possible. La motivation est claire: si nous construisons de nombreuses couches, nous pourrons plus facilement construire sur celles-ci plus tard. Cependant, il s'agit d'un piège dangereux. Parce que le caractère générique ajoute de l’entropie, vous limitez votre capacité à faire évoluer la conception dès le début du projet. Ainsi, ajouter trop de flexibilité rend plus complexe chaque changement dans le code.

Bien sûr on ne peut pas ignorer l’extensibilité. Le mouvement agile a pour cela une phrase qui résume le processus de décision pour l’ajout de fonctionnalités: YAGNI (You Aren’t Gonna Need It -Vous n’en aurez pas besoin). C'est un mantra pour éviter la sur-conception des fonctionnalités simples. Ainsi vous ne mettez en œuvre que ce dont vous avez besoin maintenant, et si vous avez besoin plus de choses plus tard, vous ne l'ajouter qu’à ce moment-là. Beaucoup de projets Java échouent car des compromis dans la conception sont sacrifiés sur l'autel de la généricité. Il est d’ailleurs paradoxal de constater qu’en voulant qu’un projet vive le plus longtemps possible on écourte finalement sa vie. Apprendre à naviguer sur la fine ligne entre l'extensibilité et la sur-conception est toutefois difficile. Et c’est là l’essence de la conception émergente qui se base principalement sur le TDD (Test Driven Developpement), le refactoring, les design patterns et la création de DSL (Domain Specific Language).


<div class = 'footnote-list'>
	<div id = 'footnote'>
	<span>1: </span>
	<a href="http://www.ibm.com/developerworks/views/java/libraryview.jsp?search_by=evolutionary+architecture+emergent+design:">
	Evolutionnary Architecture and Emergent Design </a> (Février 2009), 
	par <a href="http://nealford.com/">
	Neal Ford</a>
	<br>
	<span>2: </span>
	<a href="http://www.amazon.fr/The-Pragmatic-Programmer-Journeyman-Master/dp/020161622X/ref=sr_1_1?ie=UTF8&qid=1409236802&sr=8-1&keywords=the+pragmatic+programmer">
	The Pragmatic Programmer: From Journeyman to Master </a> (Octobre 1999), 
	par Andrew Hunt et David Thomas
	        
	</div>
</div>