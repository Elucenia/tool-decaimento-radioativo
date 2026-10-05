<!-- ELUCENIA technical documentation · decaimento-radioativo · zh · no clinical/professional/rights approval -->

# 放射性衰变

[条件、来源与许可](https://elucenia.org/zh/tools/decaimento-radioativo)

## 使用方法

在门户中使用工具，或通过本地 HTTP 服务器打开 index.html。选择语言，填写各字段，然后计算。

## 输入与单位

### 放射性核素

`iso`

- `tc99m` — 锝-99m（6.01 h）
- `f18` — 氟-18（109.7 min）
- `i131` — 碘-131（8.02天）
- `i123` — 碘-123（13.2 h）
- `ga68` — 镓-68（67.8 min）
- `lu177` — 镥-177（6.64天）

### 初始活度（MBq 或 mCi）

`a0`

MBq/mCi · 范围: 0.001–100000

### 经过时间

`t`

范围: 0–100000

### 时间单位

`tu`

- `min` — 分钟
- `h` — 小时
- `d` — 天

## 方法版本

指数形式物理衰变；已比较并舍入六个NUBASE2020半衰期；68Ga 67.8 min；177Lu 6.64天；活度保持原单位。

## 已记录的公式

A = A0 × e−λt，其中λ = ln 2 ÷ T½；等价于 A = A0 × (1/2)t ÷ T½.

结果单位与初始活度相同（1 mCi = 37 MBq）。采用NUBASE2020评估的物理半衰期舍入值。

## 限制与适用人群

此模型仅计算单一放射性核素的指数形式物理衰变，初始与最终活度须使用相同单位，时间单位须与半衰期一致。它不包括生物清除、有效半衰期、母核素产生的子核素增长或吸收剂量。六个预设值已与NUBASE2020对应条目比较并舍入：99mTc 6.01 h；18F 109.7 min；131I 8.02天；123I 13.2 h；68Ga 67.8 min；177Lu 6.64天。请注明核状态。预设值的舍入不包含评价中的不确定度，也不认证计量数据或患者剂量学。

## 参考文献

- [Kondev FG et al. The NUBASE2020 evaluation of nuclear physics properties. Chinese Physics C, 2021.](https://doi.org/10.1088/1674-1137/abddae)

- [International Atomic Energy Agency (IAEA). Live Chart of Nuclides.](https://www-nds.iaea.org/relnsd/vcharthtml/VChartHTML.html)

- [IAEA primary glossary,physical/biological/effective half-time](https://www-pub.iaea.org/MTCD/Publications/PDF/IAEA_SI_web.pdf)

- [NUBASE2020,published2021](https://www-nds.iaea.org/amdc/ame2020/NUBASE2020.pdf)

## 复现技术测试

在此仓库的根目录中运行 node test.cjs，以重复已记录的合成案例。原始输入、预期结果和容差保持不变。技术测试不构成临床验证。

```sh
node test.cjs
```

tool.json 包含来源、版本和审查范围。examples.json 保留合成输入与预期结果；results.json 记录实际得到的结果。

[记录与参考文献](../tool.json) · [JavaScript代码](../calculator.js) · [参考案例](../examples.json) · [results.json](../results.json)

## 审查与使用条件

尚未开展独立临床审查。

此界面为自主编写的翻译，并非官方或认证版本。尚未完成独立临床审查、专业语言审查或工具权利授权。

公式或分类结果。解释、处理及适用性须结合专业评估和所选来源。

## 许可与署名

Apache-2.0 仅适用于 ELUCENIA 代码。工具、出版物、翻译和数据的权利仍归各自权利人所有。请保留 LICENSE 和 NOTICE。

ELUCENIA · Felipe Guedes · Copyright © 2026
