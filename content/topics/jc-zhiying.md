---
slug: jc-zhiying
title: 挣值管理 EVM
date: 2026-10-31
tags: [挣值, EVM, EAC, ETC]
summary: PV/EV/AC 三值、偏差 CV/SV 与指数 CPI/SPI、EAC/ETC/VAC 三种预测公式与例题。
cover:
parent: jindu-chengben
---

## 一、三值

- **PV** 计划价值 = 计划应完成工作的预算
- **EV** 挣值 = 实际完成工作的预算 = 预算 × 实际完成%
- **AC** 实际成本 = 实际已花费

## 二、偏差与指数

- SV = EV − PV ；SPI = EV / PV（看进度）
- CV = EV − AC ；CPI = EV / AC（看成本）
- SV>0/SPI>1 领先；CV>0/CPI>1 节约；反之为落后/超支。

## 三、完工预测

- 典型偏差持续：`EAC = BAC / CPI`
- 非典型（未来按预算）：`EAC = AC + (BAC − EV)`
- 同时超支且滞后：`EAC = AC + (BAC − EV) / (CPI × SPI)`
- `ETC = EAC − AC`；`VAC = BAC − EAC`

## 四、例题

BAC=100 万，第 10 天计划完成 50%（PV=50），实际完成 40%（EV=40），实际花费 AC=45。

CV=40−45=−5（超支）；CPI=40/45≈0.89；SV=40−50=−10（落后）；SPI=40/50=0.8。
EAC（典型）=100/0.89≈112.4 万；ETC≈67.4 万；VAC≈−12.4 万。

## 五、自测

- [ ] PV/EV/AC 定义与计算
- [ ] CV/SV/CPI/SPI 符号含义
- [ ] EAC 三种情形及适用
- [ ] ETC 与 VAC 公式
