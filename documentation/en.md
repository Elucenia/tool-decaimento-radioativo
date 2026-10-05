<!-- ELUCENIA technical documentation · decaimento-radioativo · en · no clinical/professional/rights approval -->

# Radioactive decay

[conditions, sources and permissions](https://elucenia.org/en/tools/decaimento-radioativo)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Radionuclide

`iso`

- `tc99m` — Technetium-99m (6.01 h)
- `f18` — Fluorine-18 (109.7 min)
- `i131` — Iodine-131 (8.02 days)
- `i123` — Iodine-123 (13.2 h)
- `ga68` — Gallium-68 (67.8 min)
- `lu177` — Lutetium-177 (6.64 days)

### Initial activity (MBq or mCi)

`a0`

MBq/mCi · range: 0.001–100000

### Elapsed time

`t`

range: 0–100000

### Time unit

`tu`

- `min` — minutes
- `h` — hours
- `d` — days

## Method edition

Exponential physical decay; six NUBASE2020 half-lives compared and rounded; 68Ga 67.8 min; 177Lu 6.64 days; activity in the original unit.

## Documented formula

A = A0 × e−λt, with λ = ln 2 ÷ T½; equivalent to A = A0 × (1/2)t ÷ T½.

The result uses the initial activity unit (1 mCi = 37 MBq). Rounded physical half-lives from NUBASE2020.

## Limits and population

This model calculates only the exponential physical decay of a single radionuclide, with initial and final activity in the same unit and time consistent with the half-life. It does not include biological elimination, effective half-life, ingrowth from parent radionuclides or absorbed dose. The six presets were compared with the corresponding NUBASE2020 entries and rounded: 99mTc 6.01 h; 18F 109.7 min; 131I 8.02 days; 123I 13.2 h; 68Ga 67.8 min; 177Lu 6.64 days. Identify the nuclear state. Preset rounding does not incorporate the evaluation’s uncertainties and does not certify metrological data or patient dosimetry.

## References

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
