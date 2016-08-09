---
layout: post
title : Qu'est-ce que la conception logicielle ?
author: Olivier Lemaitre
categories: Ingenieirie
---

Même si l'article de Jack Reeves "What is software design ?"<a href='#footnote'>[1]</a> date de 1992, il donne d'impression d'avoir été écrit il y a quelques semaines. 
A cette époque c'était l'explosion des langages orientés objet (en particulier le C++) et pour expliquer ce succès l'auteur fait une hypothèse.
Celle-ci va énormément influencer les démarches agiles ainsi que les ingénieurs logiciels qui les utilisent.

Cette hypothèse c'est que les langages orientés objet sont devenus populaires car ils permettent de concevoir et programmer en même temps.
L'industrie du logiciel est passée à coté d'une subtilité dans le métier de l'ingénierie logicielle. En fait, programmer ce
n'est pas construire un logiciel. Programmer c'est concevoir un logiciel.

# Pourquoi programmer c'est concevoir ?

Le but final de n’importe quelle activité d’ingénierie est une forme de documentation. Quand un effort de conception est atteint, 
cette documentation est remise à l’équipe de fabrication. C’est une équipe complètement différente, avec d'autres compétences que celles de l’équipe de conception.
Munis des plans, elle peut alors commencer à fabriquer le produit sans aucune intervention des concepteurs. 
C'est le cas dans le bâtiment ou dans l'électronique par exemple.
 
Dans le logiciel, la seule documentation qui semble permettre cela c’est *l’ensemble du code source*. L'équipe de fabrication étant 
les machines qui exécutent la compilation (pour les langages compilés) et la chaine de déploiement. 
Cette fabrication est donc automatique et ne comporte pas d'intervention humaine.

Un document de conception doit être assez détaillé, assez complet, et suffisamment non ambigu pour qu'il puisse être interprété mécaniquement 
soit par un ordinateur ou les ouvriers d’une ligne d’assemblage. Si cela demande encore une interprétation créative par un humain alors ce n'en est pas un.
De ce point de vue, dans le développement logiciel, le document de conception c'est le code source.

Même s'il existe des notations de conception logicielle “indépendante des langages” (UML par exemple), elles ignorent toute un problème fondamental. 
La conception logicielle implique de traduire les problèmes d’un domaine dans un langage de programmation. 
Cette traduction doit être faite par des humains. Chaque fois que l'on traduit des concepts d’une forme à une autre, en particulier 
les problèmes complexes, nous perdons souvent des informations importantes. Si plusieurs traductions sont impliquées, nous finirons 
très probablement par un produit final qui aura perdu trop d’informations vitales. Fondamentalement, les langages de programmation sont une notation de conception. 
Il n'y a aucun avantage à introduire des étapes de traduction supplémentaires.

# En quoi l'ingénierie logicielle diffère des autres disciplines ?

Quand, dans d'autres disciplines d'ingénierie, les ingénieurs produisent une conception, peu importe sa complexité, ils sont quasiment sûrs que cela va fonctionner. 
Toutefois pour que ce soit possible, les ingénieurs du monde physique prennent un temps considérable à valider et affiner leur conception. 

Pour un pont par exemple, les ingénieurs font une analyse structurelle, ils construisent des modèles sur ordinateur et exécutent des simulations. 
Ils construisent des modèles réduits et font des essais en soufflerie. 
En bref, le concepteur fait tout ce qu’il peut pour être certain que sa conception soit bonne avant la construction.
Ils le font car le produit final est cher à fabriquer. Ils ne peuvent donc pas se permettre de devoir le reconstruire plusieurs fois.

Un logiciel quand à lui ne coûte quasiment rien à fabriquer, donc des méthodes équivalentes de validation de la conception ne sont pas d’une grande utilité.
Il est préférable d'écrire le code et de le tester que d’essayer de prouver qu'une conception est bonne. 
En définitive, la conception d’un logiciel représentée dans un langage de programmation sera validée et affinée à travers un cycle build/test. 

Malheureusement de nombreux processus de développement considèrent que la conception doit être complète et figée avant que la moindre ligne de code ne soit écrite.
Or, bien souvent, même le plus petit morceau de code sera probablement revu voire complètement réécrit durant la phase de test et de débuggage.
D'ailleurs cela va sans dire qu'un document de conception produit après avoir écrit le code, sera bien plus précis qu'un document écrit avant.
 
Beaucoup pensent que si nous pouvions empêcher les programmeurs de “bidouiller” et s’ils pouvaient juste “fabriquer” le logiciel avec la conception qui leur 
a été donnée, alors le développement de logiciels devrait arriver à la maturité d’une véritable discipline d’ingénierie. 
Ce n’est pas prêt d’arriver, car coder est un processus créatif, pas un processus de fabrication.

La conception des logiciels reste un exercice complexe. Elle ressemble à la conception de systèmes. 
Elle peut couvrir de nombreuses technologies et impliquer de nombreuses disciplines. 
Les spécifications changent souvent, les équipes aussi. En définitive le monde du logiciel a plus de liens avec 
des systèmes sociaux ou organiques complexes qu'avec du "hardware". Cela rend sa conception difficile.
Même si fabriquer un logiciel est économique, il est cher à concevoir, donc à coder. 

# Faut-il jeter tous les outils traditionnels de conception ?

Dans l’ingénierie logicielle nous avons besoin d’une bonne conception à plusieurs niveaux. 
Nous avons besoin d’une bonne architecture (top level design), de bonnes abstractions (class design), et de bonnes implémentations (low level design).

Les gens diffèrent énormément sur ce qui les aide à réfléchir. Certains utilisent un crayon et du papier, d’autres un tableau blanc ou encore des outils informatiques. 
Certains ont besoin d'échanger des idées avec d’autres personnes, d’autres préfèrent la paix et la tranquillité. Des personnes se sentent à l’aise avec UML, 
d’autres avec les cartes CRC. L’approche qu’ils choisissent n’a pas d’importance, au final c’est le code qui est important.

Nous devons donc garder à l'esprit que ces outils et ces notations ne sont pas une conception logicielle mais une aide à la conception. 
Nous devrions donc coder au fur et à mesure que nous modélisons et être prêt faire évoluer les choses si nécessaire.
Pour cela il lui faut un langage de programmation qui puisse "capturer" des concepts de haut niveau. 
C’est le cas des langages orientés objets qui permettent d'écrire la conception et la faire évoluer plus facilement qu'avec un langage procédural. 

Nous pouvons aussi avoir besoin d'une documentation auxiliaire. En particulier, certains aspects sont mieux décrits graphiquement et sont donc difficiles à mettre dans le code.
Cela peut concerner des concepts de haut et de bas niveau. Attention, ceci n’est pas un argument pour préférer une notation de conception plutôt qu'un langage de programmation.

# Conclusion

Le véritable logiciel tourne sur l’ordinateur. C’est une séquence de uns et de zéros. le code source n'est pas le logiciel.
Ce code source est plutôt un document qui représente la conception du logiciel. Ce sont les compilateurs et la chaine de déploiement qui le construisent. 
Les étapes avant l'écriture du code ont assez peu d'intérêt dans l'ingénierie logicielle car le produit ne coute pas très cher à fabriquer. 
Il est donc possible d'affiner la conception au fur et à mesure de la construction. Finalement, mieux vaut concentrer ses efforts sur l'écriture du code 
en s'aidant si c'est utile d'outils et de notations pour nous aider à le produire.

<div class = 'footnote-list'>
  <div id = 'footnote'>
    <span>1: </span>
      <a href="http://www.developerdotstar.com/mag/articles/reeves_design.html">What is software design ?</a> de Jack W. Reeves
  </div>
</div>