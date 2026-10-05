<!-- ELUCENIA technical documentation · decaimento-radioativo · ja · no clinical/professional/rights approval -->

# 放射性崩壊

[条件・出典・許諾](https://elucenia.org/ja/tools/decaimento-radioativo)

## 使い方

ポータルでツールを使用するか、ローカルHTTPサーバー経由でindex.htmlを開いてください。言語を選択し、項目を入力して計算してください。

## 入力項目と単位

### 放射性核種

`iso`

- `tc99m` — テクネチウム-99m（6.01 h）
- `f18` — フッ素-18（109.7 min）
- `i131` — ヨウ素-131（8.02日）
- `i123` — ヨウ素-123（13.2 h）
- `ga68` — ガリウム-68（67.8 min）
- `lu177` — ルテチウム-177（6.64日）

### 初期放射能（MBqまたはmCi）

`a0`

MBq/mCi · 範囲: 0.001–100000

### 経過時間

`t`

範囲: 0–100000

### 時間の単位

`tu`

- `min` — 分
- `h` — 時間
- `d` — 日

## 方法の版

指数関数的な物理的減衰。NUBASE2020の六つの半減期を比較し丸めた値：68Ga 67.8 min、177Lu 6.64日。放射能は元の単位。

## 記載された計算式

A = A0 × e−λt、ここでλ = ln 2 ÷ T½；同じく A = A0 × (1/2)t ÷ T½.

結果は初期放射能と同じ単位（1 mCi = 37 MBq）。NUBASE2020の物理的半減期を丸めて使用します。

## 限界・対象集団

このモデルは単一放射性核種の指数関数的な物理的減衰のみを計算します。初期・最終放射能は同じ単位、時間は半減期と整合する単位を用いてください。生物学的排泄、実効半減期、親核種からの生成、吸収線量は含みません。六つの既定値をNUBASE2020の対応する項目と比較し、丸めています：99mTc 6.01 h、18F 109.7 min、131I 8.02日、123I 13.2 h、68Ga 67.8 min、177Lu 6.64日。核状態を指定してください。既定値の丸めには評価の不確かさは含まれず、計量データや患者の線量評価を認証するものではありません。

## 参考文献

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## 技術テストの再現

このリポジトリのルートディレクトリでnode test.cjsを実行すると、記録された合成ケースを再実行できます。元の入力、期待結果、許容誤差は保持されています。技術テストは臨床的検証を意味しません。

```sh
node test.cjs
```

tool.jsonには出典、版、確認範囲が記録されています。examples.jsonには合成入力と期待結果が保持され、results.jsonには実際に得られた結果が記録されています。

[記録・参考文献](../tool.json) · [JavaScriptコード](../calculator.js) · [参照ケース](../examples.json) · [results.json](../results.json)

## 確認状況と使用条件

独立した臨床レビューは実施されていません。

このインターフェースは独自に作成した翻訳であり、公式版や認証済みの版ではありません。独立した臨床レビュー、専門家による言語レビュー、評価尺度等の権利許諾の確認は実施されていません。

式または分類の結果です。解釈、対応、適用可能性は専門家による評価と選択した出典に依存します。

## ライセンスと帰属表示

Apache-2.0はELUCENIAのコードにのみ適用されます。評価尺度等、出版物、翻訳、データの権利は、それぞれの権利者に帰属します。LICENSEとNOTICEを保持してください。

ELUCENIA · Felipe Guedes · Copyright © 2026
