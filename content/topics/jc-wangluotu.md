---
slug: jc-wangluotu
title: 网络图与关键路径
date: 2026-10-31
tags: [网络图, 关键路径, 浮动时间]
summary: 前导图 PDM、正推求 ES/EF、逆推求 LS/LF、总浮动与自由浮动计算，附例题。
cover:
parent: jindu-chengben
---

## 一、前导图法（PDM）

活动在节点，箭头表示依赖，最常见 **FS（完成-开始）**。也支持 SS、FF、SF。

## 二、双推算法

- **正推（Forward）**：从起点，ES = max(前驱 EF)，EF = ES + 历时。项目总工期 = 终点 EF 最大值。
- **逆推（Backward）**：从终点，LF = min(后继 LS)，LS = LF − 历时；终点 LF = 总工期。

## 三、浮动时间

- **总浮动 TF** = LS − ES = LF − EF；关键活动 TF = 0。
- **自由浮动 FF** = min(后继 ES) − 本活动 EF（不影响任何后继最早开始）。

## 四、例题

活动：A(3) FS→B(4)、C(5)；B、C 均 FS→D(2)。

正推：A: ES0 EF3；B: ES3 EF7；C: ES3 EF8；D: ES8 EF10 → 总工期 10。
逆推：D: LF10 LS8；B: LF8 LS4；C: LF8 LS3；A: LF4 LS1。
TF：A=1, B=1, C=0, D=0 → 关键路径 A→C→D，工期 10。

## 五、自测

- [ ] 正推/逆推公式
- [ ] TF 与 FF 区别
- [ ] 关键活动 TF 必为 0
