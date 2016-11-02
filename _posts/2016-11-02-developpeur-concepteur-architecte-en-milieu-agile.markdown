---
layout: post
title : Développeur, Concepteur, Architecte en milieu Agile. Qu'est-ce qui change ? Et pourquoi ?
author: Olivier Lemaitre
categories: Ingenierie
---

Quel rôle pour le développeur, le concepteur ou encore l’architecte dans un environnement “Agile” ? 
Sont-ils tous encore nécessaires ? Peut-être que non, mais ce qui est sûr c'est qu'ils doivent évoluer. 
Pour comprendre dans quelle direction, nous nous appuierons sur les textes fondateurs 
de Jack Reeves et Martin Fowler ainsi que des modèles d’organisation 
comme celui d’Amazon et Spotify.

## Qu'est ce qui change pour les développeurs et les concepteurs en milieu agile ?

### Qu’est ce que la Conception Logicielle ?

Qu'est-ce que la conception logicielle ? la réponse a déjà été apportée en 1992 dans 
un article <a href='#footnote'>[1]</a> qui influencera énormément les méthodes agiles 
par la suite et qui est toujours très actuel.
Jack Reeves y fait la comparaison entre le métier de l’ingénieur dans une discipline 
traditionnelle, comme le bâtiment ou l’électronique; et le métier des ingénieurs 
dans le monde du logiciel. 

Finalement quel est le rôle d’un ingénieur ? 
On peut répondre à cette question très simplement: c’est de produire une forme de documentation. 
D’ailleurs quand on cherche le terme “engineering” dans Google images, 
il nous affiche... des documents.

![](/images/developpeur-architecte-agile/engineering-google-images-min.png){: .center-image }

Ainsi l'ingénieur du bâtiment par exemple ne fabrique pas lui-même les ponts qu’il conçoit. 
Un ingénieur en microprocesseur ne grave pas lui-même les microprocesseurs qu'il a imaginés. 
Ces ingénieurs produisent une documentation qui servira à une autre équipe. Une équipe avec des compétences très
différentes, qui fabriquera le produit final (un pont ou un microprocesseur).

Par exemple, dans le bâtiment, l'équipe de fabrication se basera sur le plan DCE (Dossier de consultation des entreprises).
Ce dossier est produit par les ingénieurs ou les architectes.

Dans l’électronique, la société ARM est aussi un très bon exemple.
Elle produit juste des plans. Elle vend ensuite des licences qui permettent 
à d'autres entreprises de les utiliser pour fabriquer et vendre des microprocesseurs ARM. 
On les retrouve ensuite dans nos smartphones.

Dans l’industrie logicielle, nous avons essayé (et beaucoup essaient toujours) de construire 
les logiciels comme des ponts ou des microprocesseurs. Le processus est très similaire, 
on demande l’ensemble des exigences à la maîtrise d’ouvrage 
pour produire un cahier des charges puis on rédige des dossiers de conceptions et de 
spécification qui ressemblent aux dossiers des autres ingénieurs. 
Une fois que les choses sont figées, on commence à coder le logiciel c’est-à-dire à 
le fabriquer comme le feraient les ouvriers d’un chantier (n.b. cet ouvrier c'est le développeur).

La question maintenant c'est, qu'est-ce que l’on veut fabriquer finalement ? 
Un logiciel me direz-vous, nous sommes d'accord.

Mais, au fait, qu'est-ce qu'un logiciel ?
C'est une suite de 0 et de 1 qui seront exécutés ou traités par un microprocesseur.

![](/images/developpeur-architecte-agile/binaire-min.jpg){: .center-image }

Par qui cette fabrication est-elle assurée ?
Par les *compilateurs et les chaînes de déploiement*. 
C'est cette équipe qui utilise les plans de l'ingénieur pour fabriquer le produit.

Par déduction, la documentation que produit l’ingénieur logiciel c’est du code. 
C’est grâce à cette notation que l’ingénieur logiciel peut concevoir le logiciel.

![](/images/developpeur-architecte-agile/code.jpg){: .center-image }

En effet, les plans d’un ingénieur (ou d’un architecte) contiennent assez d'information 
et de détail pour construire le produit final 
sans avoir à poser de questions à celui qui les a produits. 

C’est vrai pour le plan DCE (Dossier de Consultation des Entreprises) dans la construction classique des bâtiments. 
Or le seul document qui peut contenir ce niveau de détail dans la construction logicielle c’est l’ensemble du code.

![](/images/developpeur-architecte-agile/comics-min.png){: .center-image }

Faut-il abandonner les outils de modélisation traditionnels comme UML ou les cartes CRC ? 
Peut-être pas mais il faut comprendre que ce que l'on produit avec ces outils n'est pas la conception.
C'est une aide à la conception, à la réflexion générale, un peu comme la maquette dans la construction des bâtiments.

![](/images/developpeur-architecte-agile/diagramme-uml.gif) 
![](/images/developpeur-architecte-agile/maquette.gif)

En les utilisant on perd beaucoup d’informations sur la problématique métier que l’on veut résoudre avec le code. 
Ils agissent comme un filtre entre le métier et les développeurs.
Dit autrement, le nombre de décisions que l’on peut écrire sur une feuille de papier est très 
largement inférieur au nombre de décisions qui se trouvent dans une page de code.

Cela veut dire que fournir un dossier de spécification même avec des diagrammes UML à 
des développeurs en espérant qu’ils sortent un bon produit, 
revient à donner la maquette en carton d’un bâtiment à une équipe d'ouvriers et
leur demander de le construire. Il y a de grandes chances que les murs porteurs ne soient pas au bon endroit 
ou que l'ouverture des fenêtres ne soient pas aux bonnes dimensions.

Dans le meilleur des cas, s'ils le peuvent, les ouvriers (ou les développeurs) viendront poser beaucoup de questions. 
Au pire ils livreront quelque chose. Mais ce quelque chose sera loin de ce que l'on voulait vraiment.
C'est une des raisons qui rend les développements à l'étranger si difficile car 
les équipes reçoivent l'équivalent d'une maquette en carton et la distance, la langue et la culture 
ne permettent pas une bonne communication.

Même si l'on peut avoir un vocabulaire commun (structure, conception, pattern, …) entre le monde physique et le monde des octets,
très vite les deux mondes divergent.

Pourquoi passe-t-on du temps à concevoir un pont (études structurelles, essais en soufflerie, maquettes, plans détaillés, etc) ? 
Parce qu'on veut qu'il tienne debout du premier coup.
Pourquoi veut-on qu'il tienne debout du premier coup ?
Parce que fabriquer un pont coute cher (bien plus que la conception). On ne peut donc pas 
le refabriquer plusieurs fois de manière différente pour voir ce qui convient le mieux. 
C'est pour cela qu'on adopte une démarche prédictive dans laquelle on va prévoir tout ce qui peut se produire.

Dans le logiciel c’est l’inverse, le coût de conception (i.e. écriture du code ) est élevé mais la 
fabrication (ce que font les compilateurs et les chaînes de déploiement) est très bon marché.
On peut le reconstruire autant de fois que l’on veut, ce qui permet d'expérimenter, d’explorer, de procéder 
par des phases courtes de construction (build) et de tests. 
On peut donc utiliser une démarche dite adaptive (qui facilite une adaptation - c.f. wikipedia).

> Il existe bien d’autres différences entre la construction d’un bâtiment et la fabrication d’un logiciel. 
Ces différences sont liées au fait que les systèmes logiciels sont extrêmement complexes, bien plus complexes qu’un bâtiment par exemple. 
La raison c'est que dans le logiciel il n’y a pas de contraintes physiques. Citons quelques-unes de ces différences.

> Quand on construit un pont, on peut avoir des milliers voir des millions de certains composants. 
Par exemple les rivets pour construire un pont en métal. 
Dans le logiciel on peut aussi avoir des millions de composants, les contrôleurs d’une application utilisant du MVC (Model-View-controler) par exemple. 
La différence c’est que chaque composant d’une application est différent de tous les autres contrairement aux rivets qui se ressemblent tous. 
Chaque composant d’un logiciel est “cousu main”. Il est impossible de remplacer un contrôleur qui bug par un autre contrôleur par exemple.

> Une autre différence fondamentale c’est le fait que sur un pont si vous percez un trou de 1 cm de profondeur dans un de ses piliers, 
il y a très peu de chance qu’il s’écroule. Par contre si vous enlevez un seul caractère dans un seul fichier de votre logiciel 
en production celui-ci peut cesser totalement de fonctionner. Le logiciel est beaucoup plus fragile qu’une construction physique ce qui le rend plus difficile à construire.
D’ailleurs si vous cherchez la cause d’un problème il peut se trouver très loin de l’endroit où l’erreur s’est produite, 
alors que si l’aile d’un avion se détache on est sûr de trouver la cause du problème en allant voir au niveau des fixations. 
Ceci rend le logiciel très difficile à analyser.

### La différence entre les démarches prédictives et adaptives

On le sait assez peu d’ailleurs, le manifeste agile “The Agile Manifesto” 
devait s’intituler “The Adaptive Manifesto” 
mais ce nom n’a pas été retenu pour ne pas le confondre à l’époque 
avec une méthode qui s’appelait “The Adaptive Software Development Methodologie”.

![](/images/developpeur-architecte-agile/spectre-bduf-emergent-design.png){: .center-image }

Il y a deux extrèmes dans la construction logicielle : le B.D.U.F (Big Design Up Front) ou le Cylce en V 
pour les démarches prédictives, et l’”Emergent Design” (ou Conception Emergente) pour les démarches adaptives.

A la première extrémité, le B.D.U.F, on construit un cahier des charges qui contient toutes les exigences du client. 
Puis on rédige des documents, dossiers de spécification, dossier de conception, qui serviront à l’équipe de fabrication. 
Une fois que toutes les briques sont construites on les assemble et on les teste. 
Finalement on met le produit fini dans les mains de l’utilisateur. Tout cela peut prendre plusieurs mois.

A l'autre extrémité on trouve la conception émergente, les exigences arrivent au fur et à mesure, 
on commence par tester, puis on fabrique et enfin… on conçoit.
Ce qui est contre intuitif et très perturbant pour un grand nombre de personnes mais 
c'est la manière la plus efficace de construire du logiciel.

Le secret réside dans le fait que les tests (que l'on appelle aussi spéficications) sont automatisés. 
Ce qui permet de reconcevoir une petite partie de l'application en étant sûr de ne pas avoir impacté le reste.

L’avantage c’est qu’on a un produit fonctionnel très rapidement, qu’on peut le faire évoluer plus facilement et 
l’adapter aux (nouveaux) besoins de l’utilisateur qui en général ne sait pas vraiment exprimer ce qu’il veut tant 
qu'on ne lui a pas donné ce qu'il avait demandé !

Evidemment il n’y a pas juste deux mondes qui s’opposent, ce sont les extrémités d’un spectre avec beaucoup de nuances. 
Je mettrai par exemple la démarche scrum au début de la 2ème partie et la programmation extrême (Extreme Programming) 
entre scrum et le "design émergent".

Vous pouvez ressentir cette différence d’approche du logiciel à chaque fois que vous utilisez une application.
Vous est-il déjà arrivé de passer une commande sur un site et d'être parfaitement en confiance 
(vous savez que vous serez livré dans les délais, que le retour sera remboursé rapidement, etc) et 
à contrario d'en utiliser un autre avec lequel vous vous demandez ce qui va encore vous arriver (retard, remboursement très long, etc).

On encore d'utiliser une application que vous trouvez bien faite et simple à utiliser 
alors que l'application concurrente ressemble à un test de Q.I. !

La raison ce n'est pas que d'un côté il y a les bons penseurs ou les bons concepteurs et de l'autre les moins bons, 
ou que d'un côté il y a des gens qui ont eu les bonnes idées et de l'autre non.

Ce n'est pas le cas du tout. Les ingénieurs ont la même valeur partout. 
Cela dénote juste une approche différente dans la construction du logiciel, d'un côté on a une démarche adaptive 
et de l'autre une démarche prédictive.

![](/images/developpeur-architecte-agile/voyages-sncf-captain-train-min.png){: .center-image }

Par exemple, si vous avez utilisé VoyagesSNCF.com d’une part et Captain Train d’autre part, vous croirez assez 
facilement que le premier à une approche prédictive (en 2014 en tout cas, l'année où j'ai abandonné voyage-sncf.com) 
et l'autre une démarche adaptive. N.B. : j'ai discuté avec des personnes qui ont travaillé dans 
les deux entreprises et ils me l'ont confirmé.

Dans les entreprises où l'on construit le logiciel de manière prédictive on sera structuré 
autour d'une maîtrise d’ouvrage (MOA) et une maîtrise d’oeuvre (MOE) comme pour construire une cathédrale.
Elle aura des cycles longs car cela prend du temps de recueilir tous les besoins et de rédiger tous les dossiers.
Elle aura tendance à piloter par les coûts de fabrication ou de ce qu'elle croit être la fabrication.
Typiquement elle va rechercher les développeurs les moins chers du monde.
En cas d'échec d'un projet elle aura tendance à être encore plus prédictive 
sur le projet suivant (avec encore plus de dossier et de comités de validation).

La conséquence c’est que si, pour améliorer l'expérience utilisateur par exemple, 
il faut modifier la position d’un bouton sur la page d'un site web,
cela prendra plusieurs semaines voire plusieurs mois.

Dans les entreprises où l'on construit des logiciels de manière adaptive on sera structuré autour 
d'équipes pluridisciplinaires (personnes techniques et non techniques) pour être au plus proche des besoins 
des utilisateurs.
On aura des cycles courts pour mettre en production les idées et les corrections le plus vite possible. 
Etsy par exemple, qui est une startup de 400 ingénieurs qui vend en ligne des produits faits main, 
fait jusqu'à 50 déploiements en production par jour.
Les ingénieurs d'Amazon.com quand à eux déploient en moyenne en production toutes les 11 à 12 secondes.
Déplacer un bouton mal placé sur une fenêtre peut se faire dans la journée.

Dans ces entreprises on va piloter par la valeur et en particulier par la création de valeur. 
Mais qu'est-ce que signifie créé de la valeur finalement ? 
De manière générale, c'est améliorer la vie de quelqu'un.
Quand on est une entreprise commerciale, c'est améliorer la vie de ses clients.
Par conséquent même si le coût du développement est plus élevé qu'ailleurs, 
ce qui est important c'est que l'on puisse facilement améliorer la vie de ses clients.

L'échec fait partie de la culture et on sait que l'on va se tromper et faire des erreurs. 
Il est d'ailleurs important de les faire le plus tôt possible (c.f. Fail Fast).
Dans des entreprises comme google par exemple, il y a des cimetières entiers de projets. 
Quelques-un seulement sont des succès.

### Qu'essaient de faire les démarches agile finalement ? et Pourquoi ?

Finalement les pratiques agiles ont pour but de permettre la construction du logiciel non pas par phases mais dans une boucle. 
C'est une boucle de feedback ou aussi appelé boucle d'apprentissage (ou plus généralement itération).

On écrit un peu de code puis on le met entre les mains des utilisateurs pour obtenir du feed-back. 
A partir de ce feed-back on fait évoluer le code et on en ajoute jusqu’à ce que l’utilisateur ait l’application qu’il voulait. 

Ces pratiques vont aussi permettre de favoriser la communication entre l'utilisateur et le développeur.
A noté que plus le développeur est proche (physiquement) de l’utilisateur final, plus ces pratiques sont efficaces.

Enfin on trouvera des pratiques qui permettront aux développeurs de reconcevoir et reconstruire les applications et 
vérifier qu'une modification n'a pas introduit une erreur ailleurs.

C'est le cas du TDD (Test Driven Development ou Test Driven Design), de BDD (Behavior Driven Developpement), 
du Refactoring (techniques de remaniement du code), de l'intégration continue, déploiement continu, etc.

Pourquoi ? Car développer c’est un processus créatif pas un processus de fabrication. 

Un développeur (donc l'ingénieur logiciel) est plus proche d’un compositeur qui crée des nouvelles partitions 
que d’un musicien qui joue des partitions déjà écrites.
Ce n'est pas un traducteur qui traduit un texte d'une langue A vers une langue B mais un écrivain qui doit faire preuve d'imagination.

Dans son article “Hackers and Painter” (qui a aussi donné un livre), Paul graham explique que la démarche intellectuelle 
de la programmation est beaucoup plus proche de celle d'un artiste (e.g. un peintre) que de celle des mathématiciens. 
Il explique aussi, que quand sa startup a été acheté par Yahoo au début des années 2000, 
il s’est aperçu que la société, qui était encore un des géants de l’internet à l’époque, 
séparait la conception de la programmation et ne considérait pas ses ingénieurs logiciels 
comme des créatifs. Ce qui l’a beaucoup surpris. 

Dans le même temps son principal concurrent, Google, laissait à ses ingénieurs une journée par semaine 
pour travailler sur des projets personnels ce qui a donné des applications comme Gmail.
Ce dernier représenterait aujourd'hui 16% de parts de marché contre 3% pour Yahoo! Mail. 
Gmail a aussi beaucoup contribué au succès de google dans le domaine des logiciels en ligne (google agenda, google docs, ...).
Même si ce n'est certainement pas l'unique raison, l’histoire a finalement donné raison à une des deux visions du logiciel.

### Conclusion pour les développeurs et les concepteurs

Pour conclure cette partie, dans un milieu agile, le développeur est aussi le concepteur. 
Il est même l'ingénieur de la construction du logiciel.
C'est lui qui peut créer et adapter le logiciel pour qu'il s'adapte aux besoins des utilisateurs.
Son rôle est donc tout simplement revalorisé.
Chez google d'ailleurs ce sont les ingénieurs logiciels séniors qui ont le plus haut salaire loin devant les managers !

## Qu'est ce qui change pour les architectes en milieu agile ?

### Qu’est ce que l'architecture Logicielle ?

Le terme d’architecture est très difficile à définir clairement. 
C’est sûrement dû au fait qu’il y a plusieurs connotations derrière ce terme.

Commençons par reprendre la définition de l'architecture dans le bâtiment, puisque le terme vient de là. 
L’architecture c’est tout d’abord un art au même titre que la sculpture ou la musique. 
Il est le premier des arts majeurs et se définit comme “l’expression de la culture” (c.f. wikipédia).

![](/images/developpeur-architecte-agile/euratechnologies-min.png){: .center-image }

Cette “expression” se voit très bien sur le bâtiment ci-dessus (Euratechnologies, un site dédié aux technologies à Lille au nord de la France).
On peut remarquer la brique rouge, le beffroi, le toit en dents de scie, les fenêtres hautes, … 
qui font référence à la culture du nord de la France et à l’industrie textile. 
On s’aperçoit aussi que ce n’est pas un lieu de culte ou un lieu d’habitation mais plutôt un lieu pour travailler. 
En bref l’architecture exprime quelque chose, ce qui n’est pas une grande préoccupation quand on fait de l’architecture logicielle.

L’architecture inclut aussi l’aménagement des espaces pour que l’expérience utilisateur soit optimum sur le lieu (la lumière, la taille des couloirs, …). 
L’équivalent en informatique serait l’UX Designer (UX = User eXperience) (le concepteur de l’expérience utilisateur).

Toutefois, quand le bâtiment atteint une certaine taille, l’architecte ne sait pas nécessairement comment le bâtiment 
va tenir debout.
En effet ce rôle n’est pas forcément du ressort de l’architecte mais plutôt d’un ’ingénieur structure qui va par exemple déterminer 
la position des murs porteurs, leur épaisseur, etc. 
Ainsi quand on parle d’architecture logicielle on devrait plutôt parler d'ingénierie des structures logicielles.

Remarque : La France considère les architectes comme des artistes. Ils sont rattachés au ministère de la culture. 
Ils ont d'ailleurs peu de notions sur l'ingénierie des structures dans leur formation.
Dans d'autres pays comme l'Allemagne l'architecte est aussi un ingénieur structure, ce qui ajoute à la confusion. 

Voici un exemple de structure logicielle :

![](/images/developpeur-architecte-agile/architecture-evolutive-2005-min.png){: .center-image }

Cette structure est, comme toute bonne discipline d'ingénierie, une documentation. 
Mais encore une fois cette documentation ne peut pas être donnée à une équipe de fabrication.
C'est plutôt un support de communication qui servira à la discussion autour d'une table.

La structure logicielle au-dessus est une structure en couches. Chaque couche a une responsabilité.
La couche du haut va gérer les interactions avec les utilisateurs (prendre une commande par exemple), 
les couches du milieu vont traiter et stocker des informations (calculer le montant de la commande et l’enregistrer par exemple) 
et enfin la couche du bas va permettre des analyses et répondre à des questions (combien ai-je eu de commandes ce mois-ci ?).

Une structure logicielle se représente sur plusieurs couches.
Si on peut prend un peu de recul et on peut voir les couches front office / back office / décisionnel. 
Cette structure est très classique des entreprises.
On peut aussi descendre dans une brique et y trouver une sous-structure logicielle comme le MVC (Model-View-Controller).
Souvent cette sous-structure est intégrée dans un framework (c’est le cas du framework rails dans le monde ruby par exemple).

On peut aussi s'intéresser à la répartition du logiciel. Souhaite-t-on le déposer sur une seule machine 
ou sur plusieurs machines qui vont communiquer entre elles. Ce sont des choix d'architecture logicielle 
qui ont leurs avantages et leurs inconvénients.

Mais revenons à la strucure initiale et faisons l’hypothèse que la structure logicielle 
au-dessus soit l’architecture de twitter en 2006 (année de sa création) 
Dix ans après cette architecture pourrait ressembler à celle-ci 
(inspiré de "Implications of Tech Stack Complexity for Executives" <a href='#footnote'>[4]</a>):

![](/images/developpeur-architecte-agile/architecture-evolutive-2016-min.png){: .center-image }

Cette application rend toujours le même service (gérer des tweets par exemple) mais son architecture s'est adaptée 
aux nouveaux besoins des utilisateurs ou aux nouveaux défis techniques.

En bref, la structure d'un logiciel évolue, c’est une grande différence avec les bâtiments. 
Une cathédrale, par exemple, possède la même structure qu’il y a 100 ans et aura la même structure dans 100 ans. 
Pensez maintenant à la structure d’une grosse application (ou d’un système applicatif) que vous connaissez. 
Pensez à sa structure il a 5 ans et à sa structure maintenant.
Il est très probable qu’elle ait changé, et il est très probable qu’elle sera encore différente dans 5 ans.

### Qu'est ce que l'architecte logicielle ? Allons plus loin !

Allons maintenant plus loin dans la définition de l’architecture logicielle et du rôle de l’architecte dans une organisation.

L’article le plus intéressant à ce sujet, 
c’est l’article de Martin Fowler “Who Needs an Architect ?” <a href='#footnote'>[2]</a> 
(Qui a besoin d'un architecte ?). 

Martin Fowler est l’auteur de nombreux livres en informatique et en particulier “Patterns Of Enterprise Application Architecture”. 
Il est aussi un des coauteurs du Manifeste Agile et un des inventeurs de la démarche “Extreme Programming”. 
On lui doit aussi le livre “Refactoring” qui marque l’histoire du logiciel en montrant que le code est quelque chose de malléable 
qu’on peut (qu’il faut) remanier en permanence. 
De mon point de vue on pourrait le comparer à Adam Smith un économiste écossais du siècle des lumières considérait 
comme un des pères des sciences économiques modernes.

Cet article qui est très souvent cité dans l’univers de l’architecture logicielle. 
C’est le cas par exemple dans la formation vidéo de Neal Ford (un auteur phare chez Oreilly) sur 
les fondamentaux de l’architecture logicielle (Software Architecture Fundamentals). 
C’est aussi le cas dans dernier livre de Gregor Hohpe “37 Things One Architect Knows”. 
Gregor Hohpe est le coauteur de “Enterprise Integration Pattern” (qui a été signé par Martin Fowler). 
Il a  travaillé sept ans chez Google et il est maintenant architecte chez Allianz (la société d'assurance). 
Son livre explique de manière très intéressante ce qui différencie ces deux types d'entreprises. 

L'article de Martin Fowler, donc, reprend une discussion qu’il a avec Ralph Johnson un professeur d’université 
qui est aussi le coauteur d'un livre très populaire chez les développeurs 
“Design Patterns - Elements of Reusable Object Oriented Software”<a href='#footnote'>[3]</a>.

Martin Fowler et Ralph Johnson discutent du terme "architecture" dans le monde du logiciel et en particulier de sa définition.
La définition officielle de “l’institut des ingénieurs électriciens et électroniciens”, l’lEEE définit l’architecture logicielle comme 
“le plus haut niveau de concept d’un système dans son environnement. L’architecture d’un système logiciel (à un moment donné dans le temps) 
est son organisation ou la structure des composants majeurs qui interagissent à travers des interfaces. Ces composants majeurs se déclinent 
en des composants et des interfaces plus petits”

Ce à quoi Ralph Johnson répond :
« cette définition est complètement buggée. Il n’y a pas de "plus haut concept d’un système". 
Les clients ont d'ailleurs des concepts différents des développeurs et se moquent complètement de la structure des composants majeurs. 
Dans ce cas on devrait dire qu’une architecture est le plus haut niveau de concept que les développeurs ont d’un système. 
Si on oublie les développeurs qui comprennent juste que leur petit morceau, 
l’architecture est alors le plus haut niveau de concept des développeurs experts. 
Finalement, qu’est-ce qui rend un composant majeur ? Il est majeur car les développeurs experts le disent.
Ainsi, une meilleure définition serait : " dans les projets qui réussissent, les développeurs experts possèdent une compréhension partagée 
de la conception du système. Cette compréhension partagée s’appelle l’architecture. Elle inclut la façon dont 
le système est divisé en composant et comment ils interagissent à travers des interfaces. Ces composants sont habituellement 
composés de composants plus petits, mais l’architecture inclut uniquement les composants qui sont compris par tous les développeurs."

En d’autres termes ce n’est pas une architecture qui dessine une équipe, mais une équipe qui dessine une architecture. 
Il ne sert à rien de faire un diagramme d’architecture et essayer d’y faire adhérer les développeurs. Mieux vaut aller voir 
l’équipe et d’essayer de comprendre ce qui est important pour elle, d'extraire cette compréhension partagée pour la mettre 
sous forme de diagramme.

La raison, rajoute Ralph Johnson, c’est que "l’architecture est avant tout une construction sociale qui ne dépend pas juste du logiciel mais 
des parties qui sont considérées comme importantes par un consensus de groupe."
Un bon test pour évaluer l’architecture sur un logiciel ou un système composé de plusieurs logiciels c’est de demander 
à chaque personne de l’équipe de décrire le système avec 3 ou 4 objets. 
Si ce sont les mêmes pour tout le monde alors c’est un bon début sinon cela signifie certainement qu’il n’existe pas de 
compréhension partagée de l’architecture. 

### L'Architecture est couplée à l'organisation : quelques exemples.

Ce qu'il faut comprendre c'est que la structure logicielle (ou architecture logicielle) et la structure sociale (ou organisation) 
sont fortement imbriquées. C'est un corollaire de la loi de Conway<a href='#footnote'>[5]</a> de 1967 qui dit qu'
"une organisation qui conçoit un système concevra un système dont la structure est une copie de la structure de communication de l’organisation"
On préconise d'ailleurs parfois de travailler la structure sociale pour obtenir la structure logicielle que l'on souhaite 
(c.f Inverse Conway Maneuver).

Allons du côté des grandes organisations agiles pour comprendre comment elles définissent leur structure logicielle et leur structure sociale.

Commençons par amazon.com le site de vente en ligne.
L’image ci-dessous représente son architecture de services en 2009 (1400 services)<a href='#footnote'>[6]</a>.
Pensez-vous qu’il y a un grand architecte pour gérer ça ?

![](/images/developpeur-architecte-agile/amazon-service-architecture-min.png){: .center-image }

Y-a-t-il un archiecte pour décider quel service il faut créer, quel service il faut faire évoluer ou supprimer.
Certainement pas, c’est bien trop complexe. 
Ce qui est important par contre ce sont les règles sociales de leur organisation. 
Il y a avant tout une règle de base très importante qui consiste à avoir des équipes qui ne dépassent pas 7 à 8 personnes. 
Des “Two Pizza Teams”, c’est-à-dire des équipes que l’on peut nourrir avec 2 pizzas (au format américain).

Lorsqu’une équipe devient trop grande elle est divisée et si une équipe reste petite trop longtemps elle est fusionnée avec une autre équipe. 
Ces équipes regroupent des profils techniques (des développeurs, ...) mais aussi des profils non techniques (expert métier, ...).

Il existe d'ailleurs chez amazon une autre règle sociale célèbre : "You build it, you run it", qui signifie 
que les développeurs (responsables du 'build' de l'application ) et les opérationnels (responsables du 'run' de l'application)
ne doivent pas être séparés mais travailler ensemble avec un objectif commun. C'est a dire travailler dans la même équipe et 
pouvoir intervenir l'un comme l'autre en cas de problème sur le service.

Une autre particularité c’est que chaque équipe peut utiliser les outils qu’elle veut et ceci est même favorisé.
Ensuite une sélection naturelle s'opère, les meilleurs restent les autres sont abandonnés.
Par exemple à une époque chez amazon.com, il y avait plusieurs outils pour faire du déploiement de code en production.
C’est après quelque temps qu’un des outils, considéré comme le meilleur a été intégré à la plateforme AWS (Amazon Web Service)
pour que toutes les équipes puissent en profiter. On le trouve sous le nom de Code Deploy sur la plateforme.

Une informatique comme celle-ci coute-t-elle plus cher qu'une informatique rationnalisée qui utilise les mêmes outils partout ? 
Oui très certainement, mais elle est plus flexible et compense ses investissements avec une plus grande statisfaction 
de ses ingénieurs qui peuvent ainsi maximiser la satisfaction des clients.

Un autre exemple c’est celui de spotify (une plateforme de musique en ligne), qui a choisi un modèle qui ressemble à celui d’amazon.com, 
c’est-à-dire des petites équipes autonomes et pluridisciplinaires focalisées sur un but commun (le service à rendre au client).
Il y a une équipe qui sera focalisée sur la recherche dans le catalogue et une autre sur la gestion de la playlist, 
une autre du système de paiement, etc<a href='#footnote'>[7]</a><a href='#footnote'>[8]</a>.

![](/images/developpeur-architecte-agile/spotify-feature-teams-min.png){: .center-image }

Cette organisation leur permet une grande agilité et une capacité à résoudre les problèmes très rapidement.

Chaque équipe représente donc physiquement une *brique de l’architecture logicielle* du service Spotify. 
Cette équipe peut-être agile car elle est autonome, pluridisciplinaire avec un but commun.

Le plus difficile c’est de minimiser les dépendances entre les équipes et ceci n’est possible 
qu’en allant sur le terrain pour comprendre comment les équipes fonctionnent et quels sont les mécanismes sociaux pour en extraire l’architecture.

C'est ce que fait Spotify qui interroge régulièrement ses équipes pour savoir si elles ont des dépendances avec d'autres, 
si cela les ralenti où les bloque. Ils essaient alors de les réduire ou même les couper si c'est le cas<a href='#footnote'>[9]</a>.

![](/images/developpeur-architecte-agile/spotify-one-team-min.png){: .center-image }

### Qu'elle est la place de l'architecte dans ce type d'organisation ?

Dans une organisation traditionnelle, l'architecte décide de ce que sont les choses importantes. 
Il est le seul à prendre des décisions en pensant que c’est le seul moyen de garder le système cohérent 
et que chacun doit suivre un plan. Si on le compare à un modèle de distribution des données, on serait plutôt sur un modèle maître/esclave.

Dans une organisation agile, un architecte va plutôt “mentorer” l’équipe de développement en essayant de tacler 
les problèmes avant qu’ils ne deviennent des problèmes sérieux. 
Le matin il travaille avec des développeurs et l’après-midi il participe à l’expression des besoins client sans utiliser des termes techniques. 
Son but c’est d’augmenter l’autonomie de l’équipe afin qu’il ne soit pas un goulet d’étranglement. 
Ici on pourrait dire qu'il est le moyen de communication d’un modèle de distribution pair à pair (peer to peer).

Martin Fowler en conclut alors que “la valeur de l’architecte est inversement proportionnelle au nombre de décisions qu’il prend”. 
Ceci sous-entend en fait que toutes les équipes ne peuvent pas prendre seules des décisions et/ou identifier ce qui est important 
mais le rôle de l’architecte est de faire en sorte que ce soit le cas le plus souvent possible.

Le terme de “décision” est d’ailleurs important ici. Car qu’est-ce qui différencie l’architecture de la conception. 
Les deux sont en fait une suite de décisions (le choix d’un pattern de conception plutôt qu’un autre, le choix d’une architecture distribuée plutôt 
qu’une architecture monolithique ou même le choix d’une technologie de base de données plutôt qu’une autre, etc).
On considère souvent que les décisions d’architecture sont des décisions qu’il faut prendre tôt dans les projets.

La raison c’est que ces décisions, comme par exemple le choix d’une technologie de base de données, sont perçues comme difficiles à changer 
plus tard. Tout comme il est difficile de déplacer un mur porteur à la fin d'une dans une construction.
Or le rôle de l’architecte est justement de faire en sorte que ces décisions soient les moins nombreuses possible ou en tout 
cas que l’on puisse les changer le plus tard possible dans le projet.
Neal Ford dit “The last responsible moment”, on entend aussi parfois le terme de "just in time architecture".

Ainsi une des tâches les plus importantes de l'architecte est de trouver des moyens d'éliminer l'irréversibilité dans la conception des logiciels.
Par exemple si vous pensez qu’il faut construire tout le modèle de la base de données avant de commencer à développer l’application alors 
il faut faire en sorte que ce modèle soit facile à changer tout au long du projet, par petite migration par exemple. Vous éliminez alors 
cette question d’architecture et vous êtes plus agile. De même, si par exemple vous pensez que votre infrastructure sera quelque 
chose susceptible de changer, faites de l’Infrastructure as Code. Les situations sont très nombreuses en réalité.

Il est évident que si les projets sont sur des cycles longs avec des investissements 
à faire tôt et des contrats avec des prestataires,
cela sera difficile voire impossible à appliquer.

### Conclusion pour les architectes

La complexité des logiciels étant croissante nous aurons de plus en plus besoin 
de compétences en architecture logicielle, mais l'architecte dans une organisation agile n'est pas un point central.
Il doit faire en sorte que les équipes aient besoin 
de lui le moins souvent possible. 
Il doit les rendre autonomes pour ne pas les ralentir.
Il doit aussi faire en sorte que les décisions 
les plus difficiles à changer (les décisions d'architecture)
deviennent des décisions faciles à changer ou 
en tout cas des décisions qui seront prises au moment où il y a assez d'informations pour le faire.

<div class = 'footnote-list'>
  <div id = 'footnote'>
    <span>1: </span>
      <a href="http://www.developerdotstar.com/mag/articles/reeves_design.html">What is sofware design ?</a> par Jack W. Reeves (1992)
  </div>
  
	<div id = 'footnote'>
	<span>2: </span>
	<a href="http://martinfowler.com/ieeeSoftware/whoNeedsArchitect.pdf">« Who Needs an Architect ?»</a>, par <a href='http://martinfowler.com'>Martin fowler</a> (Juillet/Août 2003)

	<div id = 'footnote'>
	<span>3: </span>
  <a href="https://www.amazon.fr/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612/ref=sr_1_1?ie=UTF8&qid=1477981090&sr=8-1&keywords=design+patterns">Design Patterns: Elements of Reusable Object-Oriented Software</a> par Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides

	<div id = 'footnote'>
	<span>4: </span>  
  <a href="https://www.thoughtworks.com/insights/blog/implications-tech-stack-complexity-executives?utm_campaign=transformation&utm_medium=social&utm_source=twitter">Implications of Tech Stack Complexity for Executives</a> par Jim Highsmith, Mike Mason, Mike Mason

	<div id = 'footnote'>
	<span>5: </span>  
  <a href="https://en.wikipedia.org/wiki/Conway%27s_law">La loi de Conway</a> Wikipedia
  
	<div id = 'footnote'>
	<span>6: </span>  
  <a href="https://pages.awscloud.com/rs/112-TZM-766/images/summit-paris-16-track2-session1.pdf">Innovation @ Amazon</a> au AWS Summit 2016 | Paris
  
	<div id = 'footnote'>
	<span>7: </span>  
  <a href="https://labs.spotify.com/2014/03/27/spotify-engineering-culture-part-1/">Spotify Engineering Culture (part 1)</a> par Henrik Kniberg
  
	<div id = 'footnote'>
	<span>8: </span>  
  <a href="https://labs.spotify.com/2014/09/20/spotify-engineering-culture-part-2/">Spotify Engineering Culture (part 2)</a> par Henrik Kniberg

	<div id = 'footnote'>
	<span>9: </span>  
  <a href="https://ucvox.files.wordpress.com/2012/11/113617905-scaling-agile-spotify-11.pdf">Scaling Agile @ Spotify</a> par Henrik Kniberg & Anders Ivarsson
</div>