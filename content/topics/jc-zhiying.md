---
slug: jc-zhiying
title: 挣值管理 EVM 偏差与预测
date: 2026-10-31
tags: [成本管理, 挣值管理, EVM, PV/EV/AC, 偏差分析]
summary: PV/EV/AC 三值、偏差 CV/SV 与指数 CPI/SPI、EAC/ETC/VAC 三种预测情形与完整例题。
cover:
parent: jindu-chengben
---

## 一、概念与定位

挣值管理（EVM）把范围、进度、成本集成度量，用同一货币单位衡量项目绩效。它回答"到目前为止，花了多少钱、干了多少活、按计划该干多少"，是下午案例与计算必考。

## 二、核心公式

三值：
- \(PV = BAC \times 计划完成\%\)
- \(EV = BAC \times 实际完成\%\)
- \(AC\) = 实际花费

偏差与指数：
- \(SV = EV - PV\)，\(SPI = EV / PV\)（看进度）
- \(CV = EV - AC\)，\(CPI = EV / AC\)（看成本）

判断：SV>0/SPI>1 进度领先；CV>0/CPI>1 成本节约；反之为落后/超支。

完工预测：
\[EAC = \frac{BAC}{CPI}\]（典型偏差持续）
\[EAC = AC + (BAC - EV)\]（非典型，未来按预算）
\[EAC = AC + \frac{BAC - EV}{CPI \times SPI}\]（同时超支且滞后）
\[ETC = EAC - AC,\quad VAC = BAC - EAC\]

## 三、例题（完整三情形）

某项目 \(BAC = 100\) 万元。第 10 天：计划完成 60%，实际完成 50%，\(AC = 60\) 万元。

**步骤 1：三值**
- \(PV = 100 \times 60\% = 60\)
- \(EV = 100 \times 50\% = 50\)
- \(AC = 60\)

**步骤 2：偏差与指数**
- \(CV = 50 - 60 = -10\)（超支）
- \(SV = 50 - 60 = -10\)（落后）
- \(CPI = 50/60 = 5/6 \approx 0.833\)
- \(SPI = 50/60 \approx 0.833\)

**步骤 3：三种 EAC**

典型（CPI 持续）：
\[EAC = \frac{100}{5/6} = 120,\quad ETC = 120 - 60 = 60,\quad VAC = 100 - 120 = -20\]

非典型（剩余按预算）：
\[EAC = 60 + (100 - 50) = 110,\quad ETC = 110 - 60 = 50,\quad VAC = 100 - 110 = -10\]

综合（既超支又滞后）：
\[EAC = 60 + \frac{50}{(5/6)\times(5/6)} = 60 + \frac{50}{25/36} = 60 + 72 = 132\]
\[ETC = 132 - 60 = 72,\quad VAC = 100 - 132 = -32\]

**状态结论**：CPI、SPI 均 <1 → **成本超支且进度落后**；三种预测均显示 VAC<0（预计超预算），综合情形最悲观（132 万）。

## 四、易错点

- 先算 PV/EV/AC 三值，再套偏差与指数；别颠倒分子分母。
- CV/CPI 管成本，SV/SPI 管进度，不可串。
- "ETC 按当前绩效"用 \((BAC-EV)/CPI\)，区别于非典型的 \((BAC-EV)\)。

## 五、真题自测

**题1**：CPI<1 表示？A. 成本节约  B. 成本超支  C. 进度领先  D. 进度落后
**答案**：B。

**题2**：典型偏差下 EAC 公式是？A. AC+(BAC-EV)  B. BAC/CPI  C. AC+(BAC-EV)/(CPI·SPI)  D. BAC-AC
**答案**：B。

- [ ] PV/EV/AC 计算
- [ ] CV/SV/CPI/SPI 符号与含义
- [ ] EAC 三种情形公式
- [ ] ETC 与 VAC
