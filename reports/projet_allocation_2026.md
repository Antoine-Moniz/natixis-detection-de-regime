# Projet d'allocation d'actifs – 2026

## Bloc 1 – Scénario économique (choix discrétionnaire)

**Narratif retenu : reprise modérée US en 2026**, sortie progressive du ralentissement 2024-2025, croissance PIB réel ~2 % a/a. L'Europe bénéficie d'un environnement mondial plus porteur (croissance ~1-1,5 %), sans surchauffe ni crise.

- **Chocs appliqués (voir `notebooks/scenario_dashboard.ipynb`, overrides 2026)**
  `us_gdp_qoq 2,0 %`, `ISM 52`, `Michigan 72`, `Initial claims 240k`, `NFP +180k`, `CPI MoM 0,25 %`. Chocs uniquement sur les projections 2026, historique inchangé.
- **Consommateurs** : moral en amélioration (Michigan 72, vs creux ~60 en 2024) mais sans euphorie ; marché du travail résilient (claims 240k, NFP +180k/mois) → consommation en progression modérée, soutien à la croissance.
- **Entreprises** : ISM 52 → retour en légère expansion manufacturière après la contraction de 2024 ; reprise prudente du capex et des embauches, marges stables.
- **Politiques monétaire et budgétaire** : Fed maintient les taux autour de 4,0-4,5 % en 2026, baisses graduelles possibles si l'inflation confirme son recul. BCE suit avec prudence, taux dépôt vers 2,5 %. Pas de stimulus budgétaire massif, stabilisateurs automatiques suffisent.
- **Commerce international** : demande mondiale en amélioration ; dollar stable → export US et EU bénéficient d'un cycle global plus porteur.

## Bloc 2 – Scénario financier et outil quantitatif

### Outil quanti
- Modèle **Markov 4 régimes** sur `us_gdp_qoq` + **Kalman** sur indicateurs avancés (ISM, Michigan, claims, NFP) → probabilité de récession.
- Baseline (nov. 2025) : blend ≈ **11 %** (phase « reprise »).
  Scénario US Recovery 2026 : probabilité de récession reste **basse (~15-25 %)**, phase dominante « **reprise** ». Le modèle capte la normalisation progressive des indicateurs sans basculer en régime boom ni récession.

### Traduction financière du scénario

**Lien direct macro → prix/taux (ce qui sera évalué)**
- PIB +2 % / ISM 52 → croissance bénéficiaire modeste (+5-8 % BPA), multiples actions stables à légèrement en expansion.
- Marché du travail résilient (claims 240k, NFP +180k) → Fed prudente, pas de baisse agressive des taux → courbe des taux stable, légère pentification.
- Inflation maîtrisée (CPI 0,25 % MoM ≈ 3 % annualisé) → pas de resserrement supplémentaire, mais pas de rally obligataire majeur non plus.
- Dollar stable → pas de pénalité de change pour les actifs européens.
- Environnement de carry favorable → taux courts restent rémunérateurs, actions en hausse modérée.

