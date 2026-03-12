# Audit Technique Complet d'un Compte Meta Ads

Un audit technique approfondi d'un compte publicitaire Meta (anciennement Facebook) est une étape fondamentale pour garantir l'efficacité des campagnes, maximiser le retour sur investissement (ROAS) et assurer une croissance durable. Ce processus de vérification systématique permet de déceler les erreurs de configuration, les opportunités d'optimisation et les risques potentiels qui pourraient entraver la performance. Dans un écosystème publicitaire en constante évolution, marqué par des mises à jour d'algorithmes (comme Andromeda), des systèmes d'enchères sophistiqués (GEM) et des modèles d'attribution complexes (Lattice), un audit rigoureux est plus qu'une simple maintenance ; c'est une nécessité stratégique. Ce document de référence fournit une méthodologie complète et une checklist détaillée pour mener un audit technique de compte Meta Ads, en se basant sur les meilleures pratiques de 2024-2026.


## 1. Statut du Compte : Le Fondement de la Performance

L'état de santé général du compte publicitaire est le point de départ de tout audit. Un compte restreint ou soumis à des limitations verra ses performances et sa capacité à diffuser des publicités sévèrement impactées. Il est donc impératif de vérifier ces éléments en priorité.

### Restrictions et Sanctions

Les algorithmes de Meta sont de plus en plus stricts quant au respect des règles publicitaires. Les infractions, même involontaires, peuvent entraîner des sanctions allant de la simple désapprobation de publicités à la désactivation complète du compte. Il est crucial de vérifier l'absence de sanctions dans la section "Qualité du compte" du Business Manager.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Statut du Compte Publicitaire** | Actif, sans aucune restriction. | Si le compte est désactivé, suivre immédiatement la procédure d'appel fournie par Meta. Préparer des justificatifs et un argumentaire solide. |
| **Statut du Business Manager** | Vérifié et en règle. | Si le Business Manager est restreint, cela affecte tous les actifs associés. Identifier la cause (souvent liée à la sécurité ou à des infractions répétées) et contacter le support Meta. |
| **Historique des Publicités Refusées** | Un faible volume de refus est acceptable, mais des refus systématiques sur des thématiques similaires sont un signal d'alarme. | Analyser les motifs de refus. Former les équipes sur les règles publicitaires spécifiques au secteur d'activité. Adapter les créatives et le copywriting pour se conformer aux règles. |

### Limites de Dépenses

Chaque nouveau compte publicitaire est soumis à des limites de dépenses initiales, qui sont progressivement augmentées en fonction de l'historique de facturation et de la fiabilité du compte. Il est important de connaître ces limites pour ne pas bloquer la scalabilité des campagnes.

- **Limite de dépense quotidienne :** Vérifier si une limite manuelle a été fixée au niveau du compte. Bien qu'utile pour le contrôle budgétaire, elle peut brider les performances si elle est trop basse.
- **Limite de facturation :** Comprendre le seuil de facturation du compte. Des paiements fréquents et réussis accélèrent l'augmentation de ce seuil.

Un compte sain est un compte qui a la confiance de Meta. Cette confiance se construit par une utilisation conforme des outils, une facturation transparente et le respect des utilisateurs.


## 2. Vérification du Domaine : Sécurité et Autorité

La vérification du domaine est une étape obligatoire pour tout annonceur souhaitant utiliser des fonctionnalités essentielles comme la mesure des événements de conversion agrégés (AEM) et l'édition des aperçus de liens organiques. Elle prouve à Meta que vous êtes le propriétaire légitime du domaine vers lequel vous dirigez les utilisateurs.

### Importance de la Vérification

Au-delà de l'accès aux fonctionnalités, la vérification de domaine est un signal de confiance pour Meta. Elle contribue à lutter contre la désinformation et les acteurs malveillants. Un domaine non vérifié est un frein majeur à la performance et à la mesure précise des conversions, en particulier depuis les mises à jour liées à la confidentialité (iOS 14+).

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Statut de Vérification du Domaine** | Le domaine principal de l'annonceur est listé et son statut est "Vérifié" dans les paramètres du Business Manager. | Si le domaine n'est pas vérifié, suivre l'une des trois méthodes proposées par Meta : ajout d'un enregistrement DNS TXT, import d'un fichier HTML à la racine du site, ou ajout d'une balise meta à la section `<head>` de la page d'accueil. La méthode DNS est la plus robuste. |
| **Attribution des Actifs** | Le domaine vérifié est associé au compte publicitaire et à la Page Facebook correspondante. | Dans les paramètres du domaine au sein du Business Manager, s'assurer que les partenaires et les actifs (Pages) pertinents sont bien connectés au domaine. |
| **Propriété du Domaine** | Le Business Manager qui a vérifié le domaine est bien celui de l'entreprise ou de son agence principale. | En cas de multiples Business Managers (agences, freelances), il est crucial que la propriété du domaine soit centralisée pour éviter les conflits d'attribution des événements de conversion. |


## 3. Configuration du Pixel et de l'API Conversions (CAPI) : Le Cœur du Suivi

Le duo Pixel Meta et API Conversions est le système nerveux central de la mesure de performance sur Meta. Une configuration imprécise ou incomplète conduit inévitablement à une optimisation sous-optimale des campagnes, à des audiences mal construites et à une attribution erronée du retour sur investissement. L'audit de cette configuration est sans doute l'étape la plus technique mais aussi la plus cruciale.

### La Synergie Pixel + CAPI

Le **Pixel Meta** est un code JavaScript qui s'exécute sur le navigateur de l'utilisateur. Il collecte les actions (événements) directement depuis le site web. Cependant, il est de plus en plus sujet aux blocages (ad-blockers, navigateurs axés sur la confidentialité, mises à jour comme ITP d'Apple).

L'**API Conversions (CAPI)**, quant à elle, permet d'envoyer les événements depuis le serveur du site web directement vers les serveurs de Meta. Cette méthode est plus fiable, plus sécurisée et n'est pas affectée par les limitations côté client (navigateur). 

L'utilisation conjointe des deux, avec une **déduplication** correcte, est la norme d'excellence. Le Pixel offre un signal rapide, tandis que CAPI assure la robustesse et la complétude des données. Le système de Meta est conçu pour traiter ces deux flux de données, les dédupliquer grâce à un identifiant d'événement unique, et ne conserver que le premier événement reçu (généralement celui du Pixel) pour l'attribution en temps réel, tout en utilisant les données serveur pour combler les lacunes.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Installation du Pixel** | Le Pixel est présent sur toutes les pages du site. L'extension "Meta Pixel Helper" ne remonte aucune erreur majeure. | Utiliser l'outil de test des événements dans le Gestionnaire d'Événements pour parcourir le site et vérifier que les événements standards (PageView, ViewContent, AddToCart, etc.) se déclenchent correctement. En cas d'absence, vérifier l'intégration (via GTM, une extension CMS ou en dur dans le code). |
| **Mise en Place de CAPI** | Le Gestionnaire d'Événements montre des événements provenant à la fois du "Navigateur" et du "Serveur". | Si seuls les événements du navigateur sont visibles, CAPI n'est pas (ou mal) configuré. Mettre en place CAPI via une intégration partenaire (ex: Shopify, Zapier, Google Tag Manager Server-Side) ou une implémentation personnalisée. |
| **Qualité de la Correspondance des Événements (Event Match Quality)** | Le score de qualité de la correspondance est "Bon" ou "Excellent" (idéalement supérieur à 8/10) pour les événements les plus importants (Purchase, AddToCart, Lead). | Améliorer la quantité et la qualité des informations client envoyées avec les événements CAPI. Inclure systématiquement l'adresse e-mail, le numéro de téléphone, le nom, le prénom, et si possible l'identifiant de session (`fbp`) et l'identifiant de clic (`fbc`). Hacher les données avant de les envoyer. |
| **Déduplication des Événements** | Le pourcentage d'événements dédupliqués est élevé. Le Gestionnaire d'Événements ne montre pas d'avertissement concernant des problèmes de déduplication. | S'assurer que le même `event_id` est envoyé pour un même événement via le Pixel et via CAPI. L'identifiant doit être unique pour chaque action d'un utilisateur. Vérifier que le paramètre `event_name` est identique entre le Pixel et CAPI. |
| **Latence des Événements CAPI** | Les événements serveur sont reçus par Meta dans un délai de quelques minutes à une heure maximum après leur occurrence réelle. | Des délais trop longs peuvent affecter l'optimisation en temps réel. Vérifier la configuration du serveur et la fréquence d'envoi des lots d'événements. Meta tolère un délai allant jusqu'à 7 jours, mais pour l'optimisation, la fraîcheur est clé. |


## 4. Événements de Conversion Prioritaires (AEM)

La Mesure des Événements Agrégés (Aggregated Event Measurement ou AEM) est le protocole de Meta pour mesurer les actions des utilisateurs d'iOS 14.5 et plus, tout en respectant leur choix en matière de suivi via l'App Tracking Transparency (ATT). Ce système impose une limitation majeure : seuls 8 événements de conversion peuvent être configurés et priorisés par domaine pour l'optimisation des campagnes.

### Hiérarchisation Stratégique des Événements

Lorsqu'un utilisateur refuse le suivi, Meta ne peut recevoir qu'un seul événement de conversion pour sa session. La hiérarchisation de ces 8 événements est donc capitale. Si un utilisateur déclenche plusieurs événements, seul l'événement le plus haut dans la hiérarchie sera rapporté. L'ordre de ces événements doit donc refléter la valeur commerciale de chaque action, de la plus haute (l'achat) à la plus basse (la vue de contenu).

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Configuration des 8 Événements** | Les 8 slots d'événements sont configurés dans le Gestionnaire d'Événements, sous l'onglet "Mesure des événements agrégés". | Si la configuration n'est pas faite, les campagnes ciblant les utilisateurs iOS ne pourront pas être optimisées pour la conversion. Sélectionner le domaine vérifié et configurer les 8 événements. |
| **Ordre de Priorité** | Les événements sont ordonnés logiquement par valeur décroissante. Exemple type pour un e-commerce : 1. Purchase, 2. InitiateCheckout, 3. AddToCart, 4. ViewContent. | Un ordre incorrect (ex: ViewContent avant Purchase) entraînera une perte massive de données de conversion. Réorganiser les événements par glisser-déposer. Attention : toute modification de la configuration AEM entraîne une pause de 72 heures avant que les changements ne soient effectifs et que les campagnes puissent recommencer à diffuser correctement. |
| **Utilisation des Valeurs de Conversion (Value Sets)** | Pour l'événement "Purchase", l'optimisation de la valeur est activée, avec une configuration de 4 à 8 fourchettes de valeur. | Ne pas configurer l'optimisation de la valeur pour l'événement d'achat est une opportunité manquée. Cela permet à l'algorithme (GEM) de distinguer les gros paniers des petits et d'optimiser pour un ROAS plus élevé. Configurer les "Value Sets" dans les paramètres AEM. |
| **Conflits de Domaines** | Aucun avertissement de conflit de configuration d'événements entre différents domaines ou Business Managers. | Des conflits peuvent survenir si plusieurs entités tentent de gérer les événements pour un même domaine. Centraliser la gestion du domaine et des événements dans un seul Business Manager propriétaire. |


## 5. Audiences Personnalisées : Le Carburant du Retargeting et des Lookalikes

Les audiences personnalisées sont des segments d'utilisateurs que vous créez à partir de vos propres sources de données. Elles sont le pilier des stratégies de retargeting (reciblage) et la matière première pour créer des audiences similaires (Lookalikes) de haute qualité. La santé, la pertinence et la fraîcheur de ces audiences influencent directement la capacité de l'algorithme à trouver les bonnes personnes au bon moment.

### De la Donnée Brute à l'Audience Actionnable

Une audience personnalisée n'est efficace que si les données qui l'alimentent sont fiables et à jour. Des audiences basées sur des événements Pixel/CAPI mal configurés, des listes de clients obsolètes ou des segments mal définis conduiront à des performances médiocres. L'audit doit s'assurer que chaque audience est non seulement techniquement fonctionnelle mais aussi stratégiquement pertinente.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **État des Audiences Clés** | Toutes les audiences stratégiques (ex: visiteurs du site 30j, ajouts au panier 14j, clients 180j) ont le statut "Prête" ("Ready"). | Si une audience est "En cours de remplissage" ("Populating") depuis trop longtemps, vérifier la source de données. Si elle est "Trop petite" ("Too Small"), la source ne génère pas assez d'utilisateurs (minimum ~1000 pour être efficace). Si elle est en "Erreur", investiguer la cause (souvent liée à la source de données ou à un problème de hachage de la liste de clients). |
| **Taille des Audiences** | Les audiences de retargeting sont suffisamment larges pour permettre une diffusion sans saturation rapide. Les audiences sources pour les Lookalikes contiennent au moins 1000 personnes, idéalement plusieurs milliers, pour garantir la qualité. | Si une audience est trop petite, élargir la fenêtre de rétention (ex: passer de 30j à 60j) ou regrouper plusieurs événements similaires. Pour les Lookalikes, utiliser des sources plus qualifiées (ex: clients récurrents vs. tous les visiteurs). |
| **Fraîcheur des Audiences** | Les audiences basées sur le Pixel/CAPI sont dynamiques et se mettent à jour en temps réel. Les listes de clients sont actualisées régulièrement (au moins une fois par trimestre). | Des listes de clients statiques et anciennes perdent rapidement de leur pertinence. Mettre en place un processus d'actualisation automatique via des outils comme Zapier ou des intégrations CRM, ou manuellement de façon récurrente. |
| **Structure et Nomenclature** | Les audiences sont nommées de manière claire et standardisée (ex: `[WEB] - All Visitors - 30D`, `[CUST] - Purchasers - 180D`). La structure des audiences couvre l'ensemble du funnel de conversion. | Une nomenclature chaotique rend la gestion de compte difficile et risquée. Renommer toutes les audiences selon une convention stricte. Créer les audiences manquantes pour chaque étape clé du parcours client. |
| **Utilisation des Audiences** | Les audiences sont bien utilisées dans les campagnes (inclusions et exclusions). Les exclusions sont logiques (ex: exclure les acheteurs récents des campagnes d'acquisition). | Vérifier dans la section "Audiences" que les segments créés sont bien assignés à des ad sets. Utiliser la fonction "Chevauchement d'audience" pour identifier les redondances excessives entre les segments et affiner le ciblage. |


## 6. Paramètres du Compte : Les Réglages Fondamentaux

Les paramètres de base du compte publicitaire sont souvent configurés lors de sa création et rarement consultés par la suite. Pourtant, une erreur à ce niveau peut avoir des conséquences importantes sur la facturation, l'analyse des données et la gestion quotidienne. Un audit doit impérativement inclure une vérification de ces réglages fondamentaux.

### Cohérence et Stabilité

La cohérence de ces paramètres est essentielle. Un changement de fuseau horaire ou de devise en cours de route, par exemple, peut corrompre l'historique des données et rendre les analyses de performance temporelles caduques. Il est crucial de s'assurer que ces réglages sont corrects dès le départ et restent stables.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Fuseau Horaire** | Le fuseau horaire du compte publicitaire correspond au fuseau horaire principal de l'entreprise ou de son marché cible. | Un mauvais fuseau horaire décale tous les rapports de performance. L'analyse des performances par heure de la journée devient erronée. **Attention : le fuseau horaire ne peut pas être modifié après la création du compte.** Si l'erreur est critique, la seule solution est de créer un nouveau compte publicitaire et de migrer les campagnes. |
| **Devise** | La devise du compte correspond à la devise dans laquelle l'entreprise opère et analyse sa comptabilité. | Comme pour le fuseau horaire, **la devise ne peut pas être modifiée.** Une devise incorrecte oblige à des conversions manuelles constantes pour toute analyse financière, augmentant le risque d'erreur. La seule solution est la création d'un nouveau compte. |
| **Limite de Dépenses du Compte** | Aucune limite de dépense n'est fixée au niveau du compte, sauf si cela correspond à une politique budgétaire interne stricte et consciente de ses implications. | Une limite de dépense globale oubliée est une cause fréquente de blocage soudain des campagnes. Si une limite est active, s'assurer qu'elle est suffisamment élevée pour ne pas brider la performance et la scalabilité. La désactiver si elle n'est pas stratégique. |
| **Méthode de Paiement** | Une méthode de paiement principale valide et une méthode de secours sont enregistrées. | Un échec de paiement entraîne l'arrêt immédiat de toutes les campagnes. Avoir une carte de crédit de secours ou un compte PayPal secondaire évite cette interruption. Vérifier les dates d'expiration des cartes enregistrées. |
| **Informations de l'Entreprise** | Le nom, l'adresse et le numéro de TVA de l'entreprise sont correctement renseignés pour la facturation. | Des informations incorrectes peuvent entraîner des problèmes comptables et fiscaux. Mettre à jour toutes les informations dans les paramètres de facturation du compte. |


## 7. Intégration Shopify/Meta : Le Lien E-commerce

Pour les annonceurs utilisant Shopify, l'application "Facebook & Instagram" est le pont principal entre leur boutique et l'écosystème publicitaire de Meta. Une intégration correcte et à jour est vitale pour assurer la synchronisation du catalogue produits, un suivi des conversions fiable (via l'intégration CAPI de Shopify) et l'accès à des formats publicitaires dynamiques.

### Synchronisation et Fiabilité

L'application centralise de nombreuses fonctionnalités critiques. Un dysfonctionnement peut désynchroniser les prix, les stocks, ou pire, arrêter la remontée des événements de conversion. L'audit de cette connexion doit être particulièrement méticuleux.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Connexion de l'Application** | L'application "Facebook & Instagram" dans Shopify est connectée et tous les actifs (Page Facebook, Compte publicitaire, Pixel, Commerce Account) sont correctement sélectionnés et validés. | Si la connexion est rompue ou si des actifs sont incorrects, cela peut interrompre toutes les synchronisations. Reconnecter l'application en suivant attentivement chaque étape. S'assurer d'utiliser le bon Business Manager et les bons identifiants. |
| **Partage de Données (CAPI Shopify)** | Dans les paramètres de partage de données de l'application, le niveau "Maximum" est sélectionné. Le Pixel Meta et l'API Conversions sont actifs. | Les niveaux "Standard" ou "Amélioré" n'envoient pas toutes les données client nécessaires pour une haute qualité de correspondance (Event Match Quality). Sélectionner "Maximum" pour envoyer toutes les informations possibles (email, téléphone, etc.) via CAPI, ce qui est crucial post-iOS 14. |
| **Statut du Catalogue Produits** | Le catalogue dans le Commerce Manager de Meta est synchronisé avec Shopify. Il n'y a pas d'erreurs de produits (ex: images manquantes, prix à zéro). | Un catalogue non synchronisé ou plein d'erreurs empêche l'utilisation des publicités dynamiques (DPA/DABA) et des fiches produits. Forcer une resynchronisation depuis l'application Shopify. Utiliser l'outil de diagnostic du Commerce Manager pour identifier et corriger les erreurs produit par produit. |
| **Domaine Suivi** | Le domaine utilisé pour le suivi dans l'application Shopify est bien le domaine principal de la boutique, et c'est ce même domaine qui est vérifié dans le Business Manager. | Un conflit de domaine peut entraîner une mauvaise attribution des événements. S'assurer de la cohérence entre le domaine configuré dans Shopify et celui utilisé pour la configuration AEM dans Meta. |


## 8. Structure des Campagnes : L'Architecture de la Performance

La manière dont les campagnes, les ensembles de publicités (ad sets) et les publicités sont organisés a un impact direct sur la capacité de l'algorithme de Meta (le système GEM - Generalized Entity Model) à apprendre et à optimiser efficacement. Une structure de compte désorganisée, fragmentée ou trop complexe gaspille le budget, ralentit la phase d'apprentissage et rend l'analyse des résultats inutilement compliquée.

### Simplicité, Clarté et Consolidation

La tendance depuis plusieurs années, renforcée par la puissance des algorithmes, est à la simplification et à la consolidation. Moins de campagnes, moins d'ad sets, et plus de budget par ad set permettent à l'algorithme de disposer de plus de données pour prendre des décisions d'optimisation. L'ère de la micro-segmentation et des dizaines d'ad sets à 5€ par jour est révolue.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Nomenclature** | Une convention de nommage claire et cohérente est utilisée pour les campagnes, les ad sets et les publicités (ex: `[Date]_[Type]_[Objectif]_[Audience]`). | Une mauvaise nomenclature rend le compte illisible et l'analyse impossible. Mettre en place une charte de nommage et renommer toutes les entités actives. |
| **Objectifs de Campagne** | Les objectifs de campagne (Ventes, Prospects, Trafic, etc.) sont alignés avec les objectifs commerciaux réels. | Utiliser un objectif de "Trafic" pour générer des ventes est une erreur courante. L'algorithme optimisera pour des clics peu coûteux, pas pour des acheteurs. Choisir systématiquement l'objectif qui correspond à l'action finale souhaitée. |
| **Consolidation des Ad Sets** | Le nombre d'ad sets par campagne est limité. Les audiences similaires mais proches (ex: Lookalike 1% et 2% des acheteurs) sont regroupées dans un seul ad set. | La fragmentation du budget sur trop d'ad sets empêche chacun d'entre eux de sortir de la phase d'apprentissage (environ 50 conversions par semaine). Consolider les ad sets avec des ciblages proches pour donner plus de latitude à l'algorithme. |
| **Utilisation de l'Advantage Campaign Budget (CBO)** | Le budget est majoritairement géré au niveau de la campagne (CBO) plutôt qu'au niveau de l'ad set (ABO), surtout pour les campagnes de scaling. | Le CBO permet à Meta de répartir dynamiquement le budget vers les ad sets et les publicités les plus performants en temps réel. C'est un outil puissant pour maximiser le ROAS. Passer les campagnes existantes en CBO (cela peut réinitialiser la phase d'apprentissage). |
| **Phase d'Apprentissage** | La majorité des ad sets actifs et dépensant une part significative du budget ont le statut "Actif" et ne sont pas bloqués en "Apprentissage limité". | Un ad set en "Apprentissage limité" n'a pas assez de conversions pour que l'algorithme puisse s'optimiser. Augmenter le budget, simplifier l'événement de conversion (passer de "Achat" à "Ajout au panier"), ou élargir l'audience sont des solutions possibles. |


## 9. Qualité des Créatives : Le Moteur de l'Engagement

Dans un flux d'actualités saturé, la qualité et la pertinence des créatives (images, vidéos, carrousels) sont les facteurs les plus déterminants pour capter l'attention et susciter l'intérêt. Un audit technique doit également évaluer la manière dont les créatives sont gérées et testées, car cela a un impact direct sur les coûts (CPM) et les taux d'interaction (CTR, taux de conversion).

### Test, Itération et Diversification

Une stratégie créative efficace n'est pas statique. Elle repose sur un processus continu de test de nouvelles approches, d'itération sur les concepts gagnants et de diversification des formats pour s'adapter aux différents placements (Reels, Stories, Feed, etc.). L'utilisation de publicités dynamiques (Dynamic Creative) est une méthode puissante pour automatiser une partie de ce processus.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Utilisation de la Publicité Dynamique (Dynamic Creative)** | L'option "Publicité dynamique" est activée au niveau de l'ad set pour tester systématiquement différentes combinaisons de titres, textes, images/vidéos et appels à l'action. | Ne pas utiliser la publicité dynamique est une opportunité manquée d'automatiser les tests créatifs. Pour les nouvelles campagnes, activer cette option et fournir plusieurs ressources (au moins 3-5 images/vidéos, 3 textes, 3 titres). |
| **Adaptation aux Placements** | Les créatives sont adaptées aux formats de chaque placement principal (ex: format 9:16 pour les Stories/Reels, 1:1 pour le Feed). | Utiliser une seule créative 16:9 pour tous les placements résulte en un affichage tronqué et peu professionnel, nuisant gravement à la performance. Utiliser l'outil de personnalisation par placement au niveau de la publicité pour télécharger des créatives spécifiques à chaque format. |
| **Renouvellement des Créatives** | Un processus de renouvellement des créatives est en place pour lutter contre la fatigue publicitaire (ad fatigue). De nouvelles créatives sont introduites régulièrement (au moins toutes les 2-4 semaines pour les campagnes actives). | Des créatives qui tournent depuis des mois voient inévitablement leur performance décliner (hausse du CPM, baisse du CTR). Analyser la fréquence et mettre en place un calendrier de production et de test de nouvelles créatives. |
| **Qualité Technique des Visuels** | Les images et vidéos sont en haute résolution, sans compression excessive. Le texte incrusté dans les images est limité (règle des 20% de texte, bien que moins stricte, reste une bonne pratique). | Des visuels de mauvaise qualité décrédibilisent la marque et sont pénalisés par l'algorithme. Utiliser des ressources de haute qualité et respecter les spécifications techniques recommandées par Meta pour chaque format. |


## 10. Historique de Performance : Apprendre du Passé

L'analyse de l'historique des performances du compte est essentielle pour comprendre ce qui a fonctionné et ce qui a échoué. Cette analyse rétrospective permet d'identifier des tendances, de comprendre la saisonnalité et de poser des diagnostics sur les problèmes de performance passés. C'est une étape cruciale pour éclairer les décisions stratégiques futures.

### Analyse Structurée des Données

Il ne s'agit pas simplement de regarder le ROAS global. Une analyse approfondie nécessite de segmenter les données par période, par type de campagne (acquisition vs. retargeting), par audience et par créative. L'objectif est de transformer les données brutes en informations actionnables.

| Élément à Vérifier | Valeur Attendue | Actions Correctives en Cas de Problème |
| :--- | :--- | :--- |
| **Tendances des KPIs Clés** | Les KPIs principaux (CPM, CTR, Coût par Achat, ROAS) sont analysés sur différentes périodes (30, 90, 365 jours) pour identifier des tendances à la hausse ou à la baisse. | Une dégradation progressive des performances peut indiquer une saturation de l'audience ou une fatigue créative. Utiliser les graphiques de performance du Gestionnaire de Publicités pour visualiser ces tendances. |
| **Performance par Funnel** | Les performances des campagnes de prospection (Prospecting) et de reciblage (Retargeting) sont analysées séparément. | Le ROAS attendu n'est pas le même pour ces deux types de campagnes. Un ROAS de prospection de 1.5 peut être excellent, tandis qu'un ROAS de retargeting de 3 peut être décevant. Analyser la contribution de chaque partie du funnel au résultat global. |
| **Analyse des "Top Performers" et "Worst Performers"** | Les campagnes, ad sets, et publicités les plus et les moins performants sont clairement identifiés. | Comprendre les caractéristiques communes des gagnants (audience, angle créatif, promotion) pour les répliquer. Analyser les perdants pour éviter de répéter les mêmes erreurs. |
| **Impact des Changements** | L'impact des changements majeurs (ex: lancement d'une nouvelle gamme de produits, changement de stratégie de ciblage) sur les performances est analysé. | Corréler les variations de performance avec le journal d'activité du compte (si disponible) ou avec le calendrier marketing de l'entreprise pour comprendre les relations de cause à effet. |


## Apprentissages Terrain

*Cette section est destinée à être complétée au fil des audits réels. Elle recueillera les observations pratiques, les cas particuliers et les nouvelles tendances non documentées officiellement qui seront découvertes sur le terrain. Chaque apprentissage devra être daté et contextualisé.*


## Références

1. [Meta for Developers: Conversions API Best Practices](https://developers.facebook.com/docs/marketing-api/conversions-api/best-practices/)
2. [Meta Business Help Centre: About Aggregated Event Measurement](https://www.facebook.com/business/help/721422165168351)
3. [Shopify Help Center: Facebook & Instagram app](https://help.shopify.com/en/manual/promoting-marketing/create-marketing/facebook)
4. [Lebesgue: How to do a Comprehensive Facebook Ads Audit in 2024](https://lebesgue.io/product-features/how-to-do-a-comprehensive-facebook-ads-audit-in-2024)
5. [Socium Media: How To Conduct a Facebook Ads Audit](https://www.sociummedia.com/blog/facebook-ads-audit-guide/)
