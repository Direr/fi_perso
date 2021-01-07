---
description: >-
  La simulation de son patrimoine et de sa capacité d'épargne est une étape
  préalable à une bonne allocation de sa richesse.
---

# Tout commence par un grand inventaire

Au programme :

* [x] Distinguer le patrimoine de la richesse intertemporelle
* [x] Simuler les différentes composantes de la richesse sur le cycle de vie
* [x] Comptabiliser un patrimoine immobilier acheté à crédit

#### Simuler sa capacité d'épargne

Une simulation de son épargne consiste à projeter le capital détenu jusqu'à une échéance choisie, sous une hypothèse de rendement, et en ajoutant chaque année l'épargne de la période. Il existe un grand nombre de simulateurs en ligne, par exemple celui de [Cardif](https://www.cardif.fr/placement-epargne/simulation-epargne), ou du [Crédit Mutuel](https://www.creditmutuel.fr/fr/simulations/epargne.html). La plupart de ces simulateurs ont pour objectif d'évaluer la capacité de l'épargnant à réaliser un projet précis ou sont attachés à un produit d'épargne particulier. Nous proposons notre propre [simulateur de patrimoine](https://direr.shinyapps.io/R_shiny_blog_01/). Notre objectif étant de simuler le patrimoine global de l'épargnant sur son cycle de vie, nous ne distinguons pas différents projets ou produits d'épargne.

Comme vu précédemment, l'épargnant détient des "droits" sur deux catégories différentes de richesse : 1\) le patrimoine $$w_0$$ et 2\) la richesse potentielle issue de ses revenus futurs :

$$
Y_0= (1+r)^{-1} y_1 + (1+r)^{-2} y_2 + ... + (1+r)^{-T} y_T
$$

Les deux composantes forment la richesse intertemporelle : $$W_0 = w_0 + Y_0$$ . Afin de simuler le patrimoine présent et futur, nous devons légèrement réécrire l'identité intertemporelle : $$w_0 + Y_0 = C_0 + S_0$$. Soustrayons des deux côté la valeur actuelle de la consommation : $$S_0 = w_0 + (Y_0 - C_0)$$ . En notant $$s_t = y_t - c_t$$ l'épargne de la période t, nous obtenons une expression intuitive de la **richesse intertemporelle**, c'est à dire le patrimoine auquel sont ajoutés les flux d'épargne futurs actualisés :

$$
S_0 =w_0 + (1+r)^{-1} s_1 + (1+r)^{-2} s_2 + ... + (1+r)^{-T} s_T
$$

Comment évolue la composition de l'épargne intertemporelle au cours du cycle de vie ?

Pour le voir, laissons s'écouler une année. L'épargnant a accumulé la richesse supplémentaire $$w_1 = (1+r) w_0 + s_1$$. Dans le même temps, sa richesse future est diminuée d'une année d'épargne :

$$
S_1 = w_1 + (1+r)^{-1} s_2 + (1+r)^{-2} s_3 + ... + (1+r)^{-(T-1)} s_T
$$

Une fraction de la richesse potentielle s'est en effet convertie en patrimoine. Après deux années, il dispose de $$w_2 = (1+r)^2 w_0 + (1+r) s_1 + s_2$$ et sa richesse intertemporelle est :

$$
S_2 = w_2 + (1+r)^{-1} s_3 + ... + (1+r)^{-(T-2)} s_T
$$

A la fin de la période d'accumulation, son épargne intertemporelle est composée en totalité de son patrimoine :

$$
S_T = (1+r)^T w_0 + (1+r)^{T-1} s_1 + (1+r)^{T-2} s_2 + ... +  s_T
$$

En reprenant l'exemple numérique de Pierre \(épargne annuelle de 11 000 euros, 1 % de rendement, progression de l'épargne de 1 % chaque année et un horizon de 30 ans\), la Figure 1 indique l'évolution de la richesse et de ses deux composantes sur le cycle de vie de l'épargnant, la patrimoine $$w_t$$ et l'épargne future actualisée.

**Figure 1** Composition de la richesse au cours du cycle de vie 

![](https://i.ibb.co/2Mf5c12/composition.png)

En début de cycle de vie, l'épargnant dispose essentiellement d'une richesse potentielle qu'il convertit progressivement en patrimoine. La richesse intertemporelle et le patrimoine augmentent de façon légèrement exponentielle en raison de la capitalisation des intérêts. Même un rendement de 1 % sur le patrimoine est une source non négligeable de richesse une fois capitalisé sur 30 ans. La richesse finale serait de 416 500 euros avec un rendement nul au lieu de 485 000 euros avec un rendement positif.

Comme rien ne remplace l'expérience personnelle, vous pouvez simuler vous-même votre patrimoine et ses deux composantes sur [l'application dédiée](https://direr.shinyapps.io/R_shiny_blog_01/).

### Annexe

#### Patrimoine et emprunt immobilier

La richesse intertemporelle prend une signification particulière dans le cadre d'un emprunt immobilier. Elle constitue les "fonds propres" de l'acheteur dont la fonction est de sécuriser l'emprunt consenti par la banque. Notons I __la valeur du bien immobilier acquis, $$D_0$$ la partie financée par crédit bancaire et $$a_0$$ l'apport de l'emprunteur : $$I = a_0 + D_0$$. Le bilan financier de l'emprunteur intègre à l'actif le bien immobilier, la patrimoine financier $$w_0$$ après déduction de l'apport $$a_0$$ et la richesse future, actif non échangeable mais dont le prix est évalué par la somme actualisée de l'épargne future :

| Actif | Passif |
| :--- | :--- |
| Richesse future $$(Y_0 -C_0)$$   Bien immobilier $$(I)$$   Patrimoine $$(w_0 - a_0)$$  | Fonds propres $$(S_0)$$   Dette $$(D_0)$$   $$\,$$  |

Côté passif, nous retrouvons la dette bancaire ainsi que la richesse intertemporelle $$S_0$$ de l'individu. Par définition comptable, cette dernière composante mesure la richesse totale de l'individu inscrite à l'actif nette de ses dettes : $$S_0 = (Y_0 - C_0) + I (w_0 - a_0) - D_0$$ , elle représente d'une certaine façon ses fonds propres.

Reprenons l'exemple d'un épargnant âgé de 35 ans disposant d'un patrimoine de 30 000 euros, dont les revenus annuels nets sont de 36000 euros et ses dépenses de 25 000 euros. Son épargne est donc $$s_0$$ = 11 000 euros, laquelle progresse de 1 % chaque année. La banque lui accordera, après étude de son dossier

$$
D_0 = (1+r^d)^{-1} s_1 + (1+r^d)^{-2} s_2 + ... + (1+r^d)^{-T'} s_{T'}
$$

En supposant un taux du crédit de 2 % et une durée de remboursement de 20 ans, la banque lui accordera $$D_0$$ = 199 000 euros . Le montant du crédit est déterminé selon la même méthode de calcul que celle de la capacité d'épargne $$S_0 - w_0$$ qui aboutissait à un montant de 330 000 euros. L'écart provient de deux différences : la capacité de remboursement de l'emprunteur est calculé sur 20 ans et non 30 ans et le taux qui actualise l'épargne future est le taux du crédit de 2 % et non le rendement de l'épargne d'1 %.

