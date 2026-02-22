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

| Classe d'actifs (5) | Hypothèse 2026 | Lien direct avec bloc 1 + probas |
| --- | --- | --- |
| Actions US (SPX) | +8-12 % prix, BPA +5-8 %, PER stable ~20x | Reprise confirmée par blend <25 % ; croissance bénéficiaire soutenue par la consommation et le capex. |
| Actions Europe (SX5E) | +6-10 % prix, rattrapage de valorisation | Europe bénéficie du cycle global, valorisations attractives (PER <14x) ; soutien budgétaire UE. |
| Taux US 10 ans | Stable autour de **4,0-4,3 %** fin 2026 | Fed prudente, pas de rally obligataire ; portage correct mais gains en capital limités. |
| Taux EUR core (Bund/OAT 10 ans) | Bund vers **2,3 %**, OAT vers **2,9 %** | BCE baisse graduellement ; spread OAT stable, pas de stress budgétaire. |
| Cash EUR (ESTRON) | Rendement glisse de 3,0 % à 2,5 % | Portage encore correct mais en érosion progressive ; moindre intérêt si les actifs risqués performent. |

## Bloc 3 – Allocation stratégique 2026 (8 lignes, ref 12,5 % chacune)

Référence : benchmark égal-pondéré 8 lignes × 12,5 %. En phase de reprise modérée, on **surpondère les actions** (moteur de performance via croissance bénéficiaire) et on maintient une **exposition obligataire neutre** (portage mais sans rally massif). Le cash est réduit car le coût d'opportunité augmente en reprise.

**Achats / ventes vs benchmark (Δ en points de %)**
- Actions renforcées : SPX +7,5 ; SX5E +5,5.
- Duration longue neutre à légèrement sous-pondérée : US10 -2,5 ; Bund10 -1,0 ; OAT10 +1,5.
- Courts maintenus pour le portage : US2 +1,0 ; Bund2 -3,0.
- Cash ESTRON -9,0 (réduit fortement, coût d'opportunité en reprise).

| Ligne (indice) | Poids final | Δ vs 12,5 % | Rationale (reprise modérée 2026) |
| --- | --- | --- | --- |
| Actions US (SPX) | **20 %** | +7,5 | Surpondération : BPA en hausse, consommation résiliente, tech & services porteurs ; principal moteur de performance. |
| Actions Europe (SX5E) | **18 %** | +5,5 | Surpondération : valorisations attractives, rattrapage du cycle, soutien budgétaire UE et reprise industrielle. |
| US Treasuries 10Y (USGG10) | **10 %** | -2,5 | Sous-pondération modérée : portage correct mais gains en capital limités si la Fed reste prudente. |
| US Treasuries 2Y (USGG2) | **13,5 %** | +1,0 | Légère surpondération : portage attractif à ~4 %, faible duration = protection si taux remontent. |
| Bund 10Y (GDBR10) | **11,5 %** | -1,0 | Légère sous-pondération : détente BCE limitée, portage moyen ; on préfère le carry court. |
| Bund 2Y (GDBR2) | **9,5 %** | -3,0 | Sous-pondération : portage EUR court moins attractif que US2 ; BCE plus lente que Fed. |
| OAT 10Y (GFRN10) | **14 %** | +1,5 | Légère surpondération : spread vs Bund offre du carry supplémentaire, risque souverain contenu. |
| Marché monétaire EUR (ESTRON) | **3,5 %** | -9,0 | Fortement réduit : coût d'opportunité élevé en reprise ; on garde un minimum pour la liquidité. |

Total = 100 %. Lecture : portefeuille **orienté croissance**, performance attendue principalement des actions (US et EU). Obligations en portage neutre sans pari directionnel fort. Cash minimal car la reprise rend l'attentisme coûteux.

**Pourquoi cette exposition globale ?**
Nous anticipons une reprise modérée confirmée par le modèle (blend ~15-25 %, phase « reprise ») : la source principale de performance est la croissance bénéficiaire des actions, accompagnée d'un portage obligataire correct. Les actions sont surpondérées car les fondamentaux s'améliorent sans surchauffe (ISM 52, pas 60+). La duration longue est neutre car la Fed ne coupe pas agressivement en reprise. Le cash est réduit au minimum de liquidité.

**Cadre temporel**
Allocation décidée **début 2026** en vue de la trajectoire projetée **fin 2026** : on se positionne tôt sur les actions pour capter la revalorisation progressive, on maintient du portage obligataire, et on conserve la flexibilité de pivoter vers la duration si le cycle se dégrade.

### Risques clés
1. **Rechute en récession** (choc exogène, crise géopolitique, resserrement du crédit) → surpondération actions coûteuse, nécessité de pivoter vers la duration longue.
2. **Inflation ré-accélère** (chocs énergie, salaires) → Fed relève les taux, pénalise à la fois actions et obligations ; nécessité de renforcer le cash.
3. **Surchauffe / boom** (croissance plus forte que prévu, ISM >57) → bascule vers un régime boom, risque de bulle ; opportunité de surfer mais nécessité de surveiller les excès de valorisation.
4. **Stagnation prolongée** (reprise sans conviction, ISM reste ~50) → actions déçoivent, portage obligataire devient la seule source de performance.
