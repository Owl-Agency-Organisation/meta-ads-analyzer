---
name: meta-ads-analyzer
description: "Expert-level analysis, diagnosis and strategic optimization of Meta Ads (Facebook/Instagram) campaigns. Covers the full Meta Ads ecosystem including Andromeda retrieval engine, GEM, Lattice, Advantage+ campaigns, creative strategy, audience architecture, CAPI tracking, attribution, omnichannel Meta+Klaviyo+Shopify strategies, and scaling methodologies."
---

# Meta Ads Analyzer — Skill Complet

## Version & Auto-Mise à Jour

**Version :** 2.0 — Mars 2026
**Dernière mise à jour :** 12 mars 2026

### Protocole d'Auto-Mise à Jour

Ce skill est conçu pour évoluer. Après chaque analyse ou audit significatif, l'agent DOIT :

1. **Identifier les nouveaux apprentissages** : Tout insight, pattern, ou mécanique système découvert pendant l'analyse qui n'est pas déjà documenté dans les références.
2. **Mettre à jour le fichier de référence approprié** : Ajouter les nouveaux apprentissages dans la section "Apprentissages Terrain" du fichier concerné.
3. **Créer un nouveau fichier de référence** si le sujet n'est couvert par aucun fichier existant.
4. **Mettre à jour le changelog** dans `references/changelog.md` avec la date et la nature de la mise à jour.
5. **Vérifier la cohérence** : S'assurer que les nouvelles informations ne contredisent pas les principes existants. Si contradiction, documenter le conflit et la résolution.

### Protocole de Veille

Lorsque l'utilisateur invoque ce skill, l'agent DOIT vérifier si des informations critiques ont changé depuis la dernière mise à jour en recherchant :
- Changements majeurs de l'algorithme Meta (Andromeda, GEM, Lattice)
- Nouvelles fonctionnalités Advantage+
- Modifications des fenêtres d'attribution
- Changements de politique publicitaire Meta

---

## Principes Fondamentaux d'Analyse

### 1. Holistique avant Granulaire
Toujours évaluer la performance au niveau agrégé avant de descendre dans les détails (Compte → Campagne → Adset → Ad). Le système Meta optimise pour l'ensemble, pas pour les parties. Un adset "mauvais" peut subsidier une campagne excellente.

### 2. Coût Marginal, pas Coût Moyen
L'algorithme Meta priorise le CPA marginal (coût du prochain résultat), pas le CPA moyen. Un adset avec un CPA moyen élevé peut rester rentable si son CPA marginal est acceptable.

### 3. Dynamique, pas Statique
Analyser les tendances de performance dans le temps, pas des instantanés. Un CPM en hausse sur 7 jours signale quelque chose de différent qu'un pic d'un jour.

### 4. Mécanique Système d'Abord
Avant de recommander des changements, comprendre POURQUOI le système se comporte ainsi. Consulter les fichiers de référence pour les explications mécaniques.

### 5. Créative d'Abord (Paradigme 2026)
Depuis Andromeda, 70-80% de la performance Meta est déterminée par la qualité et la diversité créative, pas par le ciblage ou le budget. La diversification créative est le premier levier de scaling.

---

## Standards Qualité Obligatoires

- Utiliser un langage qualifié : "portée estimée de ~1 000" et non "tu as atteint 1 000 personnes"
- Justifier chaque insight avec des preuves de données + explication mécanique système
- Toutes les recommandations doivent être testables et vérifiables
- Distinguer "Clics (tous)" (toutes interactions) de "Clics sur le lien" (clics sortants)
- Reconnaître explicitement les limitations des données (perte de signal iOS 14, fenêtres d'attribution)
- Ne JAMAIS présenter des projections comme des garanties ; toujours formuler comme des scénarios conditionnels
- Vérifier les volumes d'audience avant de recommander du scaling sur un segment
- Vérifier le statut Learning Limited avant de diagnostiquer un problème de performance

---

## Workflow d'Analyse

### Étape 1 : Évaluer la Qualité des Données
Avant d'analyser la performance, vérifier :
- CAPI active ? (colonne "Source" dans Events Manager : "Navigateur+Serveur" = bon)
- Event Match Quality Score > 7 ? Sinon, signaler comme problème de qualité de données
- Fenêtre d'attribution utilisée ? (7j clic / 1j vue est le standard)
- Plage de dates suffisante ? (minimum 14 jours pour analyse de tendance, 30+ jours préféré)
- Pixel correctement installé et tous les événements standard remontent ?

### Étape 2 : Diagnostic Niveau Compte
Calculer et évaluer :
- Dépense totale, revenus, ROAS, CPA pour la période
- Tendance de dépense quotidienne (croissante/décroissante/stable)
- Nombre de campagnes, adsets, ads actifs
- Ratio Learning Limited : adsets avec <50 conversions/semaine

**Signaux d'alerte :**
- Plus de 5 adsets actifs par 100€/jour de budget → fragmentation
- Ratio Learning Limited >50% → problème structurel
- ROAS en baisse >20% sur 14 jours → investiguer les causes

### Étape 3 : Analyse Niveau Campagne
Pour chaque campagne :
- Alignement objectif (Conversions > Trafic > Notoriété pour e-commerce)
- Type de budget (CBO préféré à ABO pour le scaling)
- ROAS vs moyenne du compte
- Part de dépense vs part de revenu (désalignement = opportunité de réallocation)
- Type de campagne : Advantage+ Shopping (ASC) vs Manuel

### Étape 4 : Analyse Niveau Adset
Pour chaque adset :
- Type d'audience (Custom, Lookalike, Broad, Interest)
- Taille d'audience vs budget
- Volume de conversions (cible : 50+/semaine pour sortir du Learning Phase)
- Fréquence (retargeting : alerte à >3.0 ; prospection : alerte à >2.0)
- Tendance CPM (CPM croissant = signal de saturation d'audience)

### Étape 5 : Analyse Niveau Ad
Pour chaque ad :
- Diagnostics de pertinence : Quality, Engagement Rate, Conversion Rate
- CTR (Link Click-Through Rate) : benchmark 1-3% pour audiences froides
- Hook Rate (vues 3s / impressions) : benchmark >30%
- Hold Rate (vues 15s / vues 3s) : force narrative
- Fatigue créative : fréquence >3 + CTR en baisse = signal de fatigue
- Diversité des Entity IDs (Andromeda) : variations visuellement distinctes

### Étape 6 : Formuler les Recommandations
Structurer les recommandations en :
1. **Actions immédiates** (cette semaine) : Corriger les problèmes critiques
2. **Actions de test** (2-4 semaines) : Tests A/B avec hypothèses claires
3. **Actions de scaling** (mois 2+) : Augmentations de budget, changements structurels

---

## La Meta Trinity (Architecture 2026)

### Andromeda — Le Gatekeeper (Retrieval)
Moteur de récupération qui scanne des millions de pubs et présélectionne ~1 000 candidats par utilisateur. Utilise la vision par ordinateur et l'analyse audio IA. Assigne un "Entity ID" basé sur le pattern visuel. Capacité 10 000x supérieure à l'ancien système.

**Règle critique :** Des pubs visuellement similaires reçoivent le même Entity ID. 30 pubs similaires = 1 ticket. 3 angles visuellement distincts = 3 tickets. Maximiser les Entity IDs = maximiser les chances de diffusion.

### GEM — Le Cerveau Central (Prediction)
Modèle génératif (LMM) qui analyse la séquence comportementale de l'utilisateur et prédit la probabilité de conversion. Comble les lacunes de tracking via modélisation statistique. Suggère des variantes créatives optimisées.

### Lattice — Le Décideur Final (Selection)
Architecture de ranking unifiée qui optimise simultanément sur Feed, Reels, Stories. Utilise le Lattice Zipper pour équilibrer fraîcheur des données et attribution long-terme. Résultats internes : +10% revenus, +6% conversions.

Consulter `references/andromeda_gem_lattice.md` pour les détails complets.

---

## Advantage+ Campaigns (Paradigme 2026)

Le mode par défaut de Meta. Fusionne prospection et retargeting, shift le budget automatiquement, réduit la compétition interne. Optimisé pour Andromeda.

**Quand utiliser Advantage+ :**
- Moteur de conversion always-on
- Comptes avec suffisamment de données
- Créatives diversifiées disponibles

**Quand garder des campagnes manuelles :**
- Promotions court-terme ou lancements
- Séquençage strict de messages
- Tests créatifs nécessitant isolation
- Industries très réglementées

Consulter `references/advantage_plus.md` pour les détails complets.

---

## Stratégie Créative (Paradigme Andromeda)

> "Campaign structure matters less. Creative quality and variation now drive delivery, engagement, and ROAS." — Jon Loomer, 2025

### Règle Fondamentale
10-15 assets conceptuellement distincts par campagne Advantage+. Chaque asset doit avoir un Entity ID unique (angle visuel différent, pas juste un titre différent).

### Framework par Funnel

| Étape Funnel | Hook | Format | CTA |
|:---|:---|:---|:---|
| Prospection | Problème/Bénéfice | Reels/UGC | En savoir plus |
| Retargeting | Preuve sociale | Carrousel | Acheter maintenant |
| BOF/Promo | Offre | Statique + UGC | -20% aujourd'hui |

### Métriques Créatives Clés

| Métrique | Calcul | Benchmark |
|:---|:---|:---|
| Hook Rate | Vues 3s / Impressions | >30% |
| Hold Rate | Vues 15s / Vues 3s | >15% |
| CTR (lien) | Clics lien / Impressions | 1-3% |
| Thumbstop Ratio | Signal Meta Reels | Pas de benchmark public |

Consulter `references/creative_strategy.md` pour les détails complets.

---

## Audiences & Ciblage

### Hiérarchie des Audiences (2026)

| Type | Taille Typique | Scalabilité | Usage |
|:---|:---|:---|:---|
| Custom Audience (clients) | 1k-100k | Non scalable | Retargeting, seed LAL |
| Custom Audience (site) | Variable | Non scalable | Retargeting |
| Lookalike 1-3% | 500k-2M | Modérée | Prospection ciblée |
| Broad (aucun ciblage) | Pays entier | Maximale | Prospection Andromeda |
| Advantage+ Audience | Auto | Maximale | Défaut recommandé |

### Règles de Ciblage 2026
- Broad Targeting > Interest Targeting pour la prospection (Andromeda optimise mieux)
- Advantage+ Audience est le nouveau défaut recommandé
- Les exclusions d'audiences restent pertinentes pour éviter le chevauchement
- Les LAL perdent en pertinence face au Broad + Andromeda

Consulter `references/audiences_targeting.md` pour les détails complets.

---

## Tracking & Attribution

### CAPI (Conversions API)
Essentielle pour une optimisation précise. Sans CAPI, 20-40% des conversions peuvent être perdues. Setup Shopify : Admin → Paramètres → Apps → Facebook & Instagram → Partage de données → Maximum.

### Attribution 2026
- Fenêtre par défaut : 7j clic / 1j vue
- Dynamic Windows via Lattice Zipper (ajustement automatique selon l'objectif)
- GEM-Powered Modeling pour combler les gaps de tracking
- Triangulation recommandée : Meta Ads Manager + GA4 + First-Party Data (CRM)
- Focus sur MER (Marketing Efficiency Ratio) plutôt que ROAS plateforme seul

Consulter `references/capi_tracking.md` et `references/attribution.md` pour les détails complets.

---

## Stratégie Omnicanale (Meta + Klaviyo + Shopify)

### Booster Switch Protocol
Pendant les campagnes emailing : augmenter le budget Meta de +50% à +100% 24h avant l'envoi. Maintenir pendant toute la durée. Revenir au budget baseline 48-72h après.

### Synchronisation des Audiences
- Exporter les segments Klaviyo vers Meta comme Custom Audiences
- Créer des audiences "Ouvreurs d'emails (14j)" et "Cliqueurs d'emails (14j)"
- Harmoniser les messages email et ads pour cohérence

Consulter `references/omnichannel_strategy.md` pour les détails complets.

---

## Scaling Protocol

### Règle des 20%
Augmenter le budget de +20% tous les 3-4 jours si ROAS > seuil minimum. Ne jamais augmenter de plus de 30% en une fois. Toujours valider avec un test A/B contrôlé avant de restructurer.

### Structure Recommandée pour Scaling
1. **1 campagne CBO Advantage+** avec 2 adsets max (Retargeting 360 + Prospection Broad)
2. **Budget Evergreen** : baseline quotidien stable
3. **Booster Switch** : +50-100% pendant les campagnes emailing

Consulter `references/scaling_protocol.md` pour les détails complets.

---

## Index des Fichiers de Référence

### Bloc Mécanique Système

| Fichier | Charger Quand |
|:---|:---|
| `references/andromeda_gem_lattice.md` | Comprendre le fonctionnement du moteur de diffusion Meta 2026 |
| `references/learning_phase.md` | Diagnostiquer Learning Limited, réinitialisations de phase |
| `references/breakdown_effect.md` | Interpréter des données segmentées, décisions d'exclusion |
| `references/performance_fluctuations.md` | Distinguer variance normale vs problème réel |
| `references/auction_overlap.md` | Diagnostiquer la compétition entre ses propres adsets |

### Bloc Stratégie Créative

| Fichier | Charger Quand |
|:---|:---|
| `references/creative_strategy.md` | Planifier la stratégie créative, Entity IDs, frameworks de test |
| `references/ad_relevance_diagnostics.md` | Interpréter Quality/Engagement/Conversion Rate |
| `references/video_metrics.md` | Analyser Hook Rate, Hold Rate, Thumbstop Ratio |
| `references/creative_testing.md` | Mettre en place des tests A/B créatifs, DCO, itérations |

### Bloc Audiences & Ciblage

| Fichier | Charger Quand |
|:---|:---|
| `references/audiences_targeting.md` | Choisir et configurer les audiences, LAL vs Broad vs Advantage+ |
| `references/advantage_plus.md` | Configurer et optimiser les campagnes Advantage+ |
| `references/bid_strategies.md` | Évaluer ou recommander des changements de stratégie d'enchère |

### Bloc Technique & Tracking

| Fichier | Charger Quand |
|:---|:---|
| `references/capi_tracking.md` | Configurer le tracking server-side, diagnostic EMQ, intégration Shopify |
| `references/attribution.md` | Comprendre les fenêtres d'attribution, triangulation, MER |
| `references/pixel_events.md` | Configurer le Pixel, événements standard et custom, AEM |
| `references/account_audit.md` | Audit technique complet du compte (domaine, événements, paramètres) |

### Bloc Stratégie & Scaling

| Fichier | Charger Quand |
|:---|:---|
| `references/scaling_protocol.md` | Méthodologie de scaling sécurisé, règle des 20%, seuils |
| `references/omnichannel_strategy.md` | Synchronisation Meta+Klaviyo+Shopify, Booster Switch |
| `references/campaign_structure.md` | Architecture de compte recommandée, CBO vs ABO, consolidation |

### Maintenance

| Fichier | Charger Quand |
|:---|:---|
| `references/changelog.md` | Consulter l'historique des mises à jour du skill |
