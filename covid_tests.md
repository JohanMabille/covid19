# Efficacité des tests de dépistage

## Introduction

En France, à partir du 11 mai 2020, le déconfinement sera accompagné de tests massifs des personnes présentant des symptômes du COVID 19. Or, les résultats de ces tests, ainsi que leur efficacité à divers stades de l'épidémie, sont des sujets souvent méconnus ou mal interprétés, par manque d'explication accessible à tous.

Ces tests, considérés comme prématurés en début de pandémie, sont désormais présentés comme une arme efficace pour lutter contre le virus. Cette affirmation peut paraître surprenante, notamment du fait que certains pays ont choisi de tester leur population très tôt. Et ce, alors que beaucoup de professionnels de santé affirment que des tests massifs, à l'aveugle, sont "inutiles", voire "contre-productifs".

Cet article a pour but d'expliquer, de manière simple, les différentes caractéristiques d'un test de dépistage et comment en interpréter les résultats. Bien qu'appliqués aux tests de dépistage du COVID 19, les raisonnements et résultats de cet article sont transposables à tout test médical (et de manière plus générale, à tout test ayant pour but de détecter une caractéristique spécifique au sein d'une population).

## Caractéristiques d'un test de dépistage

On entend souvent qu'un test de dépistage est efficace à 95% (par exemple). Cette affirmation est imprécise. Il y a en réalité deux nombres à considérer:

- la *sélectivité clinique*: la proportion de résultats positifs dans une population de gens que l'on sait malades. Un test parfait aurait une sélectivité clinique de 100%, autrement dit il n'y aurait pas de faux négatifs (personne testé négativement alors qu'elle est malade).
- la *spécificité clinique*: la proportion de résultats négatifs dans une population de gens que l'on sait non malades. Un test parfait aurait une spécificité clinique de 100%, autrement dit il n'y aurait pas de faux positifs (personne testée positivement alors qu'elle n'est PAS malade).

Ces deux nombres peuvent être très différents. Par exemple, les tests de grossesse ont généralement une très bonne spécificité clinique (il est très improbable qu'une femme qui n'est pas enceinte soit testée positivement), mais une sélectivité clinique moins bonne (il arrive qu'une femme enceinte ait un test de grossesse négatif).

**Imaginons qu'un test de dépistage du covid 19 ait une sélectivité clinique et une spécificité clinique de 95%. Un test positif NE signifie PAS que vous avez 95% de risque d'avoir la maladie.**

Ce risque est en réalité inférieur. Les caractéristiques d'un test permettent de connaître la probabilité d'avoir un test positif ou négatif pour des populations malades ou saines. Cependant, dans la pratique, on souhaite en réalité connaître la probabilité d'être malade en fonction des résultats du test.

La section suivante montre comment on peut calculer, à  partir de ces caractéristiques, le risque d'être réellement malade *sachant que* l'on a été testé positif.

## Exemple 

Considérons une maladie génétique qui touche 1 personne sur 1000 (soit 0.1% de la population). Une population de 1 000 000 de personnes comporte donc 1000 malades et 999 000 personnes saines. On dispose d'un test capable de détecter 80% des malades (*sélectivité de 80%*), et qui génère 5% de faux positif (*spécificité de 95%*).
Si l'on teste le million de personnes suscité, le nombre de résultats positifs peut se décomposer comme suit:

- le nombre de malades détectés par le test: 80% de 1000 malades, soit **800**
- le nombre de personnes saines, faussement détectées: 5% de 999 000 personnes saines, soit **49 950**

Première remarque: le nombre de faux positifs est environ 50 fois plus élevé que le nombre total de malades! Mettons cela de côté pour le moment. 

Le nombre total de tests positifs est donc 800 + 49 950 = **50 750**.
Si je suis testé positif, mes risques d'être réellement malade sont: 

    nombre de cas détectés / nombre total de tests positifs, soit 800 / 50 750 = 1.57%!

Si je suis testé positif, j'ai donc moins de 2% de risques d'être malade. Cela reste certes beaucoup plus élevés que le pourcentage de malades dans la population complète (0.1%), mais nettement inférieur aux 80% de détection du test (souvent considéré à tort comme étant le risque d'être malade en cas de test positif).

Comment améliorer ce test? Le rapport entre malades détectés (800) et faux positifs (49 750) montre qu'augmenter la sensibilité du test ne changera pas grand-chose. En effet, même si le test est capable de détecter tous les malades (soit 1000), ce nombre reste nettement inférieur au nombre de faux positifs. On a donc intérêt agir sur ce dernier.

Imaginons qu'un laboratoire parvienne à faire chuter ce taux de faux positifs à 1% et reprenons les calculs précédents:

- nombre de malades détectés par le test: 80% de 1000 malades, soit **800**
- nombre de faux positifs: 1% de 999 000 personnes saines, soit **9 990**
- nommbre total de tests positifs: 800 + 9 990 = **10 790**
- risques d'être effectivement malade sachant que l'on est testé positif: 800 / 10 790 = **7.41**%

Même si c'est beaucoup mieux que le résultat précédent, on est encore loin d'être sûr d'être malade. Ce genre de tests est en réalité inadapté à la détection de maladie peu fréquentes à cause du nombre élevé de faux positifs.

## Influence du nombre de malades

Considérons à présent une autre maladie, qui touche non plus 1 personne sur 1000, mais 5 sur 100. Une population de 1 000 000 de personnes comporte donc 50 000 malades, et 950 000 personnes saines. Avec les mêmes caractéristiques que le test précédent, on obtient:

- nombre de malades détectés par le test: 80% de 50 000 malades, soit **40 000** 
- nombre de faux positifs: 1% de 950 000, soit **9500**
- nombre total de tests positifs: 40 000 + 9500 = **49 500**
- risques d'être effectivement malade sachant que l'on est testé positif: 40 000 / 49500 = **80.81%**

Ainsi l'efficacité d'un test dépend non seulement de sa capacité à détecter les malades, à ne pas générer de faux positifs, mais également du *pourcentage de la population malade (estimé statistiquement)* : plus ce pourcentage est faible, moins un test positif permet de conclure.

Si un test détecte 95% des malades, l'erreur classique consistant à dire que l'on a 95% de risque d'être malade avec un test positif, est appelé *oubli de la fréquence de base*. Et comme le montre l'exemple précédent, cela amène à surestimer ce risque.

**Autrement dit, si un test de dépistage d'une maladie grave se révèle positif, il est important de se renseigner sur le nombre de faux positifs générés par le test, et sur la part de la population atteinte par la dite maladie, cela permet souvent de relativiser.**

Notons que ce raisonnement est transposable à d'autres domaines, au hasard la surveillance vidéo de masse pour faire diminuer la criminalité. Même si la reconnaissance faciale s'est grandement améliorée ces dernière années, elle continue à générer de nombreux faux positifs, comme le révèlent différentes études menées aux Etats-Unis et au Royaume Uni. Je laisse le soin au lecteur de conclure quant à l'efficité du dispositif pour repérer par exemple les terroristes, dont la part dans la population est *extrêmement faible*.

## Cas du COVID 19

Mais revenons au cas qui nous intéresse, la pandémie actuelle. Les calculs précédents supposent que l'on connaisse déjà la part de la population atteinte en moyenne (la fréquence de base). Or, dans le cas du COVID-19, la maladie est nouvelle, donc on ne connaît pas cette part. Pire, cette part évolue: très peu de gens contaminés au début, puis augmentation qui dépend de nombreux facteurs, comme les mesures de distanciation sociale, la circulation de la population, etc. On estime aujourd'hui qu'entre 3% et 6% de la population française est infectée.

Par ailleurs, la HAS a publié le [cahier des charges](https://www.has-sante.fr/upload/docs/application/pdf/2020-04/cahier_des_charges_test_serologique_covid19.pdf) des tests:

- sensibilité clinique (capacité à détecter les malades) entre 90% et 95%
- spécificité clinique (capacité à ne pas générer de faux positifs) à 98%

La figure ci-dessous permet d'illustrer l'efficacité des tests en fonction de ces données:

- en rouge, les risques d'être effectivement malade suite à un test positif (à gauche) ou à un test négatif (à droite)
- en vert les chance d'être sain

Sous la figure, différents élements de contrôle vous permettent de faire varier les caractéristiques du test et de constater leur influence sur son efficacité. Une explication mathématique plus formelle est fournie après la figure pour ceux qui le souhaitent. Les lecteurs peu férus de maths peuvent sauter directement à la conclusion.

## Démonstration Mathématique

Les résultats exposés en début d'article se retrouvent grâce aux probabilités. Notons A l'évènement "Le test est positif" et B "La personne est malade". On cherche à calculer les chances que l'on a d'être malade sachant que le test est positif. Dit autrement, on cherche à connaître la probabilité de l'évènement B sanchant que l'évènement A s'est réalisé. On note cette probablité p(B/A) (lire probabilité de B sachant A).

Les caractéristiques du test nous fournissent d'autres probabilités:

- sensibilité: probabilité que le test soit positif sachant que la personne est malade, soit p(A/B)
- taux de faux positifs: probabilité que le test soit positif sachant que la personne n'est PAS malade, soit p(A/non(B))

Par ailleurs, le taux de contamination n'est autre que la probabilité d'être malade (indépendamment de tout test), soit p(B).

Le théorème de Bayes (que nous ne démontrons pas ici) dit que p(B/A) x p(A) = p(A/B) x p(B). Ou, écrit autrement,
p(B/A) = p(A/B) x p(B) / p(A).

On connaît déjà p(B) (taux de contamination) et p(A/B) (sensibilité du test), il nous reste à évaluer p(A), c'est à dire la probabilité qu'un test se révèle positif. Lorsque l'on teste une personne au hasard, il y a deux possibilités: soit la personne est malade, soit elle ne l'est pas. On peut ainsi dire que la probabilité qu'un test soit positif se décompose en:
- la probabilité qu'un test soit positif *sachant que* la personne est malade, soit p(A/B)
- la probabilité qu'un test soit négatif *sachant que* la personne n'est pas malade, soit p(A/non(B)).

Autrement dit, c'est la somme de la sensibilité et du taux de faux positifs: p(A) = p(A/B) + p(A/non(B)).

On a donc p(B/A) = p(A/B) x p(B) / \[p(A/B) + p(A/non(B))\]

Dit autrement: p(B/A) = sensibilité x taux de contagion / (sensibilité + taux de faux positifs)

## Conclusion

Nous avons donc vu que la sensibilité (capacité à détecter les personnes effectivement malades) et la spécificité (capacité à ne pas générer de faux positifs) ne suffisent pas à interpréter les résultats d'un test de dépistage. Un paramètre souvent oublié, la part de la population atteinte en moyenne, va grandement influer sur les résultats: plus cette part est faible, plus le nombre de faux positifs va être important.

Ainsi, tester massivement la population en début d'épidémie, quand peu de gens sont contaminés, n'apparaît pas être une stratégie efficiente: le nombre de faux positifs à traiter sera beaucoup trop élevé. En revanche, il semble plus adapté de tester massivement une fois l'épidémie installée car un taux de contamination plus élevé permettra d'avoir des résultats de tests plus fiables.

Une manière de diminuer le nombre de faux positifs est de multiplier le nombre de tests sur une même personne: la probabilité d'être malade augmente alors avec le nombre de résultats positifs. Nous verrons cependant dans un prochain article que le nombre de tests requis reste toutefois assez conséquent en début d'épidémie, et qu'il n'est pas forcément judicieux de démarrer une campagne de dépistage massif trop tôt.
