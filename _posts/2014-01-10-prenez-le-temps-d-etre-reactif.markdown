---
layout: post
title : Prenez le temps d'être réactif
author: Olivier Lemaitre
categories: Agile
---

Souvent la dernière préoccupation dans les projets informatiques, la qualité du logiciel devient pourtant vitale dans les entreprises. 
Cet article a pour but de la définir, d'expliquer pourquoi elle est nécessaire mais aussi pourquoi nous avons autant de difficultés à intégrer 
cette dimension dans nos projets. Enfin nous décrirons les mesures à prendre pour rectifier le tir. 
Cet article se base sur une étude très complète du sujet : « Livre blanc qualité logicielle, pragmatisme et productivité »<a href='#footnote'>[1]</a>.

Le logiciel n’a jamais été aussi important pour les entreprises : Amazon, FaceBook, Apple, eBay pour ne citer qu’elles, sont des entreprises qui ont assis 
leur domination grâce à l’avantage concurrentiel que leur procuraient les logiciels. 
Elles ont compris, bien avant les autres, l’importance de la qualité logicielle. Toute défaillance engendrant une perte directe de chiffre d’affaires.

A ce jour néanmoins, dans nos entreprises, malgré de nombreux efforts 
(Assurance qualité, direction qualité, responsable qualité, qualimétrie, processus unifié, modèle de maturité,...) le logiciel de qualité reste l’exception. 
On pourrait pourtant s’attendre à ce que, après un demi-siècle d’existence, le développement logiciel ait atteint une forme de maturité. 
Or lancer un projet informatique reste pour beaucoup une opération pénible, risquée, coûteuse, incertaine et aux résultats trop souvent décevants.

Cette situation n’est pas une fatalité. Mais pour cela il faut comprendre que la qualité n’est pas fonction du processus de fabrication du logiciel, 
mais la discipline et de la compétence de ceux qui sont chargés de le concevoir et de le programmer – en premier lieu les développeurs et les testeurs.

#*Qu’est ce que la qualité logicielle ?*

Tout d’abord nous allons définir ce que nous entendons par la qualité du logiciel. Cette définition ne peut tenir en une seule phrase 
pour la simple est bonne raison qu’elle est perçue différemment selon les points de vue. 
Un utilisateur final, par exemple, se basera sur l'ergonomie, la stabilité, la fiabilité, les performances. 
Un développeur appréciera la conception, la lisibilité du code source ou encore la testabilité. 
L’exploitant s’attachera davantage à la facilité d’installation et de mise à jour, à la simplicité du diagnostic et de la supervision. 
L’architecte, quant à lui, sera plus sensible à l’interopérabilité, à la portabilité, à l’intégration harmonieuse de la solution dans le système d’information. 
Un DSI, enfin, se fiera aux coûts de développement, de maintenance et d'évolution.

Pour cet article un logiciel de qualité sera un logiciel solide que l’on peut faire évoluer facilement. 
Non pas que les autres aspects ne soient pas importants mais ceux-là sont les plus coûteux pour l’industrie informatique dans son ensemble. 
Ainsi, un manque de fiabilité se traduira par des erreurs de fonctionnement – des bugs -, dont les conséquences opérationnelles 
peuvent être catastrophiques. Un logiciel peu maintenable, quant à lui, verra ses coûts d’évolution croître avec le temps, 
potentiellement jusqu’à la calcification complète. Ce défaut de réactivité peut être mortifère si l’on admet que la production 
logicielle a acquis une dimension stratégique pour de nombreuses organisations, et que ce statut impose d’ajuster 
en permanence les capacités fonctionnelles des logiciels à des exigences opérationnelles en évolution permanente.

#*Pourquoi les logiciels de nos informaticiens sont-ils si peu fiables ?*

Il existe des moyens simples pour réduire les défauts de fonctionnement d’un logiciel. 
Le principal est le renforcement des pratiques de tests. 
Mais les pratiques de tests sont souvent défaillantes dans de nombreuses organisations.

Tout d’abord, tester davantage a un coût. 
Ce coût est d’autant plus important que le système est complexe, et il peut être mesuré au préalable. 
Le coût des dysfonctionnements quant à lui ne peut être mesuré qu’à postériori.

Par exemple en 2009, un petit bug dans la gestion des arrondis pour le calcul du nombre de trimestres cotisés à l’assurance-vieillesse est découvert. 
Ce bug, introduit dans le système en 1984, a conduit à affecter un trimestre de trop à près de 8 millions de salariés, et à surestimer 
en conséquence le montant de leur pension. 25 ans plus tard, le coût total pour l’Assurance Sociale approche les 2,5 milliards d’euros.

Il va de soi qu’écrire un test unitaire validant la règle d’arrondi du nombre de trimestres à prendre en compte pour le calcul 
de la pension de retraite aurait représenté une charge pratiquement nulle – surtout si on la met en regard de la perte engendrée par l’erreur. 
Mais pour que ce test ait eu une chance d’être écrit, il aurait fallu une politique de tests unitaires exhaustive, couvrant l’intégralité des fonctions du système. 
Et une telle politique impliquait un surcoût immédiat, alors difficile à mettre en regard de gains futurs. 
La plupart des projets informatiques sont soumis à de fortes contraintes de budget et de délais. 
La préférence pour le présent consiste bien souvent à préserver des objectifs à court terme – livrer à temps – au détriment des risques à moyen et long terme. 
Ainsi les tests fournissent une variable d’ajustement commode. 
Or, il est communément admis qu'au moins 30% de la charge d'un projet doit être attribuée aux tests. 

Ce phénomène économique est amplifié par la crainte de la sur-qualité. 
On entend alors que le niveau de test actuel est déjà suffisant, et que tout effort additionnel risquerait d’avoir un rendement très faible voire négatif. 
Il est vrai que la sur-qualité, et les coûts qu’elle comporte, a longtemps été réservée aux projets ayant une sensibilité extrême aux défauts. 
Par exemple, le système de pilotage automatique d’une navette spatiale ne supporte pas l’échec. 
Mais aujourd’hui, un grand nombre d’applications informatiques sont devenues critiques et même stratégiques. 
Par conséquent la sur-qualité est devenue rentable. 
Sacrifier certains tests pour respecter certaines contraintes de coûts ou de délais à court terme est bien souvent un arbitrage peu judicieux. 
Il est souvent préférable de réduire le périmètre du logiciel mais de s’assurer que ce qui est livré est fiable.

On peut aussi ajouter que très naturellement, les tâches qui ne se voient pas ou ne font pas avancer le projet fonctionnellement (comme coder un test) 
ne sont pas satisfaisantes, voire stressantes. Chacun veut se rassurer sur sa capacité à réaliser la tâche à laquelle il est affecté et pour cela, il faut voir 
le résultat au plus vite. 

#*Pourquoi est-il si difficile de faire évoluer une application ?*

S’il est facile de mesurer le manque de fiabilité, qui se traduit par des défauts de fonctionnement, il n’en est pas de même pour la « maintenabilité » 
(ici, la capacité à évoluer). Cela se comprend aisément : un logiciel peu maintenable coûte cher à faire évoluer ; 
mais il est impossible de comparer ce coût à ce qu’il aurait été si le logiciel avait été plus maintenable. 
l faudrait deux versions du logiciel pour comparer.

L’approche traditionnelle de la maintenance logicielle s’appuie sur l’idée que les principaux changements apportés à 
un logiciel après sa première mise en service relèvent de la correction d’anomalies. Mais il est de plus en plus communément admis 
que le nombre de lignes de code produites après la première mise en service d’une solution logicielle est supérieur 
à celui produit avant (60 à 80% du code est produit lors de la maintenance évolutive ou corrective).  
A cela, deux raisons : en premier, les applications sont de plus en plus proches des fonctions stratégiques des organisations, 
et doivent donc être en permanence ajustées à son environnement opérationnel ; nouvelles offres, nouveaux marchés, nouveaux concurrents, 
nouvelles façons de faire… le monde change vite, et les logiciels doivent s’adapter au même rythme. 
Deuxièmement, les architectures modernes, orientées réseaux, autorisent la diffusion instantanée des changements à tous les utilisateurs 
pour des coûts très faibles. Pourquoi, dès lors, se priver de mises à jour fréquentes ?

Ainsi, si les évolutions sont nombreuses et le logiciel peu maintenable, le surcoût est mécaniquement démultiplié. 
De surcroît, le défaut d’évolutivité tend à s’amplifier avec le temps – un logiciel peu adaptable, que l’on fait évoluer au forceps, 
se dégrade encore davantage. Le coût marginal des évolutions est alors croissant, jusqu’au stade où la seule décision rationnelle devient 
la réécriture complète.

#*Quelles mesures prendre pour rendre un logiciel fiable et maintenable ?*

**L’automatisation des tests** (tests fonctionnels, tests unitaires, tests d’intégration, tests de charge) est la première mesure indispensable 
pour augmenter la tolérance au changement. La raison en est simple. Quelle que soit la raison pour laquelle on souhaite modifier un logiciel, 
la plupart des modifications se font à la marge. Autrement dit, le volume de code qui n'est pas modifié est très largement supérieur au volume 
de code modifié. Tout le risque réside alors dans les éventuelles régressions introduites dans le reste du code par cette modification marginale. 
Pour s’assurer contre ce risque de régression, il est nécessaire non seulement de tester les nouvelles fonctionnalités, mais également de vérifier 
que toutes les autres fonctionnent toujours correctement. En somme, le coût total d’une évolution comprend le développement de la nouvelle 
fonctionnalité, plus le test de l’intégralité du logiciel. Le nombre de fonctionnalités allant croissant, cet effort de test ne fait qu’augmenter. 
Rapidement, le coût des tests de non-régression excède très largement celui du développement des évolutions. Seule une automatisation 
poussée permet alors de maintenir ce coût dans des proportions acceptables. L'automatisation est un investissement obligatoire si l'on fait 
des livraisons sur des cycles courts. Il n’est pas rentable de suite car l'expérience montre qu’il le devient à partir de la 4ème campagne de tests. 

Seconde mesure visant à augmenter la tolérance au changement de nos logiciels, <b>une conception favorable aux changements</b>. 
Il existe plusieurs paradigmes de programmation, les principaux sont : la programmation fonctionnelle, procédurale et orientée objet. 
Nous parlerons uniquement ici de la dernière car c’est la plus répandu à ce jour dans les applications métier, et probablement celui dont les 
fondements théoriques sont les plus directement liés à la problématique de l’évolutivité.

La programmation orientée objet a en effet spécifiquement été conçue dans les années 60 pour simplifier les évolutions de logiciels à la complexité croissante. 
Elle est sous-tendue par un modèle mathématique sophistiqué, dont la principale vertu est de limiter les effets de bord d’un changement. 
Pour cela, la conception objet repose sur un ensemble d’unités discrètes et indépendantes, les classes, chacune dotée d’un rôle ou d’une responsabilité 
distincts. Ces classes encapsulent données et comportements, et collaborent avec d’autres classes pour réaliser des traitements complexes. 
Correctement utilisées, les techniques de programmation orientée objet offrent des leviers spectaculaires pour limiter 
les efforts nécessaires à l’implémentation d’une nouvelle fonctionnalité, et les risques de régression associés.

Malheureusement, et malgré le succès spectaculaire des langages orientés objet (Java, C++, C#, VB.NET, Ruby, PHP, etc.), le niveau 
de la conception objet reste bien souvent insuffisant ; et bien souvent les applications, bien qu’écrites avec un langage objet, sont plutôt 
conçues sur un mode procédural. En effet Il est plus facile d'écrire du code linéaire, comme nous le ferions avec un langage procédural, 
et d'ajouter des conditions, pour faire évoluer son comportement, que de penser objet. Le revers viendra après avec l'ajout de fonctionnalités, 
les adaptations de l'existant. Le code se traduira le plus souvent par des méthodes de plus en plus longues, des enchainements de 
conditions interminables dans lesquels le développeur, même expérimenté se perdra facilement, engendrant une explosion des temps de 
développement et des anomalies plus fréquentes. Améliorer la tolérance au changement des logiciels passe en conséquence par une élévation 
de la conscience objet des développeurs.

Enfin, dernière mesure visant à favoriser la tolérance au changement des logiciels, <b>la lisibilité du code</b>. 
Une nouvelle fois, il s’agit d’un aspect très souvent négligé. Pourtant, ce défaut de lisibilité est souvent évoqué : une règle quasiment universelle 
du développement est qu’il est beaucoup plus difficile de lire du code existant que d’écrire du nouveau code. 
D’où la tentation récurrente de la part des développeurs de tout réécrire, plutôt que de chercher à comprendre ce qui existe. 
C’est vrai lorsque l’on consulte le code écrit par un autre développeur, mais c’est aussi vrai lorsque l’on consulte du code que l’on a écrit soi-même, 
quelques semaines ou quelques mois plus tôt. Si le code est difficile à lire, il est ardu de comprendre ce qu’il fait. Il est alors malaisé de 
déterminer ce qui doit être changé et, pire encore, il est très difficile de réaliser un changement sans corrompre l’intégrité conceptuelle du code existant.

La raison pour laquelle il est plus difficile de lire du code que d’en écrire est très simple : lorsque l’on programme, la principale difficulté 
consiste à décrire un comportement en utilisant un langage formel très contraignant. A ce moment-là, l’enjeu réside principalement dans 
des considérations syntaxiques et algorithmiques : ce qu’attend le compilateur pour convertir le texte en programme exécutable. 
Le compilateur n’a que faire de la sémantique du code, ou de l’intention du programmeur. 
Pour lui, une méthode nommée acheterDesBananes a autant de sens qu’une méthode nommée calculerEncours, 
pour peu que les règles syntaxiques soient respectées. Les noms des classes, des méthodes et des variables lui importent peu : 
ils seront convertis en symboles adressables. Pour celui qui lit le code, par contre, le nommage et la simplicité sont primordiaux. 
Une méthode trop longue est difficile à comprendre, même si elle est fonctionnellement correcte. 
Une méthode dont le nom ne reflète pas la fonction sera source de confusion, voire de malentendu, pour celui qui cherchera à en comprendre l’usage. 
Et nous pourrions multiplier les exemples.

Ces mesures (automatisation des tests, conception favorable aux changements et lisibilité) sont indispensables à l'obtention d'un logiciel de qualité. 

#*Quels sont les outils pour parvenir à obtenir un logiciel de qualité ?*

Il existe de nombreux « framework » pour automatiser les tests, il existe aussi beaucoup d’outils qui permettent de concevoir un modèle 
objet tout comme il existe des outils d’analyse permettant de détecter des algorithmes trop complexes. Mais c’est loin d’être suffisant.

La solution réside surtout dans des pratiques techniques et collaboratives, voici les principales :

- Une des pratiques majeures est le TDD (Test Driven Development ou Développement Piloté par le Tests). 
Cette technique a pour but de garantir que le code qui est écrit est bien testé automatiquement. 
Pour cela le développeur doit toujours écrire le test de la fonctionnalité avant d’écrire le code correspondant.

- Le « refactoring », opération de maintenance visant à revoir une partie de la conception ou du code. 
Cette pratique va permettre à ce dernier de supporter les modifications à venir, améliorer sa lisibilité, simplifier sa maintenance. 
Il doit être pleinement intégré au processus de développement. 
A noter que le TDD facilite grandement le « refactoring » et l’émergence de la conception.

- L’intégration continue : partant du constat que la phase d'intégration des projets (i.e l’assemblage des composants) est longue et coûteuse, 
l'idée est de la faire en continu (une à plusieurs fois par jour) pour détecter les problèmes, et par conséquent les corriger, au plus tôt. 
Il faut savoir que détecter un problème d’intégration tardivement dans le projet coute au moins 5 fois plus cher que de la détecter 
quand il vient d’être introduit.

- La programmation en binôme permet à chacun d’apprendre des techniques et de l'expérience de l'autre et, au fil du temps, de l'ensemble 
des développeurs. Ceci contribue à l'accroissement du niveau de maitrise général de l'équipe et évite des transferts de compétence tardifs 
et peu efficaces. Mais surtout un regard neuf, permet de déceler rapidement des erreurs simples, de s'assurer que le code est lisible, et 
de lever des interrogations. Les questions posées par une personne n'ayant pas réalisé le développement sont souvent perspicaces et permettent 
de résoudre des problèmes de conception, de codage, de compréhension en amont.

Ces pratiques ne peuvent pas s’inscrire dans un processus bien établi (un cycle en V) mais dans un processus adaptable (les méthodes agiles). 
Paradoxalement cette liberté demande beaucoup plus de discipline et de rigueur que dans un processus bien établi.
A noter aussi que toutes ces pratiques pour être correctement appliquées, doivent, d'une part, être comprises et assimilées mais aussi et 
surtout avoir l'adhésion des membres des équipes de développement ainsi que de l'encadrement.

Pour conclure, les logiciels peu fiables et peu évolutifs ne sont pas une fatalité. Il suffit de regarder ce que font les sociétés de la silicon valley 
(Avez-vous d'ailleurs déjà appelé le support informatique d’une de ces sociétés ?). 
Mais si nous voulons nous en approcher, il faut changer notre manière de concevoir le logiciel en élevant le niveau 
des équipes de développement tout en utilisant de nouvelles pratiques. 
Ceci représente évidemment un investissement, en particulier en temps, mais ça se justifie aujourd'hui. 
Il faut donc parier que la qualité du logiciel prendra une place de plus en plus importante dans nos entreprises car aujourd'hui 
ce n'est plus le plus gros qui mange le plus petit mais le plus rapide qui dépasse le plus lent.


<div class = 'footnote-list'>
	<div id = 'footnote'>
	<span>1: </span>
	<a href="http://blog.xebia.fr/wp-content/uploads/2010/12/Livre-blanc-qualit%C3%A9-logicielle.pdf">« Livre blanc qualité logicielle, pragmatisme et productivité »</a>, par la société <a href='http://xebia.com/'>Xebia</a> (Juillet/Août 2003)
	
	</div>
</div>

