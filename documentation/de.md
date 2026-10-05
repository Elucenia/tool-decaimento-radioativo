<!-- ELUCENIA technical documentation · decaimento-radioativo · de · no clinical/professional/rights approval -->

# Radioaktiver Zerfall

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/decaimento-radioativo)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Radionuklid

`iso`

- `tc99m` — Technetium-99m (6,01 h)
- `f18` — Fluor-18 (109,7 min)
- `i131` — Iod-131 (8,02 Tage)
- `i123` — Iod-123 (13,2 h)
- `ga68` — Gallium-68 (67,8 min)
- `lu177` — Lutetium-177 (6,64 Tage)

### Anfangsaktivität (MBq oder mCi)

`a0`

MBq/mCi · Bereich: 0,001–100000

### Verstrichene Zeit

`t`

Bereich: 0–100000

### Zeiteinheit

`tu`

- `min` — Minuten
- `h` — Stunden
- `d` — Tage

## Fassung der Methode

Exponentieller physikalischer Zerfall; sechs NUBASE2020-Halbwertszeiten verglichen und gerundet; 68Ga 67,8 min; 177Lu 6,64 Tage; Aktivität in der ursprünglichen Einheit.

## Dokumentierte Formel

A = A0 × e−λt, mit λ = ln 2 ÷ T½; gleichbedeutend mit A = A0 × (1/2)t ÷ T½.

Das Ergebnis bleibt in der Anfangseinheit (1 mCi = 37 MBq). Gerundete physikalische Halbwertszeiten aus NUBASE2020.

## Grenzen und Population

Dieses Modell berechnet nur den exponentiellen physikalischen Zerfall eines Radionuklids, mit Anfangs- und Endaktivität in derselben Einheit und zur Halbwertszeit passenden Zeiteinheiten. Es umfasst weder biologische Ausscheidung noch effektive Halbwertszeit, Bildung aus Mutterradionukliden oder absorbierte Dosis. Die sechs Vorgaben wurden mit den entsprechenden NUBASE2020-Einträgen verglichen und gerundet: 99mTc 6,01 h; 18F 109,7 min; 131I 8,02 Tage; 123I 13,2 h; 68Ga 67,8 min; 177Lu 6,64 Tage. Geben Sie den Kernzustand an. Die Rundung der Vorgaben berücksichtigt nicht die Unsicherheiten der Bewertung und zertifiziert weder metrologische Daten noch patientenbezogene Dosimetrie.

## Referenzen

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026
