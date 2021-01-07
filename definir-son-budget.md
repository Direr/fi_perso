---
description: >-
  Un plan financier débute par une estimation du budget de cycle de vie,
  incluant l'ensemble des ressources et des dépenses, présentes et à venir.
---

# Définir son budget pour le reste de sa vie

Au programme :

* [x] Comprendre la notion de contrainte budgétaire intertemporelle
* [x] Définir la richesse intertemporelle
* [x] Simuler le patrimoine

Nous avons vu dans un précédent billet qu'il était possible d'évaluer ses ressources intertemporelles jusqu'à une date T éloignée :

$$
W_0= w_0 + (1+r)^{-1} y_1 + (1+r)^{-2} y_2 + ... + (1+r)^{-T} y_T
$$

sachant que $$w_0$$ est le patrimoine actuel, $$y_t$$ est le revenu perçu l'année t et _r_ le rendement obtenu sur ses placements. Nous avons également vu que les ressources intertemporelles pouvaient s'interpréter comme une somme d'argent dont nous disposerions dès aujourd'hui en remplacement des revenus futurs et qui nous permettrait de financer nos dépenses jusqu'à l'année T. Grâce à cette somme 'pré-acquise', nous pourrions 'pré-acheter' tous les biens et services que nous souhaitons consommer. Nous obtenons alors une égalité entre les ressources et les emplois de cycle de vie au sein d'une seule égalité budgétaire dans laquelle toutes les opérations futures sont actualisées.

#### La prise en compte des dépenses

En notant $$c_t$$ la consommation de l'année t, l'intégralité des consommations est agrégée selon le même procédé que pour ses ressources intertemporelles, en actualisant les flux à toutes les dates futures :

$$
C_0= c_0 + (1+r)^{-1} c_1 + (1+r)^{-2} c_2 + ... + (1+r)^{-T} c_T
$$

Nous pouvons imaginer la consommation intertemporelle comme une longue **liste de courses** dans laquelle l'individu note l'ensemble des biens et services qu'il planifie d'acheter pendant les T prochaines années : ses dépenses de logement, de transport, d'alimentation, de loisirs et vacances etc...

Si nous reprenons l'exemple numérique de Pierre et supposons que ses dépenses annuelles sont de 25 000 euros puis progressent au rythme annuel de 1 %, sa consommation totale actualisée sera $$C_0$$ = 750 000 euros.

#### L'égalité budgétaire intertemporelle

De la même manière que l'épargne est la différence entre le revenu et la consommation \($$S_t = y_t - c_t$$\), la **richesse intertemporelle** est la différence entre les ressources intertemporelles et les dépenses intertemporelles : $$S_0 = W_0 - C_0. $$ Nous montrons dans l'annexe que la richesse intertemporelle est simplement le patrimoine final actualisé : $$S_0 = (1+r)^{-T} w{T+1}$$.

 L'égalité des ressources et emplois annuels $$y_t - c_t + s_t$$ ne signifie pas que l'individu est contraint chaque année de dépenser ses revenus dans la mesure où son épargne \($$s_t >0$$\) ou sa désépargne \($$s_t < 0$$\) lui permet de dissocier son revenu de sa consommation. De la même manière, l'égalité emplois-ressources $$W_0 = C_0 + S_0$$ sur le cycle de vie est une égalité comptable plus qu'une contrainte budgétaire. L'individu est pourtant bien soumis à une contrainte budgétaire qui lui impose de ne pas laisser de dettes à son décès. C'est pourquoi les banques ne prêtent plus aux individus à partir d'un certain âge, car la probabilité de décès rend le risque de défaut trop important. La contrainte budgétaire signifie dans le cas présent $$C_0 \leq W_0$$ ou encore $$S_0 \geq 0$$ si T projette l'individu au vieil âge.

L'égalité comptable $$W_0 = w_0 + Y_0 = C_0 + S_0$$ peut s'écrire sous la forme d'un "compte de résultat" qui recense tous les flux à venir, perçus ou dépensés sur le cycle de vie :

| Emplois | Ressources |
| :--- | :--- |
| Consommations $$(C_0)$$   Épargne $$(S_0)$$  | Patrimoine $$(w_0)$$   Richesse future $$(Y_0)$$  |

Dans le cas de Pierre, l'égalité budgétaire de cycle de vie s'exprime de la façon suivante :

| Emplois | Ressources |
| :--- | :--- |
| $$C_0 \;$$ 750 000 €   $$S_0 \; \;$$ 360 000 € | $$w_0 \;\; \; \; \,$$ 30 000 €   $$Y_0 \;$$ 1 080 000 € |

Cette égalité évolue avec le temps. Les revenus actualisés du travail $$Y_0$$ se réduisent d'année en année côté ressources, mais également la somme des consommations restant à financer côté emplois. De plus, l'individu dégage une épargne qui s'ajoute au patrimoine $$w_0$$ , de sortes que l'épargne intertemporelle $$S_0$$ va probablement progresser. A quoi servira cette épargne accumulée ? Elle aura essentiellement trois emplois : 1\) pallier la perte de ressources une fois à la retraite 2\) financer les dépenses du vieil âge \(dépenses médicales, perte d'autonomie, etc.\) et 3\) transmettre un capital à ses descendants.

### Annexes

#### D'où vient la contrainte budgétaire intertemporelle ?

La contrainte budgétaire intertemporelle $$W_0 = w_0 + Y_0 = C_0 + S_0$$ peut être retrouvée à partir des contraintes budgétaires périodiques. Chaque année, le revenu $$y_t$$ et finance la consommation $$c_t$$. Le solde est l'épargne : $$s_t = y_t - c_t$$ qui est aussi par définition la variation du patrimoine d'une année sur l'autre : $$s_t = w{t+1} - (1+r)wt$$. En d'autres termes, le patrimoine capitalisé $$(1+r) w_t$$ et le revenu $$y_t$$ financent conjointement la consommation $$c_t$$ de la période et la nouvelle valeur du patrimoine $$w{t+1}$$. La contrainte budgétaire s'écrit la première année $$c_0 + w_1 = y_0 + w_0$$ puis :

$$
c_1 + w_2 = y_1 + (1+r) w_1 \\
c_2 + w_3 = y_2 + (1+r) w_2 \\
... \\
c_T + w_{T+1} = y_T + (1+r) w_{T} \\
$$

Actualisons les contraintes budgétaires à la date 0. La première égalité est divisée par $$1+r$$, la seconde par $$(1+r)^2$$, etc... :

$$
c_0 + w_1  = y_0 + w_0 \\
(1+r)^{-1} c_1 + (1+r)^{-1}  w_2 = (1+r)^{-1} y_1 + w_1 \\
(1+r)^{-2} c_2 + (1+r)^{-2} w_3 = (1+r)^{-2} y_2 + (1+r)^{-1}  w_2 \\
... \\
(1+r)^{-T} c_T + (1+r)^{-T} w_{T+1} = (1+r)^{-T} y_T + (1+r)^{-T+1}  w_T \\
$$

Ces T+1 égalités peuvent être additionnées de chaque côté pour n'obtenir qu'une seule contrainte intertemporelle $$C0 + (1+r)^{-T} w{T+1} = Y0 + w_0$$_._ L'épargne actualisée est la richesse accumulée à la date terminale actualisée à la date d'aujourd'hui : $$S_0 = (1+r)^{-T} w{T+1}$$.

