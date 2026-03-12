# Métriques Vidéo Meta Ads : Le Guide de Référence Complet

## Introduction

## Les Métriques Vidéo Fondamentales

### Hook Rate

### Hold Rate

### Thumbstop Ratio

## Métriques de Visionnage et de Coût

### ThruPlay

### Average Watch Time (Durée de visionnage moyenne)

### Cost per ThruPlay (Coût par ThruPlay)

## Analyse Avancée de la Performance Vidéo

### La Courbe de Rétention d'Audience

### Optimisation du "Hook" : Les 3 Premières Secondes

## Formats Vidéo Performants et Bonnes Pratiques

### Durée Optimale par Placement

### L'Importance Cruciale des Sous-Titres

## Intégration avec les Systèmes Meta : Andromeda, GEM et Lattice

## Apprentissages Terrain

## Références

## Introduction : L'Ère de la Vidéo et la Mesure de l'Impact sur Meta

La publicité vidéo est devenue le pilier central des stratégies de communication sur les plateformes Meta (Facebook, Instagram, Messenger, Audience Network). Dans un écosystème où la capacité d'attention de l'utilisateur est une ressource rare et volatile, la simple diffusion d'un message ne suffit plus. Le succès repose sur une compréhension granulaire et une optimisation méticuleuse de la manière dont le contenu est consommé. Les métriques vidéo ne sont pas de simples indicateurs de performance ; elles sont le langage par lequel l'algorithme de Meta et les annonceurs dialoguent pour maximiser la pertinence, l'engagement et, in fine, le retour sur investissement.

Ce document de référence a pour vocation de fournir une analyse technique approfondie des métriques vidéo essentielles au sein de l'écosystème Meta. Nous dépasserons les définitions de surface pour explorer leur signification stratégique, leurs benchmarks, et la manière dont elles s'intègrent dans les mécanismes complexes des systèmes d'enchères et de diffusion publicitaire de Meta, notamment les projets connus sous les noms de code Andromeda, GEM (Generalized Engagement Model) et Lattice. Comprendre ces indicateurs est une condition sine qua non pour tout annonceur souhaitant transformer ses dépenses publicitaires en résultats commerciaux tangibles et prévisibles. Nous aborderons les métriques qui définissent la capture de l'attention initiale (Hook Rate), le maintien de l'intérêt (Hold Rate), la qualité perçue par l'algorithme (Thumbstop Ratio), jusqu'aux indicateurs de visionnage complet et de coût (ThruPlay, Cost per ThruPlay). Enfin, nous analyserons les outils d'optimisation à notre disposition, de l'analyse de la courbe de rétention aux meilleures pratiques de format, pour construire des créatifs vidéos qui non seulement performent, mais dominent.

## Les Métriques Vidéo Fondamentales : Capturer et Maintenir l'Attention

Le succès d'une publicité vidéo sur Meta se joue en quelques secondes. Les métriques fondamentales sont celles qui mesurent la capacité d'une création à stopper le défilement (le "scroll") et à retenir l'attention de l'audience. Elles constituent le premier filtre de performance et sont des signaux primordiaux pour l'algorithme de diffusion.

### Hook Rate : La Mesure de l'Accroche Initiale

Le **Hook Rate**, ou taux d'accroche, est sans doute la métrique la plus critique pour évaluer l'efficacité des trois premières secondes d'une vidéo. C'est le premier jugement de valeur que l'audience et l'algorithme portent sur votre contenu.

**Définition et Calcul :**
Le Hook Rate mesure le pourcentage d'utilisateurs qui, après avoir été exposés à votre vidéo (une impression), la visionnent pendant au moins trois secondes. La formule est la suivante :

> **Hook Rate = (Vues de 3 secondes / Impressions) * 100**

Une "vue de 3 secondes" est comptabilisée dès que la vidéo a été lue pendant un total de trois secondes, ou pour la quasi-totalité de sa durée si elle est plus courte. Ce seuil de trois secondes a été défini par Meta comme le point où une consommation passive se transforme en un engagement intentionnel, même minime.

**Benchmarks et Interprétation :**
Un Hook Rate élevé indique que le début de votre vidéo est suffisamment percutant pour capter l'attention dans un flux de contenu extrêmement dense. 

| Niveau de Performance | Benchmark de Hook Rate | Interprétation et Actions Recommandées |
| :--- | :--- | :--- |
| **Excellent** | > 30% | Votre accroche est très efficace. Le début de la vidéo est parfaitement optimisé pour votre audience. Capitalisez sur cet élément et analysez-le pour le répliquer. |
| **Bon** | 20% - 30% | L'accroche est solide mais peut être améliorée. Testez de nouvelles variations pour les 3 premières secondes (visuels, titres, questions) pour dépasser les 30%. |
| **Moyen** | 10% - 20% | Votre vidéo peine à retenir l'attention initiale. Une refonte complète du hook est nécessaire. L'audience cible n'est peut-être pas la bonne. |
| **Faible** | < 10% | L'accroche est inefficace. La vidéo est immédiatement ignorée par la majorité des utilisateurs. Il est urgent de retravailler les premières secondes ou de changer radicalement de concept créatif. |

Un Hook Rate faible est un signal d'alarme majeur. Il signifie que la majorité de votre budget est dépensée pour des impressions qui ne se transforment même pas en un début de visionnage. L'algorithme de Meta, via son modèle de prédiction de l'engagement (partie intégrante du système GEM), pénalisera la diffusion des créatifs avec un faible Hook Rate, entraînant une augmentation des coûts (CPM) et une portée réduite.

### Hold Rate : La Mesure du Maintien de l'Intérêt

Si le Hook Rate mesure la capacité à attirer l'attention, le **Hold Rate**, ou taux de rétention, mesure la capacité à la conserver. Il évalue la pertinence du contenu qui suit l'accroche initiale.

**Définition et Calcul :**
Le Hold Rate représente le pourcentage d'utilisateurs qui, après avoir visionné les trois premières secondes, continuent de regarder jusqu'à la quinzième seconde (ou jusqu'à la fin si la vidéo est plus courte). Il se calcule à partir des vues de 3 secondes, et non des impressions.

> **Hold Rate = (Vues de 15 secondes ou ThruPlays / Vues de 3 secondes) * 100**

Cette métrique est un excellent indicateur de la qualité et de la pertinence de votre message après l'accroche. Un bon "hook" suivi d'un mauvais "hold" indique une promesse non tenue.

**Benchmarks et Interprétation :**
Le Hold Rate permet de diagnostiquer si le problème de performance se situe au début de la vidéo ou dans son développement.

| Niveau de Performance | Benchmark de Hold Rate | Interprétation et Actions Recommandées |
| :--- | :--- | :--- |
| **Excellent** | > 15% | Votre contenu maintient l'intérêt de l'audience engagée. Le rythme et le message sont pertinents. La structure de votre vidéo est solide. |
| **Bon** | 10% - 15% | La rétention est correcte, mais il existe une déperdition notable après l'accroche. Analysez la courbe de rétention (voir section dédiée) pour identifier les points de décrochage entre 3s et 15s. |
| **Faible** | < 10% | Le contenu après l'accroche ne répond pas aux attentes. L'audience décroche massivement. Il faut revoir le script, le rythme, ou la clarté du message après les 3 premières secondes. |

**La Relation entre Hook et Hold Rate :**
L'analyse conjointe de ces deux métriques est fondamentale :
- **Hook élevé, Hold élevé :** La combinaison idéale. Votre vidéo est performante du début à la fin.
- **Hook élevé, Hold faible :** Votre accroche est bonne (peut-être même un "clickbait" visuel) mais le contenu déçoit. Le problème se situe dans le corps de la vidéo.
- **Hook faible, Hold élevé :** Situation rare. Ceux qui regardent sont très intéressés, mais l'accroche ne parvient pas à qualifier une audience assez large. Le début de la vidéo est à revoir, mais le message de fond est bon.
- **Hook faible, Hold faible :** La vidéo est inefficace à tous les niveaux. Un changement radical est nécessaire.

### Thumbstop Ratio : Le Signal de Qualité pour l'Algorithme

Le **Thumbstop Ratio** est une métrique plus nuancée et souvent moins visible directement dans les rapports standards, mais elle est d'une importance capitale, en particulier pour les formats verticaux comme les Reels. C'est un signal que Meta utilise pour évaluer la capacité d'un créatif à interrompre le défilement de manière qualitative.

**Définition et Interprétation :**
Contrairement au Hook Rate qui est un calcul simple, le Thumbstop Ratio est un signal composite interprété par les systèmes de Meta. Il ne se limite pas à la durée de visionnage, mais intègre d'autres facteurs comme la rapidité avec laquelle l'utilisateur arrête de faire défiler le flux pour regarder la vidéo. Un arrêt net et un visionnage immédiat ont plus de poids qu'un ralentissement et un visionnage hésitant. Un ratio élevé indique que la vidéo a un fort pouvoir d'attraction visuelle et contextuelle.

Meta priorise les contenus avec un Thumbstop Ratio élevé dans les placements comme les Reels, où l'expérience utilisateur est basée sur un flux rapide de découvertes. Un bon Thumbstop Ratio est un indicateur pour l'algorithme que votre contenu est non seulement engageant, mais qu'il améliore l'expérience sur la plateforme. Le système de diffusion de Meta, Andromeda, utilise ce type de signal pour décider quelles publicités méritent une plus grande vélocité de diffusion initiale. Un bon score peut entraîner un "effet boule de neige", où la publicité est montrée plus rapidement à une audience plus large, bénéficiant ainsi de CPM plus bas et d'un avantage concurrentiel dans les enchères.

## Métriques de Visionnage et de Coût : Mesurer l'Engagement Profond et l'Efficacité Budgétaire

Après avoir capturé et maintenu l'attention initiale, il est crucial de mesurer jusqu'où va l'engagement de l'audience et à quel coût. Ces métriques permettent de juger de la capacité d'une vidéo à transmettre un message complet et d'évaluer l'efficience de l'investissement publicitaire.

### ThruPlay : L'Indicateur Standard de Visionnage Qualitatif

Le **ThruPlay** est devenu l'indicateur de référence de Meta pour un visionnage considéré comme significatif. Il a largement remplacé les anciennes métriques comme les "vues de vidéo à 100%" dans les optimisations par défaut, car il offre un équilibre plus réaliste entre complétion et durée d'attention.

**Définition et Contexte :**
Un ThruPlay est comptabilisé lorsqu'une vidéo est visionnée jusqu'à sa fin ou pendant au moins 15 secondes, selon la première de ces éventualités. 

> **Un ThruPlay = Visionnage de 15 secondes OU Visionnage complet de la vidéo (si durée < 15s)**

Cette métrique a été introduite par Meta pour standardiser la mesure de l'engagement sur des vidéos de durées très variables. Pour une vidéo de 60 secondes, atteindre 15 secondes de visionnage est un signal d'intérêt très fort. Pour une vidéo de 8 secondes, la visionner en entier est l'équivalent logique. Le ThruPlay unifie ces deux scénarios sous une seule bannière, simplifiant l'optimisation et le reporting.

Lorsque vous choisissez l'objectif de campagne "Vues de vidéo", l'algorithme de Meta (via le système d'enchères et de diffusion Andromeda) optimise par défaut la diffusion pour générer le maximum de ThruPlays pour votre budget. Cela signifie qu'il va prioriser les utilisateurs et les placements les plus susceptibles de générer ce type d'engagement qualitatif.

**Interprétation Stratégique :**
Le nombre de ThruPlays est un excellent indicateur de la quantité d'audience que vous avez réussi à engager avec votre message principal. Si votre proposition de valeur ou votre appel à l'action se situe après la marque des 15 secondes, le ThruPlay devient une métrique de succès intermédiaire essentielle avant la conversion finale. Un volume élevé de ThruPlays à un coût maîtrisé indique que votre créatif est efficace pour délivrer son message à une audience réceptive.

### Average Watch Time (Durée de visionnage moyenne) : Le Pouls de Votre Contenu

La **durée de visionnage moyenne** est une métrique simple en apparence mais riche en informations. Elle donne une mesure brute de l'engagement moyen de tous les utilisateurs qui ont commencé à regarder votre vidéo.

**Définition et Calcul :**
Elle est calculée en divisant le temps de visionnage total de votre vidéo par le nombre total de lectures de la vidéo (personnes ayant regardé au moins 3 secondes).

> **Durée de visionnage moyenne = Temps de visionnage total / Lectures de la vidéo**

**Interprétation et Limites :**
Une durée de visionnage moyenne élevée est généralement un bon signe, mais cette métrique doit être interprétée avec prudence. Elle peut être trompeuse car elle est une moyenne. Par exemple, une vidéo de 60 secondes peut avoir une durée de visionnage moyenne de 10 secondes de deux manières très différentes :
1.  La majorité des spectateurs regardent environ 10 secondes.
2.  La moitié des spectateurs regarde 20 secondes, tandis que l'autre moitié décroche après 1 seconde.

C'est pourquoi il est crucial de ne pas analyser cette métrique isolément. Elle prend tout son sens lorsqu'elle est combinée avec l'analyse de la **courbe de rétention d'audience**, qui montre précisément *où* les gens arrêtent de regarder. Cependant, en tant qu'indicateur rapide, la comparaison de la durée de visionnage moyenne entre différentes vidéos (de durée similaire) permet d'identifier rapidement celles qui retiennent le mieux l'attention globale.

### Cost per ThruPlay (Coût par ThruPlay) : La Mesure de l'Efficacité Publicitaire

Le **Coût par ThruPlay (CPT)** est le thermomètre de l'efficacité de votre budget publicitaire vidéo. Il répond à la question simple : "Combien me coûte chaque visionnage significatif de ma vidéo ?"

**Définition et Calcul :**
Le CPT est le coût total de votre campagne ou de votre ensemble de publicités divisé par le nombre total de ThruPlays.

> **Cost per ThruPlay = Montant total dépensé / Nombre de ThruPlays**

**Benchmarks et Optimisation :**
Le CPT varie énormément en fonction du secteur, de l'audience, du placement et de la qualité du créatif. Il n'y a pas de "bon" CPT universel. L'objectif est de le minimiser tout en maximisant la qualité de l'engagement. Un CPT faible est le signe d'une adéquation réussie entre le créatif, l'audience et l'enchère.

| Facteurs d'Influence du CPT | Impact sur le CPT | Recommandations d'Optimisation |
| :--- | :--- | :--- |
| **Qualité du Créatif** | Un créatif avec un Hook et un Hold Rate élevés génère plus de ThruPlays pour le même nombre d'impressions, réduisant mécaniquement le CPT. | Itérer constamment sur les créatifs. Tester de nouvelles accroches, de nouveaux angles, de nouveaux montages. Un bon créatif est le levier le plus puissant. |
| **Pertinence de l'Audience** | Une audience bien ciblée est plus susceptible de s'engager avec le contenu, ce qui augmente le taux de ThruPlay et diminue le CPT. | Affiner le ciblage. Utiliser les audiences personnalisées (Custom Audiences) et similaires (Lookalike Audiences) pour toucher des utilisateurs à forte valeur. |
| **Concurrence et Enchères** | Une forte concurrence sur une audience donnée augmente le coût par mille impressions (CPM), ce qui se répercute directement sur le CPT. | Élargir les audiences pour réduire la pression concurrentielle. Utiliser les stratégies d'enchères automatiques de Meta pour trouver les opportunités les moins coûteuses. |
| **Placement** | Certains placements (ex: Audience Network) ont des CPT nativement plus bas mais peuvent avoir une qualité d'attention inférieure. | Analyser la performance par placement. Un CPT bas n'est pas toujours le but si l'attention et la conversion qui en découlent sont faibles. Concentrer le budget sur les placements les plus rentables. |

L'optimisation du CPT est un processus continu d'équilibrage. Il s'agit de trouver le point idéal où le coût est bas, mais où le ThruPlay représente toujours un engagement authentique qui contribue aux objectifs commerciaux finaux, qu'il s'agisse de notoriété, de considération ou de conversion.

## Analyse Avancée de la Performance Vidéo : Au-delà des Métriques Standards

Les métriques agrégées comme le Hold Rate ou la durée de visionnage moyenne donnent une vue d'ensemble de la performance, mais pour une optimisation précise, il est nécessaire de plonger dans des outils d'analyse plus détaillés. C'est ici que l'analyse de la courbe de rétention et l'optimisation chirurgicale du "hook" entrent en jeu.

### La Courbe de Rétention d'Audience : La Véritable Histoire de Votre Vidéo

La courbe de rétention d'audience est sans doute l'outil de diagnostic le plus puissant à la disposition d'un annonceur vidéo. Elle visualise le pourcentage de votre audience qui continue de regarder la vidéo à chaque seconde. Plutôt qu'un simple chiffre, elle offre une cartographie détaillée de l'engagement, seconde par seconde.

**Comment Accéder et Lire la Courbe :**
Dans le Gestionnaire de Publicités de Meta, au niveau de la publicité individuelle, vous pouvez sélectionner une vidéo et afficher ses détails de performance, y compris le graphique de rétention. Le graphique présente le temps sur l'axe des X et le pourcentage de l'audience restante sur l'axe des Y.

**Interprétation des Modèles de Courbe :**

| Forme de la Courbe | Diagnostic | Actions Recommandées |
| :--- | :--- | :--- |
| **Chute Abrupte (dans les 3 premières secondes)** | Le "hook" est inefficace. La courbe plonge de 100% à moins de 30-40% presque immédiatement. C'est le problème le plus courant et le plus critique. | Refonte complète de l'accroche. Tester des visuels plus forts, un message plus clair, une question intrigante, ou un mouvement plus dynamique dès la première seconde. |
| **Décroissance Régulière et Lente** | La vidéo est cohérente et maintient un niveau d'intérât stable. C'est une courbe saine, mâme si une décroissance est naturelle. | Identifier les légers points d'inflexion pour des micro-optimisations. Le message général est bon, mais peut-âtre que le rythme pourrait âtre accéléré. |
| **Chutes Soudaines (Dips)** | Un élément spécifique à un moment T a provoqué un décrochage massif. Cela peut âtre un changement de scène, une phrase confuse, un visuel déplaisant, ou l'apparition d'un logo. | Analyser précisément le contenu de la vidéo à la seconde exacte du "dip". Couper ou modifier cette scène spécifique. C'est l'opportunité d'optimisation la plus facile à identifier. |
| **Pics ou Remontées de la Courbe** | Indique que des spectateurs ont rejoué une portion spécifique de la vidéo. C'est un signal extrâmement positif. | Analyser ce qui se passe à ce moment précis. Est-ce une information cruciale ? Une démonstration produit impressionnante ? Un élément humoristique ? Capitaliser sur cet élément dans de futurs créatifs. |

L'analyse de la courbe de rétention transforme l'optimisation créative d'un jeu de devinettes en une science précise. Elle permet de fournir des retours exploitables aux équipes créatives ("*Nous perdons 40% de l'audience à la seconde 7, lorsque le plan change*") plutôt que des commentaires vagues ("*la vidéo ne performe pas*").

### Optimisation du "Hook" : Les 3 Premières Secondes Critiques

Nous avons établi l'importance du Hook Rate, mais comment l'optimiser concrètement ? Les trois premières secondes doivent accomplir trois objectifs en un temps record : capter l'attention, qualifier l'audience et donner une raison de continuer à regarder.

**Principes d'un Hook Efficace :**

1.  **Mouvement Immédiat :** L'œil humain est attiré par le mouvement. Une vidéo qui commence par un plan fixe est une occasion manquée. Utilisez des transitions rapides, du texte animé, ou un mouvement de caméra pour créer une dynamique dès la première image.
2.  **Visage Humain :** Les visages, en particulier ceux qui expriment une émotion claire, créent une connexion instantanée. Commencer par un gros plan sur un visage surpris, joyeux ou intrigué est une technique extrâmement efficace.
3.  **Question ou Déclaration Audacieuse :** Engager le spectateur intellectuellement. Une question qui le concerne directement ("*Votre peau est-elle sèche en hiver ?*") ou une affirmation surprenante ("*90% des gens utilisent mal ce produit*") incite à chercher la réponse.
4.  **Identification du Problème :** Montrer le "point de douleur" (le problème que votre produit résout) de manière visuelle et immédiate. Par exemple, une tache sur un vétement pour un détachant, ou une personne frustrée devant son ordinateur pour un logiciel.
5.  **Visuel Intriguant ou Satisfaisant :** Utiliser des visuels qui sortent de l'ordinaire (ASMR visuel, "oddly satisfying content", plans cinématographiques inhabituels) pour créer une curiosité purement esthétique.

**Exemples Concrets :**

| Type de Hook | Bon Exemple (pour un produit de soin de la peau) | Mauvais Exemple |
| :--- | :--- | :--- |
| **Question** | Texte en gros plan : "Ras-le-bol de ces imperfections ?" sur un visage expressif. | Logo de la marque, puis une voix off qui demande "Connaissez-vous notre nouvelle crème ?" |
| **Problème/Solution** | Plan très rapide montrant une peau irritée, suivi immédiatement par un plan montrant l'application apaisante de la crème. | Un plan lent et esthétique du packaging du produit posé sur une étagère. |
| **Visuel Fort** | Un mouvement de caméra rapide qui suit une goutte de sérum tombant sur une pétale de fleur. | Un plan fixe de la bouteille du produit avec un fond uni. |

Le testing itératif est la clé. Produisez systématiquement 3 à 5 variations des 3 premières secondes pour chaque concept vidéo. L'algorithme de Meta, grâce à ses capacités d'optimisation dynamique du créatif (Dynamic Creative Optimization), peut rapidement identifier la version la plus performante et lui allouer la majorité du budget, vous permettant d'optimiser le Hook Rate en temps réel.

## Formats Vidéo Performants et Bonnes Pratiques : S'Adapter aux Usages

Une métrique de performance n'existe pas dans le vide ; elle est intrinsèquement liée au contexte dans lequel la vidéo est consommée. Comprendre les spécificités de chaque placement et les habitudes des utilisateurs est fondamental pour créer des vidéos qui ne sont pas seulement vues, mais qui sont aussi appréciées et efficaces.

### Durée Optimale par Placement : Le Bon Contenu au Bon Endroit

La durée d'une vidéo n'est pas une décision arbitraire. Elle doit à la fois servir le message et correspondre aux attentes de l'utilisateur sur un placement donné. Une vidéo qui performe admirablement dans le fil d'actualité peut àtre un échec total en Stories si elle n'est pas adaptée.

| Placement | Durée Recommandée | Justification et Stratégie |
| :--- | :--- | :--- |
| **Reels Instagram & Facebook** | 15 - 30 secondes | L'usage est basé sur le divertissement rapide et la découverte. L'attention est extrâmement courte. Le message doit àtre délivré de manière concise et percutante. Les 15 premières secondes sont cruciales pour atteindre le ThruPlay. Une durée de 30s permet un storytelling légèrement plus développé si le hook est excellent. |
| **Fil d'actualité (Feed) Facebook & Instagram** | 15 - 60 secondes | L'utilisateur est dans un mode de consommation plus posé. Il est plus disposé à regarder des contenus plus longs s'ils sont pertinents. Une vidéo de 60 secondes peut permettre une démonstration de produit, un témoignage client ou un mini-reportage. Le défi est de maintenir l'intérât au-delà de la marque des 15 secondes. |
| **Stories Instagram & Facebook** | < 15 secondes | Le format est conçu pour des séquences courtes et immersives. Chaque "slide" de Story dure au maximum 15 secondes. Il est impératif de délivrer un message complet dans ce laps de temps. Utiliser plusieurs slides consécutives peut raconter une histoire plus longue, mais chaque slide doit pouvoir àtre comprise indépendamment. |
| **In-Stream Vidéo** | 5 - 15 secondes (non-skippable) ou > 15s (skippable) | L'utilisateur est ici pour regarder un autre contenu. Votre publicité est une interruption. Pour les formats non-skippables, le message doit àtre extrâmement direct. Pour les formats skippables après 5 secondes, ces 5 premières secondes doivent donner une raison irrésistible de ne pas cliquer sur "Ignorer l'annonce". |

Le recyclage d'un mâme fichier vidéo sur tous les placements est une erreur coûteuse. Il est essentiel de produire des déclinaisons spécifiques pour chaque format, en respectant non seulement la durée mais aussi les ratios (9:16 pour Reels/Stories, 4:5 ou 1:1 pour le Feed).

### L'Importance Cruciale des Sous-Titres : Concevoir pour le "Sound-Off"

Une des réalités les plus souvent sous-estimées de la publicité vidéo sur mobile est que la grande majorité des vidéos sont vues sans le son. Les estimations varient, mais le consensus se situe autour de **85% des vidéos vues en mode "sound-off"** dans le fil d'actualité.

**Implications Stratégiques :**
Ignorer cette réalité signifie que votre message, s'il repose uniquement sur une voix-off ou un dialogue, est tout simplement inaudible pour la majorité de votre audience. Votre investissement publicitaire est alors réduit à une séquence d'images muettes.

**Les Bonnes Pratiques du Sous-Titrage :**

1.  **Sous-titres Intégrés (Burn-in) :** Ne comptez pas sur les sous-titres générés automatiquement par Facebook, qui peuvent âtre désactivés par l'utilisateur. Intégrez les sous-titres directement dans le fichier vidéo. Cela garantit qu'ils sont toujours visibles.
2.  **Lisibilité Maximale :** Utilisez une police claire et une taille suffisante. Appliquez un fond contrasté (un bandeau noir ou une ombre portée) pour que le texte soit lisible même sur des arrière-plans complexes.
3.  **Dynamisme et Style :** Les sous-titres ne doivent pas âtre ennuyeux. Utilisez des animations de texte (pop-up, changement de couleur sur le mot prononcé) pour ajouter du dynamisme et guider l'attention du spectateur. Ce style, popularisé par des créateurs comme Alex Hormozi, est devenu une norme de performance.
4.  **Synthèse et Mots-Clés :** Ne vous contentez pas de transcrire mot pour mot. Mettez en évidence les mots-clés avec des couleurs, des tailles ou des styles différents. Le sous-titre doit renforcer le message, pas seulement le transcrire.

Concevoir pour une consommation sans son ("sound-off design") n'est pas une option, c'est une nécessité. Une vidéo doit âtre parfaitement compréhensible sans le son. Le son, lorsqu'il est activé, doit enrichir l'expérience, mais pas en âtre la condition de compréhension.

## Intégration avec les Systèmes Meta : Andromeda, GEM et Lattice

Pour l'annonceur expert, comprendre les métriques en surface n'est pas suffisant. La véritable maîtrise provient de la compréhension de la manière dont ces métriques sont interprétées et utilisées par les systèmes algorithmiques de Meta. Ces systèmes, souvent désignés par des noms de code internes comme Andromeda (le système de diffusion), GEM (Generalized Engagement Model - le modèle d'engagement généralisé) et Lattice (l'infrastructure de données en temps réel), forment un écosystème complexe qui détermine le sort de chaque publicité.

### Andromeda : Le Chef d'Orchestre de la Diffusion Publicitaire

**Andromeda** est le système de diffusion publicitaire de nouvelle génération de Meta. Son rôle est de décider quelle publicité montrer, à quel utilisateur, à quel moment, et sur quel placement, afin de maximiser la valeur pour l'utilisateur et l'annonceur. Les métriques vidéo sont des signaux d'entrée fondamentaux pour Andromeda.

- **Hook Rate et Thumbstop Ratio comme Signaux de Vélocité :** Lorsqu'une nouvelle vidéo est lancée, Andromeda la diffuse à un petit échantillon de l'audience cible. Il mesure en temps réel les premiers signaux d'engagement. Un Hook Rate et un Thumbstop Ratio élevés sont interprétés par Andromeda comme un indicateur de haute qualité et de pertinence. En réponse, le système accorde une "vélocité" de diffusion plus élevée à la publicité, la sortant plus rapidement de la phase d'apprentissage et la montrant à une plus grande partie de l'audience. À l'inverse, un mauvais Hook Rate peut entraîner une limitation précoce de la diffusion, Andromeda jugeant que la création dégrade l'expérience utilisateur.

### GEM (Generalized Engagement Model) : Le Prédicteur de l'Intérât

Le **GEM** est un ensemble de modèles de machine learning dont le but est de prédire la probabilité qu'un utilisateur s'engage avec un contenu donné (une publicité, une publication, etc.). Pour chaque impression potentielle, GEM calcule un score d'engagement prédictif (p-Engagement).

- **Du Hook Rate au p-ThruPlay :** GEM ne se contente pas de prédire un clic ou un "like". Il prédit des engagements beaucoup plus granulaires. Lorsque vous optimisez pour les ThruPlays, GEM utilise les données historiques de votre compte et des créatifs similaires pour prédire la probabilité qu'un utilisateur spécifique génère un ThruPlay sur votre vidéo. Les métriques passées (Hook Rate, Hold Rate) de vos vidéos sont des données d'entraànement cruciales pour ce modèle. Une vidéo avec un historique de Hold Rate élevé aura un score p-ThruPlay plus élevé pour des utilisateurs similaires, ce qui lui donnera un avantage dans l'enchère.

### Lattice : L'Infrastructure de Données en Temps Réel

**Lattice** est l'infrastructure qui permet à des systèmes comme Andromeda et GEM de fonctionner avec des données fraîches et en temps réel. C'est le système nerveux qui collecte, traite et rend disponibles les milliards de signaux générés chaque seconde sur les plateformes Meta.

- **Rétroaction en Temps Réel :** Grâce à Lattice, les résultats d'une diffusion publicitaire sont réinjectés quasi instantanément dans les modèles. Si votre vidéo commence à obtenir un excellent Hook Rate dans les premières minutes de sa diffusion, cette information est immédiatement utilisée par Andromeda pour ajuster la stratégie de diffusion. C'est ce qui permet aux systèmes d'optimisation dynamique du créatif de fonctionner si efficacement, en testant plusieurs variations et en convergeant rapidement vers la plus performante.

En résumé, les métriques vidéo ne sont pas de simples données de reporting. Elles sont le carburant et les signaux de direction pour les moteurs algorithmiques de Meta. Un annonceur qui optimise ses vidéos pour améliorer son Hook Rate et son Hold Rate ne fait pas que créer de meilleures publicités ; il entraîne activement les modèles de Meta à mieux performer pour son compte, créant ainsi un cercle vertueux de performance et d'efficacité.

## Apprentissages Terrain

*Cette section est destinée à àtre complétée avec des observations et des données concrètes issues d'analyses de campagnes futures. Les benchmarks et les tendances du marché y seront consignés pour maintenir ce document à jour.*

## Références

[1] Meta for Business. "Spécifications techniques et recommandations relatives aux publicités vidéo du fil Facebook." Consulté le 12 mars 2026.

[2] Meta for Business. "À propos des vues de vidéo ThruPlay." Consulté le 12 mars 2026.

[3] Meta AI. "Annonce de la nouvelle génération de notre infrastructure de diffusion publicitaire." Blog de recherche de Meta AI. Consulté le 12 mars 2026.
