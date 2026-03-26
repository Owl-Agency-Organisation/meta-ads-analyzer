# Architecture de Compte Meta Ads Recommandée 2026

## Introduction : La Simplification comme Levier de Performance

## Les Mécaniques Internes de Meta : Comprendre Andromeda, GEM et Lattice

## CBO vs. ABO : Le Duel de l'Optimisation Budgétaire

## La Structure de Campagne Simplifiée : 1 à 3 Campagnes Maximum

## Consolidation des Adsets : La Puissance du Retargeting et de la Prospection

## Conventions de Nommage : Clarté et Rigueur pour le Scaling

## Quand Créer une Nouvelle Campagne vs. Ajouter un Adset ?

## La Structure Hybride : Advantage+ Always-On et Campagnes Manuelles Tactiques

## Budget Evergreen vs. Budget Booster : Gérer l'Investissement

## Erreurs Structurelles Courantes et Comment les Éviter

## Migration : D'une Structure Fragmentée à une Structure Consolidée

## Apprentissages Terrain

### 1. Règle du Budget Minimum par Publicité (26 mars 2026 - Cas Mulebar)

**Contexte** : Configuration Sprint 1 pour Mulebar (nutrition sportive, ~5k visiteurs/mois, budget 10€/jour).

**Erreur initiale** : Proposition de 8 publicités (2 anciennes + 6 nouvelles) dans campagne ASC avec budget 10€/jour.

**Problème identifié** :
```
Budget 10€/jour ÷ 8 pubs = 1,25€/pub/jour

Avec ROAS 3,0x et panier 25€ :
→ 1,25€ × 3,0 = 3,75€ revenus/pub
→ 3,75€ ÷ 25€ = 0,15 conversion/jour/pub
→ 1 conversion/semaine/pub

Insuffisant pour Learning Phase Meta (besoin 3-5 conversions/semaine/pub minimum)
```

**Apprentissage** :
- **Règle : Minimum 3-5€/jour/pub** pour que Meta puisse apprendre efficacement
- Avec budget limité, nombre optimal pubs = Budget total ÷ 3€
- Exemple : 10€/jour → maximum 2-3 pubs
- Exemple : 20€/jour → maximum 4-7 pubs
- Exemple : 50€/jour → 10-15 pubs (sweet spot Advantage+)

**Table de référence Budget / Nombre de pubs optimal** :

| Budget/jour | Nb pubs optimal | €/pub/jour | Learning Phase | Performance ASC |
|:-----------|:---------------|:-----------|:---------------|:----------------|
| 10€        | 2-3            | 3-5€       | 7-10j ✅       | 70% potentiel   |
| 10€        | 8              | 1,25€      | 14-21j ❌      | 40% potentiel   |
| 15€        | 3-4            | 4-5€       | 7-10j ✅       | 80% potentiel   |
| 20€        | 4-5            | 4-5€       | 7-10j ✅       | 90% potentiel   |
| 30€        | 5-8            | 4-6€       | 7-10j ✅       | 100% potentiel  |
| 50€        | 8-12           | 4-6€       | 7-10j ✅       | 100% potentiel  |

**Action corrective** : Sprint 1 Mulebar finalisé avec 2 pubs seulement (budget 5€/pub), permettant Learning Phase normale et performances stables.

---

### 2. Audiences Custom Inutiles pour Petits Volumes de Trafic (26 mars 2026 - Cas Mulebar)

**Contexte** : Création audiences retargeting/exclusion pour Mulebar (~5k visiteurs/mois).

**Erreur initiale** : Création 5 audiences custom + exclusion "Acheteurs 180j" dans adset Advantage+ Broad (portée 50M).

**Problème identifié** :
```
Impact réel exclusion :
→ 200 personnes exclues sur 50 000 000 de portée
→ 200 ÷ 50 000 000 = 0,0004%
→ Impact = ZÉRO

Temps perdu : 2h création/config pour 0% impact
```

**Apprentissage** :
- **Audiences custom pertinentes uniquement si volume >10 000 personnes**
- Avec Advantage+ Broad, Meta gère automatiquement retargeting + prospection
- Exclusions <1% audience totale = inutiles
- Pour petits comptes (<10k visiteurs/mois) : **Advantage+ automatique sans audiences custom**

**Seuil de pertinence audiences custom** :

| Trafic site/mois | Taille audiences | Action recommandée |
|:----------------|:----------------|:-------------------|
| <5k             | <500            | Advantage+ auto uniquement |
| 5-10k           | 500-1 000       | ASC auto + test manuel optionnel |
| 10-50k          | 1k-5k           | Custom audiences campagnes manuelles |
| >50k            | >5k             | Segmentation fine + exclusions |

---

### 3. Danger de l'Oscillation Stratégique (26 mars 2026 - Autocritique)

**Erreur commise** : Oscillations multiples sur décisions stratégiques (budget 7€ vs 10€, 2 pubs vs 8 pubs) en réaction aux questions client au lieu de position ferme basée calculs.

**Apprentissage** :
- **Toujours calculer budget minimum par pub AVANT recommander nombre créatives**
- **Toujours vérifier taille audiences vs portée AVANT recommander exclusions**
- Best practices théoriques doivent être **adaptées au contexte** (budget, trafic, maturité)

**Protocole d'expertise corrigé** :
1. Collecter données (budget, trafic, ROAS, panier)
2. Calculer contraintes (conversions nécessaires, budget min/pub, taille audiences)
3. Recommander config basée calculs
4. Si objection : recalculer pour valider/invalider, ne pas pivoter aveuglément

**Leçon** : "Configuration théoriquement 'pro' mais inadaptée < Configuration simple adaptée au contexte". Pragmatisme > Complexité.

## Références

1. Anchour. (2025, November 5). *Meta Ads in 2026: New Algorithm, Creative Strategy & Guide*. Consulté le 12 mars 2026, à l'adresse https://www.anchour.com/articles/meta-ads-2026-playbook/
