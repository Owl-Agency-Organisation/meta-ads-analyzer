# Stratégies d'enchères Meta Ads : Le Guide de Référence Technique

## Introduction

La maîtrise des stratégies d'enchères est un pilier fondamental de la performance sur Meta Ads. Choisir la bonne stratégie ne se résume pas à une simple sélection dans une liste déroulante ; il s'agit d'une décision stratégique qui influence directement la rentabilité, la portée et la capacité à atteindre les objectifs marketing fixés. Une stratégie d'enchère inadéquate peut entraîner des coûts par acquisition (CPA) trop élevés, une diffusion limitée, ou encore l'incapacité à scaler les campagnes profitables. À l'inverse, une stratégie bien choisie et correctement gérée permet d'optimiser la livraison des publicités, de contrôler les coûts et de maximiser le retour sur investissement (ROAS).

Ce document de référence technique a pour vocation de fournir une analyse approfondie et actionnable des différentes stratégies d'enchères disponibles sur Meta Ads en 2024-2026. Nous irons au-delà de la simple description des options pour plonger au cœur des mécanismes qui les gouvernent, en nous appuyant sur les concepts internes à Meta, notamment les systèmes **Andromeda**, **GEM** (Generalized Estimation Model) et **Lattice**. Comprendre, même à un niveau conceptuel, comment ces systèmes modélisent et prédisent le comportement des utilisateurs est essentiel pour tout expert souhaitant véritablement maîtriser la plateforme.

Nous aborderons en détail chaque stratégie, du "Lowest Cost" au "Bid Cap", en passant par le "Cost Cap" et le "ROAS Goal". Pour chacune, nous analyserons son fonctionnement, ses avantages, ses inconvénients, et les cas d'usage les plus pertinents. Ce guide inclut également un arbre de décision pour vous aider à sélectionner la stratégie la plus adaptée à votre contexte, une analyse de l'impact de chaque stratégie sur la phase d'apprentissage, ainsi qu'un inventaire des erreurs les plus courantes et des méthodes pour les éviter. L'objectif est de vous armer des connaissances nécessaires pour prendre des décisions éclairées, optimiser vos campagnes avec précision et scaler vos investissements publicitaires de manière durable.

## Les Fondamentaux du Système d'Enchères Meta (Andromeda, GEM, Lattice)

Pour véritablement maîtriser les stratégies d'enchères, il est indispensable de comprendre la mécanique interne qui régit la diffusion des publicités sur Meta. Le système publicitaire de Meta est l'un des plus sophistiqués au monde, reposant sur une infrastructure complexe de modèles de machine learning conçus pour optimiser la valeur pour les utilisateurs et les annonceurs. Au cœur de ce système se trouvent des projets et des modèles dont les noms de code, tels qu'**Andromeda**, **GEM** et **Lattice**, symbolisent les différentes couches de l'intelligence artificielle à l'œuvre.

**Andromeda** peut être vu comme le système global de diffusion publicitaire, l'écosystème qui orchestre l'ensemble du processus, de la sélection de l'audience à la diffusion finale de la publicité. Il intègre d'innombrables signaux en temps réel pour prendre des décisions en quelques millisecondes. L'objectif d'Andromeda est de maximiser la valeur totale, qui est une combinaison de la valeur pour l'annonceur (atteindre son objectif au meilleur coût) et de la valeur pour l'utilisateur (voir des publicités pertinentes et engageantes).

Le **GEM (Generalized Estimation Model)** est un composant crucial de ce système. Il s'agit d'un modèle prédictif dont le rôle est d'estimer la probabilité qu'un utilisateur spécifique effectue une action donnée (un clic, une conversion, une vue de vidéo, etc.) s'il est exposé à une publicité particulière. Le GEM est "généralisé" car il est capable de faire ces prédictions pour une multitude d'objectifs et de types d'annonces. Pour chaque impression publicitaire potentielle, le GEM calcule un score de propension, qui est ensuite utilisé pour déterminer la valeur attendue de cette impression pour l'annonceur. Ce score est un élément central de l'enchère.

**Lattice** est un autre système de modélisation qui travaille de concert avec le GEM. Alors que le GEM se concentre sur la prédiction d'événements spécifiques, Lattice peut être compris comme un système de calibration et de gestion des 
budgets et des enchères à un niveau plus macro. Il s'assure que la diffusion des publicités est lissée dans le temps et que le budget est dépensé de la manière la plus efficace possible sur la durée de la campagne. Lattice aide à répondre à des questions comme : "Étant donné ce budget et cet objectif, à quel point devrions-nous être agressifs dans les enchères à ce moment précis de la journée ?". Il joue un rôle clé dans les stratégies de "pacing", c'est-à-dire la gestion du rythme de dépense du budget.

L'interaction de ces systèmes est fondamentale. Lorsqu'un annonceur choisit une stratégie d'enchère, il ne fait pas que fixer un paramètre ; il donne une instruction à cet ensemble de modèles. Par exemple, en choisissant "Lowest Cost", l'annonceur demande à Andromeda, GEM et Lattice de trouver les opportunités de conversion les moins chères possibles, sans contrainte de coût spécifique. Le système sera alors incité à enchérir de manière agressive pour les utilisateurs les plus susceptibles de convertir à bas coût. À l'inverse, en fixant un "Cost Cap", l'annonceur impose une contrainte au système, qui devra alors ajuster ses enchères pour respecter ce plafond, quitte à perdre certaines opportunités plus chères mais potentiellement intéressantes.

Comprendre cette mécanique permet de démystifier le comportement de la plateforme. Par exemple, lorsqu'une campagne en "Cost Cap" ne dépense pas son budget, ce n'est pas un "bug", mais la conséquence logique d'une contrainte trop forte : le système, guidé par GEM et Lattice, a déterminé qu'il n'y avait pas suffisamment d'opportunités de conversion sous le plafond de coût fixé. Cette vision "sous le capot" est la clé pour diagnostiquer les problèmes de performance et pour choisir la stratégie d'enchère qui correspond non seulement à l'objectif business, mais aussi à la réalité du marché et à la manière dont les algorithmes de Meta l'interprètent.

## Les Stratégies d'Enchères en Détail

Meta Ads propose un éventail de stratégies d'enchères conçues pour répondre à différents objectifs et niveaux de contrôle. Chaque stratégie interagit différemment avec les systèmes de modélisation de Meta (GEM, Lattice) pour atteindre le but fixé par l'annonceur. Analysons chacune d'entre elles en profondeur.

### 1. Lowest Cost (Coût le Plus Bas)

La stratégie **Lowest Cost**, souvent appelée "Highest Volume" dans la nouvelle nomenclature de Meta, est la stratégie par défaut et la plus simple à utiliser. Son objectif est de dépenser l'intégralité du budget alloué en obtenant le plus grand nombre possible de résultats (conversions, clics, etc.).

**Fonctionnement interne :**
Avec cette stratégie, l'annonceur ne fixe aucune contrainte de coût par résultat. Il donne carte blanche à Meta pour enchérir de la manière la plus agressive possible afin de remporter les impressions qui, selon le modèle GEM, ont la plus forte probabilité de mener à une conversion au coût le plus bas possible à un instant T. Le système va donc prioriser les "fruits les plus bas de l'arbre", c'est-à-dire les utilisateurs les moins chers à convertir. Au fur et à mesure que le budget est dépensé et que ces opportunités bon marché s'épuisent, le système va progressivement enchérir sur des segments d'audience plus coûteux pour continuer à dépenser le budget. Cela explique pourquoi le coût par résultat (CPA) a tendance à augmenter naturellement au cours de la journée ou de la durée de la campagne avec cette stratégie.

**Avantages :**
*   **Simplicité :** Aucune connaissance préalable des CPA ou des enchères n'est requise.
*   **Maximisation du volume :** Idéal pour les phases de test, de lancement de produit, ou lorsque l'objectif principal est d'acquérir un maximum de clients ou de données rapidement.
*   **Meilleure stratégie pour le scaling :** C'est la stratégie qui offre le plus de flexibilité à l'algorithme pour trouver des poches de performance et augmenter les volumes. En augmentant le budget, on permet au système d'aller chercher des conversions plus chères mais toujours rentables, ce qui est la définition même du scaling.

**Inconvénients :**
*   **Aucun contrôle sur le CPA :** Le coût par résultat peut fluctuer de manière importante et augmenter significativement, surtout si l'audience est limitée ou la concurrence élevée.
*   **Moins prévisible :** La rentabilité peut varier d'un jour à l'autre, ce qui peut être problématique pour les entreprises avec des marges serrées.

**Cas d'usage :**
*   Lancement de nouvelles campagnes ou de nouveaux produits pour acquérir rapidement des données.
*   Campagnes de génération de leads où le volume est plus important que le coût par lead à court terme.
*   Scaling de campagnes profitables qui ont déjà fait leurs preuves.
*   Entreprises avec des marges confortables qui peuvent absorber des fluctuations de CPA.

### 2. Cost Cap (Plafond de Coût)

La stratégie **Cost Cap**, ou "Cost Per Result Goal", vise à maintenir un coût par résultat moyen autour d'un montant cible défini par l'annonceur, tout en maximisant le volume de conversions.

**Fonctionnement interne :**
En fixant un Cost Cap, l'annonceur impose une contrainte forte au système. Meta va utiliser le modèle GEM pour estimer le CPA probable pour chaque opportunité d'impression. Le système n'enchérira que sur les opportunités dont le CPA estimé est inférieur ou égal au Cost Cap fixé. Contrairement à une idée reçue, le Cost Cap n'est pas un plafond strict pour chaque enchère individuelle. C'est un objectif de CPA moyen. Meta peut donc remporter des enchères avec un CPA supérieur au Cost Cap si le système anticipe de pouvoir compenser avec d'autres conversions à un CPA inférieur, de manière à ce que la moyenne reste proche de l'objectif. Cependant, en pratique, le système est assez conservateur et évitera les enchères trop éloignées du cap.

**Avantages :**
*   **Contrôle du CPA :** Permet de maîtriser la rentabilité et d'assurer que chaque conversion est acquise à un coût soutenable pour l'entreprise.
*   **Prévisibilité :** Offre une meilleure stabilité des coûts par rapport au Lowest Cost.

**Inconvénients :**
*   **Limite la portée (reach) :** En ignorant les opportunités d'enchères au-dessus du cap, la campagne peut ne pas atteindre tout son potentiel d'audience. Si le Cost Cap est trop bas, la diffusion peut être très limitée, voire complètement bloquée.
*   **Moins efficace pour le scaling :** Le plafond de coût empêche le système d'aller chercher des volumes additionnels à un coût légèrement supérieur, ce qui est souvent nécessaire pour scaler.
*   **Nécessite une bonne estimation du CPA :** Fixer un Cost Cap trop bas est l'erreur la plus courante et la plus préjudiciable. Il faut avoir une idée réaliste du CPA atteignable sur la plateforme.

**Cas d'usage :**
*   Entreprises avec des marges strictes qui doivent maintenir un CPA cible pour être rentables.
*   Campagnes "evergreen" (permanentes) où la stabilité et la prévisibilité des coûts sont primordiales.
*   Annonceurs expérimentés qui connaissent bien leur CPA cible et les dynamiques de leur marché.

### 3. Bid Cap (Plafond d'Enchère)

Le **Bid Cap** est la stratégie la plus restrictive et celle qui offre le plus de contrôle manuel à l'annonceur. Elle consiste à fixer le montant maximum que l'on est prêt à payer pour remporter une enchère.

**Fonctionnement interne :**
Avec le Bid Cap, l'annonceur prend le contrôle direct de l'enchère. Meta n'enchérira jamais un montant supérieur au Bid Cap fixé. C'est une approche très différente du Cost Cap. Alors que le Cost Cap se concentre sur le coût final du résultat (le CPA), le Bid Cap se concentre sur le coût de l'impression (le CPM). L'annonceur doit donc être capable de faire le lien entre le montant de son enchère, le taux de conversion attendu et le CPA final. La formule est la suivante : CPA = (CPM / 1000) / Taux de Conversion. Pour utiliser le Bid Cap efficacement, il faut donc avoir une excellente maîtrise de ces trois variables.

**Avantages :**
*   **Contrôle total :** L'annonceur a un contrôle granulaire sur le montant de ses enchères.
*   **Peut débloquer des situations :** Dans de rares cas, si l'on est certain que le système sous-estime la valeur d'une audience, un Bid Cap agressif peut forcer la diffusion.

**Inconvénients :**
*   **Extrêmement complexe :** Nécessite une compréhension approfondie des mécanismes d'enchères et une analyse constante des données.
*   **Très restrictif :** Le risque de fixer un Bid Cap trop bas et de ne pas diffuser du tout est encore plus élevé qu'avec le Cost Cap.
*   **Non recommandé pour la majorité des annonceurs :** Cette stratégie est réservée à une poignée d'experts qui gèrent des budgets très importants et qui ont des modèles de prédiction internes.

**Cas d'usage :**
*   Annonceurs très sophistiqués avec des équipes de data science capables de modéliser le lien entre enchère, CPM et CPA.
*   Situations de concurrence extrême où il faut manuellement sur-enchérir pour s'assurer de la visibilité.

### 4. ROAS Goal / Minimum ROAS (Objectif de ROAS)

La stratégie **ROAS Goal** (ou "Minimum ROAS") est conçue pour les annonceurs e-commerce ou ceux qui peuvent mesurer la valeur monétaire de leurs conversions. L'objectif est de maintenir un retour sur investissement publicitaire (Return On Ad Spend) moyen autour d'un objectif fixé.

**Fonctionnement interne :**
Cette stratégie est une évolution du Cost Cap, mais au lieu de raisonner en coût, elle raisonne en valeur. L'annonceur doit avoir configuré le suivi des conversions avec valeur (par exemple, remonter le montant du panier d'achat). Le système va alors utiliser le modèle GEM non seulement pour prédire la probabilité d'une conversion, mais aussi pour estimer la valeur potentielle de cette conversion. Il n'enchérira que sur les opportunités qui, selon les prédictions, permettront d'atteindre le ROAS cible. Par exemple, si le ROAS Goal est de 3, le système cherchera à obtenir 3€ de revenus pour chaque euro dépensé en publicité.

**Avantages :**
*   **Optimisation directe de la rentabilité :** C'est la seule stratégie qui se concentre explicitement sur le retour sur investissement.
*   **Maximise la valeur :** Le système ne se contente pas de chercher des conversions, il cherche les conversions qui ont le plus de valeur.

**Inconvénients :**
*   **Nécessite un suivi de la valeur :** Le pixel Meta et l'API de Conversion doivent être parfaitement configurés pour remonter des données de revenus fiables.
*   **Risque de ROAS Goal irréaliste :** Comme pour le Cost Cap, fixer un objectif de ROAS trop élevé peut étrangler la diffusion. Il faut être réaliste sur le ROAS atteignable.
*   **Peut réduire le volume de conversions :** Le système peut ignorer des conversions à faible valeur pour se concentrer sur celles à plus forte valeur, ce qui peut réduire le nombre total de clients acquis.

**Cas d'usage :**
*   E-commerce avec un catalogue de produits aux prix variés.
*   Entreprises qui ont une vision claire du ROAS minimum requis pour être profitable.
*   Campagnes de retargeting où l'on cherche à maximiser la valeur des clients existants.

## Arbre de Décision : Choisir la Bonne Stratégie d'Enchère

Le choix de la stratégie d'enchère est crucial et dépend de multiples facteurs : l'objectif de la campagne, la maturité de l'entreprise, la connaissance du marché, et le niveau de contrôle souhaité. Cet arbre de décision est conçu pour guider les annonceurs dans ce choix stratégique.

**Étape 1 : Quel est votre objectif principal ?**

*   **A. Maximiser le volume (conversions, leads, trafic) et/ou acquérir des données rapidement ?**
    *   Passez à l'Étape 2.
*   **B. Contrôler le coût par acquisition (CPA) pour garantir la rentabilité ?**
    *   Passez à l'Étape 3.
*   **C. Maximiser le retour sur investissement (ROAS) ?**
    *   Passez à l'Étape 4.
*   **D. Avoir un contrôle manuel total sur chaque enchère ?**
    *   **Stratégie recommandée : Bid Cap.** (Attention : réservé aux experts absolus).

**Étape 2 : Vous voulez maximiser le volume. Quel est votre niveau de tolérance aux fluctuations de coût ?**

*   **A. Élevé.** Vous êtes en phase de lancement, de test, ou vous avez des marges confortables. Le plus important est d'obtenir un maximum de résultats, même si le CPA varie.
    *   **Stratégie recommandée : Lowest Cost (Highest Volume).** C'est la stratégie idéale pour le scaling et la découverte d'audience.
*   **B. Faible.** Vous voulez du volume, mais vous ne pouvez pas vous permettre des dérapages de CPA trop importants.
    *   **Alternative :** Commencez en **Lowest Cost** avec un budget modéré pour établir un CPA de référence. Une fois que vous avez une idée claire du CPA moyen, vous pouvez basculer vers une stratégie **Cost Cap** légèrement supérieure à ce CPA de référence pour allier volume et contrôle.

**Étape 3 : Vous voulez contrôler votre CPA. Avez-vous une idée précise et réaliste de votre CPA cible ?**

*   **A. Oui.** Vous avez des données historiques solides (d'autres campagnes, d'autres canaux) qui vous permettent de définir un CPA cible réaliste.
    *   **Stratégie recommandée : Cost Cap.** Fixez le cap à un niveau qui vous garantit la rentabilité. Soyez prêt à l'augmenter légèrement si la diffusion est trop faible.
*   **B. Non.** Vous n'êtes pas sûr du CPA que vous pouvez atteindre sur Meta Ads.
    *   **Action préalable :** Lancez une campagne en **Lowest Cost** avec un budget contrôlé pendant 7 à 14 jours. L'objectif est de laisser l'algorithme vous montrer le CPA atteignable sur votre audience. Une fois cette donnée obtenue, vous pourrez créer une nouvelle campagne en **Cost Cap** avec un objectif de CPA pertinent.

**Étape 4 : Vous voulez maximiser votre ROAS. Avez-vous un suivi fiable de la valeur des conversions ?**

*   **A. Oui.** Votre Pixel Meta et/ou votre API de Conversion sont correctement configurés pour remonter la valeur de chaque achat ou conversion.
    *   **Stratégie recommandée : ROAS Goal.** Définissez un objectif de ROAS minimum qui assure votre rentabilité. Comme pour le Cost Cap, si la diffusion est limitée, il faudra peut-être revoir l'objectif à la baisse pour donner plus de latitude à l'algorithme.
*   **B. Non.** Vous ne suivez pas la valeur des conversions.
    *   **Action préalable :** Mettez en place le suivi de la valeur. C'est un prérequis non négociable. En attendant, vous devez vous rabattre sur une stratégie au **Cost Cap** (Étape 3), en calculant un CPA cible moyen qui devrait vous amener à la rentabilité globale.

**Tableau Récapitulatif**

| Stratégie | Idéal Pour | Niveau de Contrôle | Complexité | Risque Principal |
| :--- | :--- | :--- | :--- | :--- |
| **Lowest Cost** | Volume, Scaling, Test | Faible | Faible | CPA fluctuant et potentiellement élevé |
| **Cost Cap** | Contrôle du CPA, Stabilité | Moyen | Moyen | Plafond trop bas bloquant la diffusion |
| **Bid Cap** | Contrôle manuel total | Élevé | Élevé | Plafond trop bas, complexité extrême |
| **ROAS Goal** | E-commerce, Rentabilité | Moyen | Moyen | Objectif irréaliste, nécessité suivi de valeur |

## Impact sur la Phase d'Apprentissage (Learning Phase)

La phase d'apprentissage est une période critique durant laquelle le système de diffusion de Meta explore et apprend à qui montrer vos publicités pour obtenir les meilleurs résultats. L'algorithme a besoin de collecter un volume de données suffisant (généralement autour de 50 conversions par ad set sur une période de 7 jours) pour sortir de cette phase et atteindre un régime de diffusion stable et optimisé. La stratégie d'enchère choisie a un impact direct sur la capacité d'une campagne à sortir de la phase d'apprentissage.

**Lowest Cost :** C'est la stratégie qui facilite le plus la sortie de la phase d'apprentissage. En n'ayant aucune contrainte de coût, l'algorithme peut enchérir de manière agressive pour obtenir les 50 conversions le plus rapidement possible. C'est pourquoi il est souvent recommandé de commencer avec cette stratégie, surtout si l'on n'est pas sûr du CPA atteignable.

**Cost Cap et ROAS Goal :** Ces stratégies peuvent rendre la sortie de la phase d'apprentissage plus difficile. Si le plafond de coût ou l'objectif de ROAS est trop restrictif, l'algorithme aura du mal à trouver suffisamment de conversions sous la contrainte fixée. La campagne risque alors de rester "en apprentissage limité" (Learning Limited), ce qui signifie qu'elle ne dépense pas son budget et que ses performances sont sous-optimales. Pour éviter cela, il est crucial de fixer un objectif réaliste, voire légèrement supérieur au CPA/ROAS cible au début, pour donner de l'air à l'algorithme. Une fois la phase d'apprentissage terminée, on peut progressivement resserrer la contrainte.

**Bid Cap :** C'est la stratégie la plus susceptible de rester en apprentissage limité. Le contrôle manuel de l'enchère est si restrictif que si le montant n'est pas parfaitement calibré, le système ne remportera quasiment aucune enchère, et n'obtiendra donc jamais les données nécessaires pour apprendre.

**Quand changer de stratégie ?**
Changer de stratégie d'enchère est une modification significative qui réinitialise la phase d'apprentissage. Il faut donc éviter de le faire à la légère. Le meilleur moment pour changer de stratégie est lorsque l'objectif de la campagne évolue. Par exemple :

1.  **De Lowest Cost à Cost Cap :** Après une phase de test réussie en Lowest Cost, vous avez identifié un CPA moyen stable et rentable. Vous pouvez alors lancer une nouvelle campagne (il est souvent préférable de dupliquer ou de créer une nouvelle campagne plutôt que de modifier l'existante) avec une stratégie Cost Cap pour sécuriser cette rentabilité à long terme.
2.  **De Cost Cap à Lowest Cost :** Votre campagne en Cost Cap est stable et profitable, et vous souhaitez maintenant scaler agressivement. Vous pouvez lancer une nouvelle campagne en Lowest Cost avec un budget beaucoup plus important pour permettre à l'algorithme de chercher des volumes supplémentaires, même à un CPA légèrement plus élevé.

## Erreurs Courantes et Comment les Éviter

*   **Erreur 1 : Cost Cap / ROAS Goal trop bas.** C'est l'erreur la plus fréquente. Un annonceur fixe un objectif de CPA à 10€ alors que le marché est à 25€. Résultat : la campagne ne dépense pas, ne diffuse pas et ne génère aucun résultat. **Solution :** Toujours commencer par une phase de découverte en Lowest Cost pour établir un CPA de référence avant de fixer un cap.

*   **Erreur 2 : Changer de stratégie ou de budget trop souvent.** Chaque modification majeure réinitialise la phase d'apprentissage. Il faut laisser le temps à l'algorithme d'apprendre (au moins 7 jours et 50 conversions). **Solution :** Être patient. Ne pas sur-optimiser. Laisser les campagnes tourner et analyser les performances sur des périodes de temps suffisantes.

*   **Erreur 3 : Utiliser le Bid Cap sans expertise.** Beaucoup d'annonceurs pensent être plus malins que l'algorithme. C'est rarement le cas. **Solution :** Pour 99% des annonceurs, il faut faire confiance aux stratégies automatisées (Lowest Cost, Cost Cap, ROAS Goal) et se concentrer sur les autres leviers : la créa, l'offre, l'audience.

*   **Erreur 4 : Ne pas aligner la stratégie avec l'objectif de scaling.** Un annonceur se plaint de ne pas pouvoir augmenter son budget en Cost Cap sans que les performances ne s'effondrent. C'est normal : le Cost Cap est une stratégie de contrôle, pas de scaling. **Solution :** Pour scaler, il faut utiliser la stratégie qui donne le plus de flexibilité à l'algorithme, c'est-à-dire le **Lowest Cost**. Le scaling implique quasi-systématiquement une augmentation du CPA. L'enjeu est de s'assurer que cette augmentation reste dans des limites rentables.

## Lien avec le Scaling

Le scaling, c'est-à-dire l'augmentation significative des budgets publicitaires tout en maintenant une rentabilité acceptable, est l'objectif ultime de nombreux annonceurs. La stratégie d'enchère est au cœur de la capacité à scaler.

Comme mentionné précédemment, le **Lowest Cost est, de loin, la meilleure stratégie pour le scaling.** Pourquoi ? Parce qu'elle ne bride pas l'algorithme. En augmentant le budget, vous donnez à Meta la permission d'aller chercher des poches d'audience de plus en plus larges. Mécaniquement, atteindre ces nouvelles audiences coûte plus cher, et le CPA va donc augmenter. C'est inévitable. Le scaling n'est pas une science exacte où l'on double le budget et l'on double les ventes au même CPA. C'est un compromis : on accepte un CPA plus élevé pour obtenir un volume de ventes et un profit total plus importants.

Les stratégies **Cost Cap** et **ROAS Goal** sont, par nature, des freins au scaling. Leur but est de maintenir un coût ou un ROAS constant. Si vous doublez le budget sur une campagne en Cost Cap, le système ne va pas chercher plus de conversions plus chères. Il va simplement essayer de trouver deux fois plus de conversions *sous* le même plafond de coût. Si ces opportunités n'existent pas en quantité suffisante, le budget ne sera pas dépensé.

Le processus de scaling efficace ressemble donc souvent à ceci :
1.  **Phase 1 (Test) :** Campagnes en **Lowest Cost** avec des budgets modérés pour tester des créas, des audiences, et établir un CPA de référence.
2.  **Phase 2 (Stabilité) :** Une fois les éléments gagnants identifiés, création de campagnes "BAU" (Business As Usual) en **Cost Cap** ou **ROAS Goal** pour sécuriser un socle de rentabilité stable et prévisible.
3.  **Phase 3 (Scaling) :** Création de campagnes dédiées au scaling en **Lowest Cost**, avec des budgets importants, en acceptant une dégradation contrôlée du CPA. Ces campagnes sont alimentées par les meilleures créas et les meilleures audiences identifiées dans les phases précédentes.

## Apprentissages Terrain

*Cette section est destinée à être complétée au fur et à mesure des analyses de comptes publicitaires réels. Elle regroupera des observations, des études de cas et des nuances qui ne se trouvent pas dans la documentation officielle.*

## Références

[1] [Meta Business Help Center: About bid strategies](https://www.facebook.com/business/help/1619591734742116)
[2] [Héroï: Stratégie d’enchère Facebook Ads : tout ce que vous devez savoir](https://www.heroi.fr/blog/facebook/strategie-enchere-facebook-ads/)
