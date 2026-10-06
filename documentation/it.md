<!-- ELUCENIA technical documentation · decaimento-radioativo · it · no clinical/professional/rights approval -->

# Decadimento radioattivo

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/decaimento-radioativo)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Radionuclide

`iso`

- `tc99m` — Tecnezio-99m (6,01 h)
- `f18` — Fluoro-18 (109,7 min)
- `i131` — Iodio-131 (8,02 giorni)
- `i123` — Iodio-123 (13,2 h)
- `ga68` — Gallio-68 (67,8 min)
- `lu177` — Lutezio-177 (6,64 giorni)

### Attività iniziale (MBq o mCi)

`a0`

MBq/mCi · intervallo: 0,001–100000

### Tempo trascorso

`t`

intervallo: 0–100000

### Unità di tempo

`tu`

- `min` — minuti
- `h` — ore
- `d` — giorni

## Edizione del metodo

Decadimento fisico esponenziale; sei emivite NUBASE2020 confrontate e arrotondate; 68Ga 67,8 min; 177Lu 6,64 giorni; attività nell’unità originale.

## Formula documentata

A = A0 × e−λt, con λ = ln 2 ÷ T½; equivalente a A = A0 × (1/2)t ÷ T½.

Il risultato mantiene l’unità iniziale (1 mCi = 37 MBq). Emivite fisiche NUBASE2020 arrotondate.

## Limiti e popolazione

Questo modello calcola soltanto il decadimento fisico esponenziale di un radionuclide, con attività iniziale e finale nella stessa unità e tempo coerente con l’emivita. Non include eliminazione biologica, emivita effettiva, produzione da radionuclidi progenitori né dose assorbita. I sei valori preimpostati sono stati confrontati con le voci corrispondenti di NUBASE2020 e arrotondati: 99mTc 6,01 h; 18F 109,7 min; 131I 8,02 giorni; 123I 13,2 h; 68Ga 67,8 min; 177Lu 6,64 giorni. Identificare lo stato nucleare. L’arrotondamento dei valori preimpostati non incorpora le incertezze della valutazione e non certifica dati metrologici né la dosimetria del paziente.

## Riferimenti

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Risultati documentati

Le informazioni seguenti conservano gli output del metodo per esempi sintetici. Non costituiscono una validazione clinica indipendente.

### 1

50,0% dell’attività iniziale dopo 1,00 emivita/e

| Dettagli del risultato | |
| --- | --- |
| Emivita fisica utilizzata | 6,01 h |
| Costante di decadimento (λ) | 0,1153 all’ora |
| Tempo trascorso | 6,01 h |


### 2

25,0% dell’attività iniziale dopo 2,00 emivita/e

| Dettagli del risultato | |
| --- | --- |
| Emivita fisica utilizzata | 109,7 min |
| Costante di decadimento (λ) | 0,3791 all’ora |
| Tempo trascorso | 3,66 h |


### 3

12,5% dell’attività iniziale dopo 3,00 emivita/e

| Dettagli del risultato | |
| --- | --- |
| Emivita fisica utilizzata | 8,02 giorni |
| Costante di decadimento (λ) | 0,0036 all’ora |
| Tempo trascorso | 577,44 h |


### 4

73,6% dell’attività iniziale dopo 0,44 emivita/e

| Dettagli del risultato | |
| --- | --- |
| Emivita fisica utilizzata | 67,8 min |
| Costante di decadimento (λ) | 0,6134 all’ora |
| Tempo trascorso | 0,50 h |

