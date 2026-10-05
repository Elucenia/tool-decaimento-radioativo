<!-- ELUCENIA technical documentation · decaimento-radioativo · fr · no clinical/professional/rights approval -->

# Décroissance radioactive

[conditions, sources et autorisations](https://elucenia.org/fr/outils/decaimento-radioativo)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Radionucléide

`iso`

- `tc99m` — Technétium-99m (6,01 h)
- `f18` — Fluor-18 (109,7 min)
- `i131` — Iode-131 (8,02 jours)
- `i123` — Iode-123 (13,2 h)
- `ga68` — Gallium-68 (67,8 min)
- `lu177` — Lutétium-177 (6,64 jours)

### Activité initiale (MBq ou mCi)

`a0`

MBq/mCi · intervalle: 0,001–100000

### Temps écoulé

`t`

intervalle: 0–100000

### Unité de temps

`tu`

- `min` — minutes
- `h` — heures
- `d` — jours

## Édition de la méthode

Décroissance physique exponentielle ; six périodes radioactives NUBASE2020 comparées et arrondies ; 68Ga 67,8 min ; 177Lu 6,64 jours ; activité dans l’unité originale.

## Formule documentée

A = A0 × e−λt, avec λ = ln 2 ÷ T½ ; équivalent à A = A0 × (1/2)t ÷ T½.

Le résultat conserve l’unité initiale (1 mCi = 37 MBq). Demi-vies physiques NUBASE2020 arrondies.

## Limites et population

Ce modèle calcule uniquement la décroissance physique exponentielle d’un radionucléide, avec les activités initiale et finale dans la même unité et un temps compatible avec la période radioactive. Il n’inclut ni élimination biologique, ni période effective, ni production par des radionucléides parents, ni dose absorbée. Les six valeurs prédéfinies ont été comparées aux entrées correspondantes de NUBASE2020 et arrondies : 99mTc 6,01 h ; 18F 109,7 min ; 131I 8,02 jours ; 123I 13,2 h ; 68Ga 67,8 min ; 177Lu 6,64 jours. Identifiez l’état nucléaire. L’arrondi des valeurs prédéfinies n’intègre pas les incertitudes de l’évaluation et ne certifie ni les données métrologiques ni la dosimétrie du patient.

## Références

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
