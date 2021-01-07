---
description: >-
  Un plan financier débute par une évaluation de ses ressources, présentes mais
  aussi à venir.
---

# De combien sommes nous riches ?

Au programme :

* [x] Comprendre la notion de richesse intertemporelle
* [x] Définir et calculer les ressources intertemporelles
* [x] Comprendre leur utilité pour la gestion du patrimoine

La richesse d'un individu ou d'un ménage est constituée non seulement des actifs qu'il détient, son patrimoine, mais aussi des ressources futures qu'il anticipe d'acquérir. Pour le comprendre, commençons par poser quelques notations :

* $$w_0$$ est le patrimoine actuel de l'épargnant
* r est le rendement annuel prévu sur l'ensemble du patrimoine
* $$y_t$$ sont les revenus du travail perçus l'année _t_
* _p_ est le taux de progression annuel du revenu
* T est la date maximale pour laquelle les revenus futurs sont considérés.

Le **patrimoine** couvre l'ensemble des composantes de la richesse : livrets et comptes bancaires, épargne retraite, contrats d'assurance vie, immobilier \(valeur de marché nette de l'endettement résiduel\), compte titres, ...

Le **rendement** du patrimoine est une moyenne pondérée des rendements prévus sur les différentes catégories du patrimoine.  Les **revenus annuels** sont entendus nets de toute fiscalité \(cotisations sociales, impôt sur le revenu, ...\).

L'**horizon** des flux doit être suffisamment long. La date terminale peut correspondre au pic de richesse, le moment où les dépenses sont supérieures au revenu, probablement la date de départ à la retraite, voire au-delà si l'épargnant prévoit de continuer à épargner après la retraite.

Projetons nous dans T années et supposons pour le moment que l'épargnant se borne à accumuler ses revenus sans les dépenser. Ses ressources accumulées sont la somme de son patrimoine initial et de ses revenus capitalisés au taux _r_ \(supposé fixe pour simplifier\) :

$$
(1+r)^T w_0 + (1+r)^{T-1} y_1 + (1+r)^{T-2} y_2 + ... + (1+r) y_{T-1} + y_T
$$

Détaillons la formule. Son patrimoine initial $$w_0$$ est récupéré un an plus tard avec les intérêts $$r w_0$$ soit la somme $$(1+r) w_0$$. Cette somme est ensuite placée au taux _r_ pendant encore un an. L'épargnant obtient donc deux ans plus tard le capital $$(1+r) w_0$$ plus les intérêts sur le capital $$r(1+r) w_0$$ soit $$(1+r)(1+r)w_0 = (1+r)^2 w_0$$ et ainsi de suite. Au bout de T années, le capital initial est devenu $$(1+r)^T w_0$$. Le même raisonnement s'applique au revenu perçu à la fin de la première année etc.

Prenons l'exemple de Pierre, un épargnant âgé de 35 ans disposant d'un patrimoine de 30 000 euros et dont les revenus annuels nets sont de 36 000 euros. Le rendement de son épargne est estimé à 1 % et la progression annuelle de ses revenus également à 1 %. Son horizon de placement est de 30 ans. A l'aide de ces données, nous pouvons calculer ses ressources capitalisées, soit environ 1 500 000 euros. Si le rendement de Pierre sur son épargne n'était pas de 1 mais 3 %, ses ressources seraient d'un peu plus de 2 millions d'euros.

#### Estimer la richesse future

Ses ressources intertemporelles représentnt des sommes conséquentes, mais rappelons nous que Pierre doit financer 30 années de consommation. Ce n'est donc évidemment pas la richesse finale qu'il peut espérer détenir dans 30 ans. C'est pourquoi une perspective probablement plus instructive consiste à évaluer sa richesse totale non pas dans T années mais _dès aujourd'hui_ grâce à la méthode d'actualisation des flux \(voir une présentation en annexe\). Nous dénommons la richesse accumulée pendant T années actualisée à la date d'aujourd'hui ses **ressources intertemporelles** : $$W_0 = (1+r)^{-T}w_T$$ . Cela revient à appliquer l'opération d'actualisation à l'ensemble des flux de revenus de l'équation d'accumulation :

$$
W_0= w_0 + (1+r)^{-1} y_1 + (1+r)^{-2} y_2 + ... + (1+r)^{-T} y_T
$$

 Les ressources intertemporelles sont inférieures aux ressources capitalisées en raison de l'actualisation. Dans l'exemple de Pierre, elles sont égales à 1 10 000 euros, ce qui reste une somme importante.

#### Interprétation et intérêt de la notion de ressources intertemporelles

Les ressources futures actualisées ont une interprétation intéressantes. Elles correspondent à la somme que l'épargnant obtiendrait si un prêteur lui accordait un crédit dont les annuités seraient constituées de ses revenus futurs. Si nous notons $$r^d$$ le rendement demandé par le créancier, la somme qu'il serait disposé à vous prêter est

$$
D_0= (1+r^d)^{-1} y_1 + (1+r^d)^{-2} y_2 + ... + (1+r^d)^{-T} y_T
$$

En effet, le prêteur obtiendrait la même somme finale s'il place $$D_0$$ pendant T années au taux $$r^d$$ ou s'il perçoit les remboursements périodiques $$y_t$$ et les place au taux $$r^d$$ jusqu'en T :

$$
(1+r^d)^T D_0= (1+r^d)^{T-1} y_1 + (1+r^d)^{T-2} y_2 + ... + y_T
$$

Si le coût du crédit $$r^d$$ était égal au rendement _r_ que l'épargnant obtenait sur ses placement, l'identité serait parfaite. Ce scénario reste évidemment une expérience de pensée. Il serait plus réaliste de supposer que le coût financier est supérieur \( $$r^d< r$$\) pour compenser le risque de défaut. Ou que le créancier ne prête qu'à la condition d'acquérir un bien durable qui servirait de garantie sur le prêt. Dans tous les cas, la somme que l'épargnant pourrait convertir en richesse actuelle serait inférieure à ses ressources intertemporelles.

Cet exercice de la pensée reste néanmoins instructif et souligne la nature intertemporelle du concept de richesse. De plus, évaluer ses ressources intertemporelles permet d'adopter une perspective longue de la richesse et de sa dynamique, d'appréhender les bons ordres de grandeur et de planifier l'épargne et le patrimoine au sein d'un cadre temporel approprié. Un épargnant qui gèrerait ses finances sur la seule base de son patrimoine existant et sur un horizon court prendrait le risque d'une gestion à courte vue de ses finances.

### Annexes

#### La technique d'actualisation

L'actualisation est l'opération inverse de la capitalisation. Un euro placé pendant deux ans au taux d'intérêt _r_  permet d'obtenir 1+_r_ euros la première année. Cette somme permet d'obtenir $$(1+r) \times (1+r) = (1+r)^2$$ euros deux ans plus tard. Inversement, si nous retournons la flèche du temps, $$(1+r)^2$$ euros disponibles dans deux ans sont équivalents à 1 euro aujourd'hui. Ou 1 euro dans deux ans est équivalent à $$\dfrac{1}{(1+r)^2} = (1+r)^{-2}$$ euros aujourd'hui. Les deux opérations sont symétriques et représentées dans la Figure 1.

**Figure 1** Capitalisation et actualisation d'un euro sur deux périodes 

![L&apos;actualisation et la capitalisation des flux](https://i.ibb.co/8jgM0bY/actualisation.png)

Dit autrement, 1 euro dans un an est équivalent à $$S=\dfrac{1}{1+r}$$ euro aujourd'hui puisque _S_ euros aujourd'hui permet d'obtenir exactement $$\dfrac{1+r}{1+r}=1$$ euro dans un an. Suivant le même raisonnement, 1 euro dans deux ans est équivalent à $$(1+r)^{-2}$$ euro aujourd'hui.

