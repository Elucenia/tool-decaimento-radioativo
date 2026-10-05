<!-- ELUCENIA technical documentation · decaimento-radioativo · pt-BR · no clinical/professional/rights approval -->

# Decaimento radioativo

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/decaimento-radioativo)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Radionuclídeo

`iso`

- `tc99m` — Tecnécio-99m (6,01 h)
- `f18` — Flúor-18 (109,7 min)
- `i131` — Iodo-131 (8,02 dias)
- `i123` — Iodo-123 (13,2 h)
- `ga68` — Gálio-68 (67,8 min)
- `lu177` — Lutécio-177 (6,64 dias)

### Atividade inicial (MBq ou mCi)

`a0`

MBq/mCi · intervalo: 0,001–100000

### Tempo decorrido

`t`

intervalo: 0–100000

### Unidade do tempo

`tu`

- `min` — minutos
- `h` — horas
- `d` — dias

## Edição do método

Decaimento físico exponencial; seis meias-vidas NUBASE2020 comparadas e arredondadas; 68Ga 67,8 min; 177Lu 6,64 dias; atividade na unidade original.

## Fórmula documentada

A = A0 × e−λt, com λ = ln 2 ÷ T½; o mesmo que A = A0 × (1/2)t ÷ T½.

O resultado sai na mesma unidade da atividade inicial (1 mCi = 37 MBq). Meias-vidas físicas da avaliação NUBASE2020, arredondadas.

## Limites e população

Este modelo calcula apenas decaimento físico exponencial de um radionuclídeo, com atividade inicial e final na mesma unidade e tempo compatível com a meia-vida. Não inclui eliminação biológica, meia-vida efetiva, formação por radionuclídeos pais nem dose absorvida. Os seis presets foram comparados às entradas correspondentes da NUBASE2020 e arredondados: 99mTc 6,01 h; 18F 109,7 min; 131I 8,02 dias; 123I 13,2 h; 68Ga 67,8 min; 177Lu 6,64 dias. Identifique o estado nuclear. O arredondamento dos presets não incorpora as incertezas da avaliação e não certifica dados metrológicos nem dosimetria do paciente.

## Referências

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
