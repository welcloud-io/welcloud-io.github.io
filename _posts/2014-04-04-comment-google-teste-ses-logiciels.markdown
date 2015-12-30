---
layout: post
title : Comment Google teste ses logiciels ?
author: Olivier Lemaitre
categories: Agile
---

Le seul moyen pour qu’une équipe écrive un logiciel de qualité c’est de rendre l’équipe entière responsable de la qualité. 
C'est-à-dire le responsable du produit, les développeurs, les testeurs…tout le monde. 
C'est avec ce message que commence le livre « How Google Tests Software ?»<a href='#footnote'>[1]</a>.
Cet article en reprend les meilleurs extraits.



Google n’a pas toujours eu une organisation pour tester ses logiciels.
Tournez l’horloge six ans en arrière (en 2006, le livre date de 2012), et Google était comme les entreprises pour 
lesquels on a travaillé au moins une fois : le test était une discipline en dehors des préoccupations principales. 
ses adeptes étaient sous-estimés et avaient beaucoup de travail (ils étaient surmenés).
On utilisait en grande partie des processus manuels et les gens assez bons pour les automatiser étaient 
rapidement absorber par l’ équipe de développement où ils pouvaient avoir plus d’impact.  
L’équipe fondatrice de ce que Google appelle « la productivité de l’ingénierie » a dû surmonter les préjugés sur les tests 
ainsi qu'une culture d’entreprise qui favorisait l’effort héroïque plutôt que la rigueur de l’ingénieur. 
A ce jour, les testeurs chez Google sont payés sur la même échelle que les développeurs avec 
des bonus équivalents et ils ont la même vitesse d’évolution. Le fait que la culture des tests ait eu du succès et 
qu’elle ait survécu à travers une croissance significative et des réorganisations structurelles 
devrait encourager d’autres entreprises à suivre les traces de Google.

Google est une entreprise construite sur l’innovation et la vitesse. 
Elle livre du code au moment où c’est utile (quand il y a peu d’utilisateurs à décevoir) et 
elle itère sur les fonctionnalités avec ses « early adopters ». 
Nous sortons des applications classiques comme chrome toutes les quelques semaines 
et nos applications web changent tous les jours même si notre crédit de startup a expiré depuis longtemps.

L’approche de Google est plus que contre intuitive : nous avons moins de testeurs dédiés à 
cette tâche dans l’entreprise tout entière qu’en ont beaucoup de nos concurrents  sur une seule équipe produit. 
Le test chez Google ce n’est pas une armée d’un million d’hommes. Nous sommes une petite force spéciale d’élite qui se repose sur 
des tactiques de haut niveau et d’armes de pointe pour supporter une chance de succès.  Comme pour les forces spéciales de l’armée, 
c’est cette pénurie de ressources qui forme la base de notre sauce secrète. L’absence d’abondance nous force à devenir bon pour prioriser, 
ou comme le dit Larry Page: « la pénurie entraine la clarté ». La pénurie rend aussi les ressources de test d’une très grande valeur, 
gardant les gens brillants impliqués dans la discipline.
Le premier conseil que je donne aux gens quand ils me demandent la clé de notre  succès : n’embauchez pas trop de testeurs.

Comment Google s’en sort avec un si faible nombre de testeurs ? Si je devais le dire simplement, je dirais que chez Google, 
le fardeau de la qualité est sur les épaules de ceux qui écrivent le code. 
La qualité n’est jamais le problème d’un « quelconque testeur ». 
Tous ceux qui écrivent du code chez Google sont des testeurs, et la qualité est littéralement le problème de ce collectif. 
Parler d’un ratio développement/test chez Google, c’est comme parlé de la qualité de l’air sur la surface du soleil. 
C’est un concept qui n’a pas de sens. 
Si vous êtes un ingénieur, vous êtes un testeur. 
Si vous êtes un ingénieur avec le mot « test » dans votre titre alors vous facilitez les tests pour les ingénieurs qui ne l’ont pas.

![](/images/comment-google-teste-ses-logiciels.png){: .center-image }

- « C’est difficile de couvrir 100%, mais c’est ce que nous essayons de faire. »
- « Je m'en moque s'il y a une fonctionnalité sympa en plus. Je veux juste que ce produit soit solide comme un roc.»

Une autre clé qu’utilise Google pour arriver à de bons résultats avec beaucoup moins de testeurs que d’autres entreprises 
c’est de ne sortir que très rarement un large éventail de fonctionnalités en une seule fois. 
En fait, le but c’est de faire exactement le contraire : construire le cœur du produit et le sortir au moment où il est utile au plus grand nombre. 
Alors nous prenons les feedbacks et nous itérons. C’est ce que nous avons fait pour gmail qui est resté en version bêta durant des années.
Google construit donc souvent le “produit minimum utile” comme version initiale et itère rapidement des versions successives. 
Ceci permet d'avoir des retours en interne et des retours d’utilisateurs mais aussi de prêter une attention particulière sur la qualité à chaque petit pas. 


#*Le rôle d'Ingénieur Logiciel*


L’Ingénieur Logiciel (Software Engineer) est le rôle traditionnel de développeur. 
Les Ingénieurs Logiciel écrivent du code fonctionnel à destination des utilisateurs. 
Ils documentent la conception, choisissent la structure des données et l’ensemble de l’architecture. 
Ils passent une grande majorité de leur temps à écrire et revoir du code. 
Les Ingénieurs Logiciel écrivent beaucoup de code pour tester. Ils font de la conception pilotée par les tests (TDD – Test Driven Design) 
et participent à la construction des petits, moyens et grands tests. 
Ils sont responsables de la qualité du code s’ils l’écrivent, le corrigent ou le modifient :
si un Ingénieur Logiciel modifie une fonction et que cette modification casse un test existant ou en demande un nouveau, 
il devient auteur ce code et de ce test. Les Ingénieurs Logiciel passent presque 100 pourcents de leur temps à écrire du code.


#*Le rôle d'Ingénieur Logiciel en Test*


L’Ingenieur Logiciel en Test (Software Engineer in Test) est aussi un rôle de développeur, excepter qu’il se concentre sur la testabilité. 
Les Ingenieurs Logiciel en Test revoient la conception et regardent de très près la qualité du code et le risque. 
Ils remanient le code pour le rendre plus testable. 
Ils écrivent des frameworks de tests et automatisent des batteries de tests. Ils partagent la base de code de L'Ingenieur Logiciel (Software Engineer), 
mais sont plus concernés par l'augmentation de la qualité et de la couverture de test que par l’ajout de 
nouvelles fonctionnalités ou l'accroissement des performances. 
Les Ingenieurs Logiciel en Test passent près de 100 pourcents de leur temps à écrire du code aussi, mais ils le font au service de la qualité plutôt que 
des fonctionnalités que les utilisateurs vont utiliser. En résumé, Les Ingenieurs Logiciel en Test écrivent du code qui permet 
aux Ingenieurs Logiciel de tester leurs fonctionnalités.


#*Le rôle d'Ingénieur de Test*


L’Ingénieur de Test (Test Engineer) est en relation avec le rôle de d'Ingénieur Logiciel en Test, mais il a une préoccupation  différente. 
C’est un rôle qui met le test au niveau de l’utilisateur d’abord et du développeur ensuite. 
Certains Ingénieurs de Test chez Google passent une bonne partie du temps à écrire du code sous la forme de scripts d’automatisation. 
Du code qui anime les scénarios d’utilisation et qui parfois même imitent le comportement de l’utilisateur. 
Ils organisent le travail de test des Ingenieurs Logiciel et des Ingenieurs Logiciel en Test puis pilotent l’exécution des tests et interprètent les résultats. 
Ils interviennent particulièrement dans les dernières étapes d’un projet quand la pression vers la mise en production s’intensifie. 
Les Ingénieurs de Test sont des experts, consultants en qualité, et analyseurs de risques. Beaucoup d’entre eux écrivent beaucoup de code, 
beaucoup d’entre eux en écrivent juste un peu.


#**La différence entre les _Ingénieurs Logiciel en Test_ et les _Ingénieurs de Test_ par Hason Arbon.**


Le rôle des Ingénieurs Logiciel en Test et des Ingénieurs de Test sont liés mais différents sur des points fondamentaux. 
J’ai été les deux et j’ai encadré les deux. Regardez les listes qui suivent et trouver la description qui vous convient le mieux. 
Peut-être devriez-vous changer de rôle.


Vous pourriez être un Ingénieurs Logiciel en Test si :

- Vous pouvez prendre une spécification, un tableau blanc et imaginer une solution solide et efficace.
- Quand vous codez, vous culpabilisez en pensant à tous les tests unitaires que vous devriez coder. 
Alors vous finissez par imaginer toutes les façons de générer le code qui servira pour les tests et les validations pour éviter de le faire à la main.
- Vous pensez qu’un utilisateur final est quelqu’un qui fait des appels d’API.
- Vous devenez grincheux si vous lisez une documentation d’API mal écrite.  Vous oubliez parfois pourquoi l’API est intéressante en premier lieu.
- Vous vous retrouvez à avoir des conversations de geek sur l’optimisation du code ou sur la recherche de situation de compétitions dans les logiciels multitâches.
- Vous préférez communiquer avec les autres êtres humains par un canal IRC ou par les commentaires dans les « commits » de votre code source.
- Vous préférez une ligne de commande à une interface utilisateur et vous touchez rarement la souris.
- Vous rêvez de systèmes qui exécutent votre code à travers des centaines de machines pour tester des algorithmes – démontrant qu’ils sont corrects par pur nombre de cycles CPU et de paquets réseau.
- Vous n’avez jamais remarqué ou personnalisé votre bureau virtuel sur votre machine.
- Le fait de voir des « warning » à la compilation vous rend anxieux.
- Quand on vous demande de tester un produit, vous ouvrez le code source et vous commencez à réfléchir à ce qui peut être « mocké ».
- Votre idée du leadership est de construire un super framework de tests unitaires de bas niveau dont tout le monde tire avantage ou 
qui est exécuté des millions de fois par jour sur un serveur de test.
- Quand on vous demande si le produit est prêt à être mis en production, vous pourriez juste dire : « Tous les tests passent».

Vous pourriez être un Ingénieurs de Test si :

- Vous pouvez prendre un code existant, regarder les erreurs et immédiatement comprendre le mode d’échec  probable de ce logiciel, mais vous n’avez pas forcément envie de le recoder depuis zéro ou faire des modifications.
- Vous préférez lire Slashdot ou News.com que de lire le code des autres toute la journée.
- Vous lisez la spécification d’un produit à moitié terminée, vous prenez sur vous et comblez les lacunes dans le document.
- Vous rêvez de travailler sur un produit qui créera un large impact dans la vie des gens, et que les gens reconnaissent le produit sur lequel vous travaillez.
- Vous êtes consterné par l’interface graphique de certains sites et vous demandez comment ils ont pu un jour avoir des utilisateurs.
- Vous êtes emballé à l’idée de visualiser des données.
- Vous ressentez le besoin de parler à gens au moment du repas.
- Vous ne comprenez pas pourquoi vous devez taper « i » avant de commencer à écrire dans un certain éditeur de texte.
- Votre idée du « leadership » c’est de nourrir les idées des autres ingénieurs et de défier les leurs avec un ordre de magnitude de plus grande échelle.
- Quand on vous demande si le produit est prêt pour la production, vous pourriez dire : « Je pense que c’est prêt ».

Il est important pour les testeurs de savoir qui ils sont. 
Souvent, les Ingénieurs de Test sont simplement vu comme des Ingénieurs Logiciel en Test qui ne codent pas autant ou aussi bien. 
La réalité c’est qu’ils voient des choses que les gens avec la tête dans le code toute la journée ne verront jamais. 
Les _Ingénieurs Logiciel en Test_ devraient aussi  réaliser qu’ils ne sont pas des <i>Ingénieurs de Test</i> et ne pas se sentir coupables ou se mettre la pression 
pour trouver des problèmes dans l’interface utilisateur, penser au système dans son ensemble ou à imaginer des produits compétitifs.
Ils doivent se concentrer à la place sur des modules réutilisables, testables, de très haute qualité ainsi que sur des automatisations qui impressionnent. 
Il faut des familles de testeurs diverses pour sortir un produit hors norme.


<div class = 'footnote-list'>
	<div id = 'footnote'>
	<span>1: </span>
	<a href="http://books.google.fr/books/about/How_Google_Tests_Software.html?id=vHlTOVTKHeUC&redir_esc=y">How Google Tests Software</a> (2006), par James Whittaker, Jason Arbon et Jeff Carollo

	</div>
</div>	  

