<!-- ELUCENIA technical documentation · decaimento-radioativo · es · no clinical/professional/rights approval -->

# Desintegración radiactiva

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/decaimento-radioativo)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Radionúclido

`iso`

- `tc99m` — Tecnecio-99m (6,01 h)
- `f18` — Flúor-18 (109,7 min)
- `i131` — Yodo-131 (8,02 días)
- `i123` — Yodo-123 (13,2 h)
- `ga68` — Galio-68 (67,8 min)
- `lu177` — Lutecio-177 (6,64 días)

### Actividad inicial (MBq o mCi)

`a0`

MBq/mCi · intervalo: 0,001–100000

### Tiempo transcurrido

`t`

intervalo: 0–100000

### Unidad de tiempo

`tu`

- `min` — minutos
- `h` — horas
- `d` — días

## Edición del método

Decaimiento físico exponencial; seis semividas NUBASE2020 comparadas y redondeadas; 68Ga 67,8 min; 177Lu 6,64 días; actividad en la unidad original.

## Fórmula documentada

A = A0 × e−λt, con λ = ln 2 ÷ T½; equivalente a A = A0 × (1/2)t ÷ T½.

El resultado usa la unidad inicial (1 mCi = 37 MBq). Semividas físicas NUBASE2020 redondeadas.

## Límites y población

Este modelo calcula únicamente el decaimiento físico exponencial de un radionúclido, con actividad inicial y final en la misma unidad y tiempo compatible con la semivida. No incluye eliminación biológica, semivida efectiva, formación a partir de radionúclidos progenitores ni dosis absorbida. Los seis valores predefinidos se compararon con las entradas correspondientes de NUBASE2020 y se redondearon: 99mTc 6,01 h; 18F 109,7 min; 131I 8,02 días; 123I 13,2 h; 68Ga 67,8 min; 177Lu 6,64 días. Identifique el estado nuclear. El redondeo de los valores predefinidos no incorpora las incertidumbres de la evaluación ni certifica datos metrológicos o dosimetría del paciente.

## Referencias

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

50,0% de la actividad inicial después de 1,00 vida(s) media(s)

| Detalles del resultado | |
| --- | --- |
| Vida media física utilizada | 6,01 h |
| Constante de desintegración (λ) | 0,1153 por hora |
| Tiempo transcurrido | 6,01 h |


### 2

25,0% de la actividad inicial después de 2,00 vida(s) media(s)

| Detalles del resultado | |
| --- | --- |
| Vida media física utilizada | 109,7 min |
| Constante de desintegración (λ) | 0,3791 por hora |
| Tiempo transcurrido | 3,66 h |


### 3

12,5% de la actividad inicial después de 3,00 vida(s) media(s)

| Detalles del resultado | |
| --- | --- |
| Vida media física utilizada | 8,02 días |
| Constante de desintegración (λ) | 0,0036 por hora |
| Tiempo transcurrido | 577,44 h |


### 4

73,6% de la actividad inicial después de 0,44 vida(s) media(s)

| Detalles del resultado | |
| --- | --- |
| Vida media física utilizada | 67,8 min |
| Constante de desintegración (λ) | 0,6134 por hora |
| Tiempo transcurrido | 0,50 h |

