# Protocole de Scaling Meta Ads

## Principes Fondamentaux du Scaling

Le scaling d'un compte Meta Ads est un processus méthodique qui consiste à augmenter progressivement l'investissement publicitaire tout en maintenant un niveau de rentabilité acceptable. Il ne s'agit pas simplement d'augmenter le budget : le scaling implique une compréhension fine des mécaniques de l'algorithme Meta, une structure de compte adaptée, et une discipline opérationnelle rigoureuse.

Le scaling repose sur un principe central : **l'algorithme Meta optimise pour le coût marginal, pas pour le coût moyen**. Cela signifie que lorsqu'on augmente le budget, le système cherche les conversions suivantes les moins chères disponibles dans l'audience. Plus on augmente le budget, plus on s'éloigne du "noyau dur" d'utilisateurs les plus susceptibles de convertir, et plus le coût marginal augmente. C'est pourquoi une augmentation brutale de budget provoque presque toujours une hausse du CPA.

---

## La Règle des 20%

La règle fondamentale du scaling Meta Ads est la suivante : **ne jamais augmenter le budget de plus de 20% en une seule fois**, et attendre **3 à 4 jours** entre chaque augmentation pour permettre à l'algorithme de se recalibrer.

### Pourquoi 20% ?

Une augmentation de 20% est suffisamment significative pour générer un impact mesurable sur le volume de conversions, tout en restant dans la zone de confort de l'algorithme. Au-delà de 20%, l'adset risque de réentrer en phase d'apprentissage (Learning Phase), ce qui provoque une instabilité de performance pendant 7 jours.

### Pourquoi 3-4 jours ?

L'algorithme Meta a besoin de temps pour explorer de nouveaux segments d'audience et recalibrer ses enchères. Trois à quatre jours représentent le minimum nécessaire pour obtenir des données statistiquement significatives sur le nouveau palier de budget.

### Tableau de Progression

| Jour | Budget | Variation | Action |
|:---|:---|:---|:---|
| J0 | 100 €/jour | Baseline | Démarrage |
| J4 | 120 €/jour | +20% | Si ROAS > seuil |
| J8 | 144 €/jour | +20% | Si ROAS > seuil |
| J12 | 173 €/jour | +20% | Si ROAS > seuil |
| J16 | 207 €/jour | +20% | Si ROAS > seuil |
| J20 | 249 €/jour | +20% | Si ROAS > seuil |
| J24 | 299 €/jour | +20% | Si ROAS > seuil |
| J28 | 358 €/jour | +20% | Si ROAS > seuil |

En suivant ce rythme, un budget de 100€/jour peut atteindre ~360€/jour en un mois, soit une multiplication par 3.6x.

---

## Seuils de Rentabilité (Go / No-Go)

Avant chaque augmentation de budget, vérifier les seuils suivants :

### Seuil ROAS

| Situation | Seuil Minimum | Action |
|:---|:---|:---|
| ROAS > objectif × 1.2 | ✅ Scaler | Augmenter de 20% |
| ROAS entre objectif et objectif × 1.2 | ⚠️ Maintenir | Garder le budget actuel |
| ROAS < objectif | 🔴 Réduire ou pause | Revenir au palier précédent |

Le seuil ROAS objectif dépend de la marge brute du produit. Pour un e-commerce avec 60% de marge brute, un ROAS de 3x est le breakeven. Un ROAS objectif de 5x laisse une marge confortable pour scaler.

### Seuil CPA

Le CPA maximum acceptable se calcule ainsi :

> **CPA Max = Panier Moyen × Marge Brute × (1 - Marge Nette Cible)**

Par exemple, pour un panier moyen de 40€, une marge brute de 60%, et une marge nette cible de 15% :
CPA Max = 40 × 0.60 × (1 - 0.15) = 20.40€

### Seuil de Volume

Un adset doit générer au minimum **50 événements d'optimisation par semaine** pour sortir du Learning Limited. Si le budget est insuffisant pour atteindre ce seuil, la consolidation est nécessaire avant le scaling.

---

## Scaling Vertical vs Horizontal

### Scaling Vertical (Augmenter le Budget)

Le scaling vertical consiste à augmenter le budget sur les campagnes/adsets existants. C'est la méthode la plus simple et la plus recommandée en 2026 grâce à Andromeda.

**Avantages :** Simple à exécuter, préserve les données historiques de l'adset, l'algorithme conserve ses apprentissages.

**Limites :** Le CPA augmente progressivement (rendements décroissants), risque de saturation d'audience (fréquence élevée), plafond naturel lié à la taille de l'audience.

### Scaling Horizontal (Diversifier les Créatives)

En 2026, le scaling horizontal ne se fait plus via la multiplication des adsets (qui crée de la fragmentation et du chevauchement d'enchères), mais via la **diversification créative**. Chaque nouvelle créative avec un Entity ID distinct donne à Andromeda un nouveau "ticket" pour accéder à de nouvelles audiences.

**Avantages :** Accès à de nouvelles audiences via Andromeda, réduit la fatigue créative, permet de tester de nouveaux angles.

**Limites :** Nécessite une production créative soutenue, chaque créative n'est pas garantie de performer.

### Recommandation 2026

Privilégier le **scaling vertical** avec une structure consolidée (1-2 campagnes CBO, 2 adsets max). Le scaling horizontal se fait principalement via la **diversification créative** (nouveaux Entity IDs pour Andromeda), pas via la multiplication des adsets.

---

## Structure de Compte pour le Scaling

### Structure Evergreen (Always-On)

```
Campagne: [Marque] - Evergreen - CBO
  Budget: [Budget quotidien baseline]
  Stratégie d'enchère: Lowest Cost
  
  Adset 1: Retargeting 360
    Audience: TOUTES les audiences chaudes fusionnées
              (visiteurs site 30j, liste clients, abandons panier, ouvreurs email)
    Budget: Géré par CBO
    
  Adset 2: Prospection Broad
    Audience: Aucun intérêt, aucune LAL
              Pays: France (ou marché cible)
              Âge: 18-65+
    Budget: Géré par CBO
```

### Structure Booster (Pendant les Campagnes Email)

Même structure, budget augmenté de +50% à +100% pendant la durée de la campagne email.

### Pourquoi CBO ?

Le Campaign Budget Optimization (CBO) est essentiel pour le scaling car il permet à l'algorithme de répartir dynamiquement le budget entre les adsets en fonction de leur performance en temps réel. Sans CBO, le budget est figé par adset, ce qui empêche l'optimisation automatique.

---

## Le Booster Switch (Scaling Omnicanal)

Le Booster Switch est un protocole de scaling synchronisé avec les campagnes emailing. Il exploite l'effet de halo créé par les emails pour maximiser le ROAS Meta pendant les périodes de forte demande.

### Protocole Détaillé

| Phase | Timing | Budget Meta | Action |
|:---|:---|:---|:---|
| **Pré-campagne** | J-1 | +50% | Augmenter le budget 24h avant l'envoi email |
| **Campagne active** | J0 à J+N | +50% à +100% | Maintenir le budget élevé |
| **Post-campagne** | J+N+1 à J+N+3 | +50% | Réduire progressivement |
| **Retour baseline** | J+N+4 | Baseline | Revenir au budget normal |

### Pourquoi ça Fonctionne

Pendant les campagnes emailing, les audiences de retargeting grossissent (plus de visiteurs sur le site), la notoriété de marque augmente (les utilisateurs reconnaissent la marque dans les pubs), le taux de conversion augmente (les utilisateurs sont "pré-chauffés" par l'email), et le ROAS Meta augmente mécaniquement (+50% à +100% observé).

---

## Scaling Milestones et ROAS Attendu

| Palier Budget | ROAS Attendu | Risque Principal |
|:---|:---|:---|
| 50-100 €/jour | 8-12 | Learning Limited |
| 100-200 €/jour | 7-10 | Instabilité de transition |
| 200-500 €/jour | 6-9 | Début de saturation audience |
| 500-1000 €/jour | 5-8 | Broad targeting essentiel |
| 1000+ €/jour | 4-7 | Rafraîchissement créatif critique |

Le ROAS diminue naturellement avec l'augmentation du budget. C'est attendu et acceptable tant que le **profit absolu** augmente.

---

## Calendrier de Rafraîchissement Créatif

La fatigue créative s'accélère avec des budgets plus élevés (plus d'impressions par jour) :

| Budget Quotidien | Fréquence de Rafraîchissement |
|:---|:---|
| <100 €/jour | Toutes les 4-6 semaines |
| 100-300 €/jour | Toutes les 2-4 semaines |
| 300-1000 €/jour | Toutes les 1-2 semaines |
| 1000+ €/jour | Hebdomadaire |

**Règle de rafraîchissement :** Ajouter de nouvelles créatives aux adsets existants. Ne PAS créer de nouveaux adsets pour de nouvelles créatives (évite la réinitialisation du Learning Phase).

---

## Test A/B Avant Restructuration

Avant de changer la structure entière du compte, exécuter un test A/B contrôlé :

**Setup :**
- Campagne A (Contrôle) : Meilleure campagne existante, 50% du budget total
- Campagne B (Challenger) : Nouvelle structure (CBO, 2 adsets), 50% du budget total
- Durée : Minimum 14 jours (2 cycles complets de Learning Phase)
- Métrique d'évaluation : ROAS sur la période complète de 14 jours

**Règle de décision :**
- ROAS B > ROAS A de >10% : Migrer entièrement vers B
- ROAS B dans les 10% de A : Continuer le test 7 jours de plus
- ROAS B < ROAS A de >10% : Garder A, diagnostiquer B

---

## Signaux d'Alerte pendant le Scaling

| Signal | Seuil | Action |
|:---|:---|:---|
| Fréquence en hausse | >2.5 (prospection), >4 (retargeting) | Rafraîchir les créatives |
| CPM en hausse constante | +20% sur 7 jours | Élargir l'audience ou réduire le budget |
| CTR en baisse | -30% sur 7 jours | Fatigue créative, nouvelles créatives nécessaires |
| CPA en hausse | +30% sur 7 jours | Revenir au palier précédent |
| ROAS en baisse | <seuil minimum sur 7 jours | Pause scaling, diagnostic |

### Protocole de Réaction

1. **Ne pas paniquer** : Vérifier d'abord si la baisse est dans la variance normale (±15-20%)
2. **Attendre 7 jours** : Ne jamais réagir à moins de 7 jours de données
3. **Diagnostiquer** : CAPI active ? Créatives fatiguées ? Audience saturée ? Concurrence accrue ?
4. **Agir progressivement** : Revenir au palier précédent, pas couper brutalement
5. **Documenter** : Noter le palier de budget où la performance s'est dégradée

---

## Checklist de Scaling

Avant chaque augmentation de budget :
- [ ] ROAS au-dessus du seuil sur les 7 derniers jours
- [ ] Aucun adset en Learning Limited actif
- [ ] Fréquence créative en dessous du seuil de fatigue
- [ ] CAPI active et EMQ > 7
- [ ] Aucune modification significative dans les 3 derniers jours
- [ ] Aucun événement externe majeur prévu dans les 3 prochains jours

---

## Apprentissages Terrain

*Cette section est mise à jour automatiquement lors des analyses.*

### Mulebar — Mars 2026
- Effet de halo emailing mesuré à +75% de ROAS (8.36 → 14.60)
- Audiences "pépites" (ROAS 14-17) non scalables individuellement (trop petites)
- 8/11 adsets en Learning Limited à cause de la fragmentation
- Le budget n'était pas augmenté pendant les campagnes emailing (opportunité massive ratée)
- Budget quotidien de ~85€/jour avec ROAS 9.79 : potentiel de scaling vertical significatif

---

## Références

- Meta Business Help Center — Campaign Budget Optimization
- Jon Loomer — Meta Advertising Changes 2025
- Smart Marketer — Meta Ads New Operating System 2026
- Logical Position — Paid Social Playbook 2026
- Meta Engineering Blog — Andromeda, GEM, Lattice
