# Changelog — Skill meta-ads-analyzer

## Apprentissage terrain — 8 juin 2026 (Padel Mon Amour)

**Analyse Events Manager — Compte Padel Mon Amour**

### Patterns observés

**EMQ 6.1/10 avec CAPI active :**
- CAPI active ne garantit pas un bon EMQ. Le canal peut être opérationnel mais les paramètres client (email, phone, fbp, fbc, external_id) insuffisants → score dégradé.
- Correction prioritaire : passer le partage de données Shopify en "Maximum" + ajouter external_id.

**Anomalie AddPaymentInfo < Purchase :**
- 52 AddPaymentInfo vs 76 Purchase = les méthodes de paiement express (Apple Pay, Google Pay, Stripe one-click) bypassent l'étape "Add Payment Info".
- Ce pattern est normal pour les boutiques avec checkout rapide activé. Ne pas interpréter comme une erreur de tracking sauf si l'écart est très important (>50%).

**Optimisation ATC vs Purchase sur petit volume :**
- ~2.7 achats/jour → trop peu pour optimiser directement sur Purchase (objectif : 50 conversions/semaine).
- Stratégie de contournement via ATC logique mais à revoir dès que l'EMQ est corrigé et que le volume monte.

**5 actions Meta recommandées non traitées :**
- Les actions recommandées dans l'Events Manager sont souvent des corrections de paramètres CAPI. À traiter en priorité avant toute analyse de performance.

---

## Version 2.0 — 12 mars 2026

**Reconstruction complète du skill.**

### Nouveau SKILL.md
- Méthodologie exhaustive couvrant l'intégralité de l'écosystème Meta Ads
- Protocole d'auto-mise à jour intégré
- Protocole de veille pour détecter les changements Meta
- Section Meta Trinity (Andromeda, GEM, Lattice)
- Paradigme créatif 2026 (Entity IDs, diversification)

### 18 fichiers de référence créés

**Bloc Mécanique Système :**
- `andromeda_gem_lattice.md` — Meta Trinity complète (Andromeda, GEM, Lattice)
- `learning_phase.md` — Phase d'apprentissage et Learning Limited
- `breakdown_effect.md` — Effet de répartition et biais de segmentation
- `performance_fluctuations.md` — Fluctuations normales vs préoccupantes
- `auction_overlap.md` — Chevauchement d'enchères

**Bloc Stratégie Créative :**
- `creative_strategy.md` — Stratégie créative ère Andromeda
- `ad_relevance_diagnostics.md` — Diagnostics de pertinence publicitaire
- `video_metrics.md` — Métriques vidéo (Hook Rate, Hold Rate, etc.)
- `creative_testing.md` — Framework de test créatif

**Bloc Audiences & Ciblage :**
- `audiences_targeting.md` — Audiences et ciblage 2026
- `advantage_plus.md` — Campagnes Advantage+
- `bid_strategies.md` — Stratégies d'enchères

**Bloc Technique & Tracking :**
- `capi_tracking.md` — Conversions API (CAPI)
- `attribution.md` — Attribution et fenêtres d'attribution
- `pixel_events.md` — Pixel Meta et événements
- `account_audit.md` — Audit technique de compte

**Bloc Stratégie & Scaling :**
- `omnichannel_strategy.md` — Stratégie omnicanale Meta+Klaviyo+Shopify
- `campaign_structure.md` — Architecture de compte recommandée

### Sources principales
- Meta Engineering Blog (Andromeda, GEM, Lattice)
- Jon Loomer (83 changements Meta Ads 2025, attribution 2026)
- Smart Marketer (nouveau système Meta Ads 2026)
- Logical Position (Paid Social Playbook 2026)
- Stape.io (études de cas CAPI)
- Elevar (CAPI vs Pixel)

---

## Version 1.0 — 12 mars 2026 (session initiale)

Création initiale du skill avec 8 fichiers de référence basiques.
Couverture limitée aux concepts utilisés dans l'audit Mulebar.
