
_# Stratégie Créative dans l'Ère Andromeda : Entity IDs et Diversité Visuelle

## Introduction : La Créative comme Levier Central de Performance

Dans l'écosystème publicitaire de Meta, profondément transformé par l'avènement du système de recommandation **Andromeda**, la stratégie créative n'est plus une simple composante de la campagne, mais bien son cœur névralgique. Loin de l'ère du ciblage manuel et des optimisations granulaires, la performance repose désormais sur la capacité des annonceurs à fournir au système un flux constant d'actifs visuels pertinents et diversifiés. La créative est devenue le principal langage de communication avec l'algorithme, un levier stratégique pour guider la diffusion, optimiser les coûts et, in fine, atteindre les objectifs business.

Ce document de référence technique explore en profondeur les mécaniques de la stratégie créative moderne sur Meta. Il détaille les concepts fondamentaux liés à l'architecture d'Andromeda, tels que les **Entity IDs**, et présente un framework actionnable pour structurer la production et le déploiement des créatives à travers le funnel de conversion. L'objectif est de fournir aux experts Meta Ads une compréhension fine des nouvelles règles du jeu et les outils pour construire des stratégies créatives robustes, scalables et performantes à l'horizon 2024-2026.

## 1. L'Ère Andromeda et la Révolution des "Entity IDs"

Pour saisir l'importance de la créative, il est impératif de comprendre le fonctionnement d'Andromeda, le modèle d'intelligence artificielle qui gouverne la diffusion des publicités sur les plateformes Meta. Andromeda opère une sélection et une recommandation de contenus (organiques et payants) à très grande échelle, en s'appuyant sur une analyse prédictive du comportement des utilisateurs. Au cœur de ce système se trouvent les **"Entity IDs"**, des identifiants uniques assignés à chaque composant d'une campagne.

> **Définition : Entity ID**
> Un "Entity ID" est un identifiant unique que le système Meta assigne à chaque objet publicitaire : la campagne, l'ad set, et surtout, chaque créative individuelle (image, vidéo). Cet ID est immuable et sert de clé de voûte pour l'apprentissage du système. Toute l'historique de performance, les signaux d'engagement (clics, partages, temps de visionnage) et les conversions sont agrégés au niveau de cet Entity ID.

La conséquence de cette architecture est fondamentale : la performance est attachée à la créative elle-même, et non à l'ad set ou à l'audience. Lorsqu'une créative est dupliquée dans un autre ad set, elle conserve son Entity ID et l'historique de performance qui y est associé. Ce mécanisme, souvent désigné par le terme de "social proofing" ou "post ID trick", est en réalité une interaction fondamentale avec le moteur d'apprentissage de Meta. Le système reconnaît une créative performante et utilise cet historique pour accélérer sa diffusion et optimiser ses placements futurs, indépendamment de la configuration de l'ad set.

### 1.1. La Diversité Visuelle comme Carburant de l'Algorithme

Andromeda prospère sur la diversité. Le système cherche constamment à explorer de nouvelles associations entre une créative et une micro-audience pour affiner sa compréhension et maximiser la valeur pour l'utilisateur et l'annonceur. Fournir un volume important d'actifs visuellement distincts est donc essentiel pour "nourrir" l'algorithme et lui permettre de trouver les combinaisons les plus performantes. Une stratégie reposant sur un faible nombre de créatives, même si elles sont initialement performantes, s'expose à une saturation rapide (ad fatigue) et à une hausse des coûts de diffusion (CPM).

Le concept de **"Creative Cost Multiplier"** illustre ce principe : Meta subventionne la distribution des nouvelles créatives de qualité. Le système est prêt à accepter un coût par résultat (CPA) initialement plus élevé sur un nouvel asset, car il y voit une opportunité d'apprentissage et d'exploration. Une créative qui génère des signaux d'engagement positifs et variés (indiquant qu'elle résonne avec différents segments d'audience) verra son CPM baisser progressivement, le système la "récompensant" pour sa contribution à l'écosystème. À l'inverse, une créative usée ou peu engageante sera pénalisée par des CPM croissants, le système cherchant à limiter son exposition.

La règle empirique des **10 à 15 assets distincts** par cycle de test (ou par semaine) est une ligne directrice pragmatique. Il ne s'agit pas de décliner la même idée en 15 couleurs, mais bien de proposer 10 à 15 concepts, angles ou formats radicalement différents pour maximiser les chances de découverte et alimenter le moteur d'exploration d'Andromeda.

## 2. Framework Créatif par Funnel de Conversion

Une stratégie créative efficace ne se contente pas de produire des assets en volume ; elle les articule de manière cohérente à travers le parcours client. Le modèle classique **TOF (Top of Funnel), MOF (Middle of Funnel), et BOF (Bottom of Funnel)** reste un cadre pertinent pour structurer la production créative, à condition d'adapter les objectifs et les messages aux signaux attendus par l'algorithme à chaque étape.

| Étape du Funnel | Objectif Principal | Indicateurs Clés (Signaux pour l'IA) | Types de Créatives Privilégiés |
| :--- | :--- | :--- | :--- |
| **TOF (Top of Funnel)** | Capturer l'attention, Éduquer, Inspirer | Taux de visionnage (3s, ThruPlay), Taux de Stop (Thumb Stop Ratio), Partages, Commentaires | Vidéos courtes (Reels), UGC authentique, Visuels à fort impact, Storytelling |
| **MOF (Middle of Funnel)** | Susciter la considération, Démontrer la valeur | Clics sur le lien (CTR), Visites de page de destination, Temps passé sur le site, Ajouts au panier | Carrousels, Collections, Démos produit, Témoignages clients, Comparatifs |
| **BOF (Bottom of Funnel)** | Inciter à l'action, Lever les freins | Achats, Leads, Taux de conversion, ROAS | Offres promotionnelles, Urgence (stock limité), Dynamic Product Ads (DPA), Réassurance (livraison, retours) |

### 2.1. Top of Funnel (TOF) : La Bataille de l'Attention

En haut du funnel, l'objectif est de capter une audience large qui n'a pas encore manifesté d'intérêt direct pour la marque ou le produit. La créative doit être conçue pour stopper le scroll et générer un engagement rapide. Le système Meta valorise ici les signaux d'interaction sociale et de consommation de contenu. Une vidéo qui est regardée jusqu'au bout et partagée enverra un signal extrêmement positif, même si elle ne génère pas de clic immédiat. Le but est de créer une "empreinte mémorielle" et d'identifier les segments d'audience les plus réceptifs.

**Exemple de créative TOF :** Une marque de vêtements de sport pourrait utiliser une vidéo Reel montrant un athlète réalisant une performance impressionnante, sans mentionner directement un produit. Le focus est sur l'émotion, l'inspiration et l'association de la marque à des valeurs de dépassement de soi. Le son, les sous-titres et un rythme rapide sont essentiels pour performer sur ce format.

### 2.2. Middle of Funnel (MOF) : La Construction de la Confiance

À cette étape, l'audience a déjà eu un premier contact avec la marque. L'enjeu est de l'éduquer sur la proposition de valeur et de la faire passer de simple spectateur à prospect qualifié. Les créatives doivent être plus informatives et centrées sur le produit ou le service. Les formats comme les carrousels permettent de détailler plusieurs bénéfices ou de présenter différentes facettes d'un produit. Les témoignages clients (UGC ou studio) sont particulièrement efficaces pour bâtir la confiance et la preuve sociale.

**Exemple de créative MOF :** La même marque de vêtements de sport pourrait utiliser un carrousel. La première slide montre le produit en situation, les suivantes détaillent les caractéristiques techniques (tissu respirant, coutures plates), une slide présente un avis client 5 étoiles, et la dernière slide incite à découvrir la collection complète via un appel à l'action clair.

### 2.3. Bottom of Funnel (BOF) : La Conversion

En bas du funnel, on s'adresse à une audience chaude, qui a visité le site, ajouté un produit au panier ou interagi de manière significative. La créative doit être directe, transactionnelle et lever les derniers freins à l'achat. Les Dynamic Product Ads (DPA), qui affichent automatiquement les produits consultés par l'utilisateur, sont un pilier de cette étape. On y ajoute des éléments de réassurance (livraison gratuite, retours faciles, garantie) et des leviers d'urgence ou de rareté pour accélérer la décision.

**Exemple de créative BOF :** Un DPA affiche la paire de chaussures de running exacte que l'utilisateur a consultée. Le texte de l'annonce mentionne une offre à durée limitée ("-15% pendant 24h") et une bannière superposée à l'image rappelle "Livraison et Retours Gratuits". L'objectif est de minimiser la friction et de maximiser le taux de conversion.


## 3. Typologie des Créatives Performantes

La performance sur Meta Ads repose sur un portefeuille diversifié de types de créatives. Chaque format a ses forces et répond à des objectifs spécifiques. Une stratégie mature combine ces différents types pour couvrir l'ensemble du spectre de communication, de l'authenticité brute à l'esthétique de marque parfaitement maîtrisée.

### 3.1. User-Generated Content (UGC)

L'UGC est sans doute le type de créative le plus puissant en termes d'authenticité et de preuve sociale. Il s'agit de contenus (vidéos, images) créés par des clients ou des créateurs de contenu qui présentent le produit dans un contexte réel, non scénarisé. Son efficacité repose sur la rupture avec le langage publicitaire traditionnel, ce qui génère un niveau de confiance et d'identification très élevé.

*   **Pourquoi ça fonctionne :** L'UGC imite le contenu natif que les utilisateurs consomment sur leurs feeds. Il est perçu comme un conseil d'ami plutôt que comme une publicité, ce qui abaisse les barrières psychologiques et augmente l'engagement.
*   **Utilisation :** Idéal en TOF pour capter l'attention avec un contenu authentique, et en MOF pour renforcer la confiance avec des témoignages et des cas d'usage réels.

### 3.2. Créatives Studio

Les créatives "studio" désignent les contenus produits de manière professionnelle, avec un contrôle total sur l'éclairage, le cadrage, le message et l'esthétique. Cela inclut les photos de produits sur fond neutre (packshots), les vidéos de démonstration léchées ou les publicités scénarisées. Leur force réside dans la capacité à transmettre une image de marque premium et à présenter le produit sous son meilleur jour.

*   **Pourquoi ça fonctionne :** Elles communiquent la qualité, le professionnalisme et permettent une clarté de message inégalée. Elles sont essentielles pour construire une image de marque forte et cohérente.
*   **Utilisation :** Efficaces en MOF pour détailler les caractéristiques du produit et en BOF pour les publicités de catalogue dynamique où la clarté de l'image produit est primordiale.

### 3.3. Text-Overlay et Titres Accrocheurs

Le "Text-Overlay" consiste à superposer du texte directement sur l'image ou la vidéo. C'est un élément crucial, car une grande partie des vidéos sont visionnées sans le son. Le texte doit communiquer l'idée principale dans les 3 premières secondes. Il peut s'agir d'une question qui interpelle, d'un bénéfice clé ou d'une statistique choc. L'objectif est de donner un contexte immédiat et de retenir l'attention.

*   **Pourquoi ça fonctionne :** Il garantit la transmission du message clé, même sans son, et permet de structurer le storytelling de la vidéo. Un bon titre est la première accroche de la publicité.
*   **Utilisation :** Transversal à tous les types de créatives vidéo et à toutes les étapes du funnel.

### 3.4. Carrousel et Collections

Le format carrousel permet de présenter jusqu'à 10 images ou vidéos dans une seule annonce, chacune avec son propre titre, sa description et son lien. C'est un format interactif qui invite l'utilisateur à "swiper". Les annonces de type "Collection" sont une version plus immersive, qui s'ouvre en plein écran (Instant Experience) et permet de créer une mini-landing page au sein même de l'application Meta.

*   **Pourquoi ça fonctionne :** Idéal pour le storytelling, pour présenter plusieurs produits, pour détailler les étapes d'un processus ou pour lister plusieurs bénéfices. L'interactivité augmente le temps passé sur l'annonce, un signal positif pour l'algorithme.
*   **Utilisation :** Particulièrement performant en MOF pour éduquer l'audience et en BOF pour présenter une gamme de produits ou des offres groupées.

### 3.5. Catalogue Dynamique (Dynamic Product Ads - DPA)

Les DPA sont le pilier des stratégies de retargeting. Elles utilisent le catalogue de produits de l'annonceur pour afficher dynamiquement les produits pertinents à chaque utilisateur, en fonction de son comportement sur le site web ou l'application (produits vus, ajoutés au panier, etc.). La personnalisation est maximale, ce qui se traduit par des taux de conversion très élevés.

*   **Pourquoi ça fonctionne :** La pertinence est absolue. En montrant à l'utilisateur exactement ce qui l'intéresse, on élimine toute friction et on le ramène de manière fluide dans le tunnel d'achat.
*   **Utilisation :** Strictement en BOF pour le retargeting et la finalisation des ventes.


## 4. Production Créative : Workflow Hybride et Adaptation aux Formats

La nécessité de produire un volume élevé d'assets diversifiés a transformé les workflows de production créative. L'approche traditionnelle, lente et coûteuse, n'est plus viable. L'avenir réside dans un modèle hybride, combinant l'efficacité et la capacité d'idéation de l'intelligence artificielle avec l'intuition stratégique et la supervision humaine.

### 4.1. Le Workflow de Production IA + Humain

Les outils d'IA générative (GenAI) comme **Midjourney**, **Sora de OpenAI**, et les modèles de la famille **GEM de Google** ne sont plus des gadgets, mais des outils de production à part entière. Ils permettent d'explorer des concepts visuels à une vitesse et une échelle sans précédent. Un workflow moderne pourrait se structurer comme suit :

1.  **Briefing Stratégique (Humain) :** Le stratège publicitaire définit les objectifs, l'audience, l'angle du message et le rôle de la créative dans le funnel. Ce brief reste une étape fondamentalement humaine, basée sur la compréhension du marché et de la psychologie du consommateur.

2.  **Idéation et Prototypage (IA) :** À partir du brief, des outils comme Midjourney ou DALL-E 3 sont utilisés pour générer des dizaines de concepts visuels (mood boards, scènes clés, styles graphiques). Pour la vidéo, des outils comme Sora ou Pomelli permettent de créer des storyboards animés ou des séquences complètes à partir de prompts textuels. Cette étape, qui prenait des jours, peut être réalisée en quelques heures.

3.  **Sélection et Raffinement (Humain) :** Le directeur artistique ou le stratège sélectionne les concepts les plus prometteurs générés par l'IA. Ces concepts sont ensuite affinés, soit en itérant sur les prompts, soit en les important dans des logiciels de retouche traditionnels (Suite Adobe) pour des ajustements fins, l'ajout de branding, etc.

4.  **Production des Déclinaisons (IA + Humain) :** Une fois le concept validé, l'IA peut être utilisée pour générer des variations (changement de décor, de personnage, de couleur). Des outils d'automatisation permettent ensuite de décliner la créative maîtresse dans tous les formats requis, en y ajoutant les textes, les logos et les appels à l'action. La supervision humaine garantit la cohérence et la qualité de chaque déclinaison.

**Exemple de workflow :** Pour une marque de café, le brief est "créer une vidéo courte pour Reels (TOF) montrant le rituel du café du matin comme un moment de luxe et de calme".
*   **IA (Sora/GEM) :** Prompt : "Vidéo 4K ultra-réaliste, style cinématique, d'une femme dans un loft parisien au lever du soleil. La lumière dorée filtre à travers la fenêtre. Elle verse lentement un café d'une cafetière Chemex dans une tasse en céramique. Vapeur visible. Ambiance sereine et luxueuse. Format 9:16."
*   **Humain :** Sélection de la meilleure génération. Ajout en post-production du logo de la marque en surimpression discrète et d'un overlay texte : "Votre luxe quotidien".
*   **IA + Humain :** Création de variations : une version avec un homme, une version dans un décor plus moderne, une version zoomée sur le café. Déclinaison en format 1:1 pour le feed avec un recadrage intelligent.

### 4.2. Adaptation aux Placements : La Règle du 9:16 vs 1:1

Produire une créative ne suffit pas ; il faut la penser pour les placements où elle sera diffusée. L'erreur la plus commune est d'utiliser un seul format (souvent 16:9, hérité de la vidéo classique) pour tous les placements. C'est une garantie de sous-performance. Chaque placement a ses propres codes et son propre ratio.

| Placement | Ratio | Comportement de l'Utilisateur | Bonnes Pratiques Créatives |
| :--- | :--- | :--- | :--- |
| **Reels / Stories** | 9:16 (Vertical) | Consommation rapide, divertissement, son souvent activé | Contenu immersif plein écran, sous-titres visibles, message clé dans les 2 premières secondes, rythme dynamique. |
| **Feed (Fil d'actualité)** | 1:1 (Carré) ou 4:5 | Scroll plus lent, lecture de texte, découverte | Visuel fort qui se démarque, texte de l'annonce travaillé, le carré maximise l'espace sur l'écran mobile. |
| **In-Stream Vidéo** | 16:9 (Horizontal) | Attente passive (publicité avant une vidéo choisie), son activé | Format plus traditionnel, storytelling possible, mais l'accroche doit être immédiate pour éviter le "skip". |

La stratégie "one size fits all" est morte. Il est impératif de concevoir ou à minima d'adapter les créatives pour les deux formats dominants : le **9:16** pour l'écosystème immersif des Reels et Stories, et le **1:1** (ou 4:5) pour la visibilité dans le Feed. L'utilisation de l'outil de personnalisation par placement (Asset Customization) dans le Ads Manager est non négociable pour toute campagne sérieuse.

### 4.3. Cohérence de Marque vs. Diversité Créative

Un défi majeur est de concilier le besoin de diversité créative pour nourrir l'algorithme avec l'impératif de construire une marque cohérente et reconnaissable. La solution n'est pas dans le compromis, mais dans la définition d'un "cadre de jeu" créatif.

Ce cadre peut inclure des éléments intangibles (tonalité, valeurs) et tangibles (palette de couleurs, typographie, style de logo, type de modèles). À l'intérieur de ce cadre, la liberté d'expérimentation doit être maximale. On peut tester de l'UGC, des visuels IA, des carrousels, des mèmes, tant que ces créations respectent les piliers de l'identité de marque. La cohérence n'est pas la monotonie. Une marque forte est reconnaissable même à travers une multitude d'exécutions créatives différentes.

Le **calendrier créatif** devient alors un outil stratégique, au même titre qu'une roadmap produit. Il planifie les cycles de production, les concepts à tester, les formats à produire et les moments clés de l'année, en s'assurant que le flux d'assets créatifs ne se tarit jamais.

## 5. Apprentissages Terrain

*Cette section est destinée à être complétée au fur et à mesure des analyses de campagnes et des tests réalisés. Elle a pour but de capitaliser sur les apprentissages spécifiques au contexte de chaque annonceur.*

*   **[Date] - [Observation] :** [Détail de l'apprentissage, ex: "Le test de créatives UGC vs Studio sur l'audience X a montré une surperformance de 30% du CPA en faveur de l'UGC en TOF, mais une inversion de la tendance en MOF."]
*   **[Date] - [Observation] :** [Détail de l'apprentissage]


## Références

1.  Meta for Business. (2023). *"The Role of Creative in a New Era of Performance."* [Lien interne ou fictif]
2.  Google AI. (2024). *"GEM: Unlocking the Future of Multimodal AI."* [Lien interne ou fictif]
3.  OpenAI. (2024). *"Sora: Creating Video from Text."* [Lien interne ou fictif]
