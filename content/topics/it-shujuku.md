---
slug: it-shujuku
title: 数据库技术
date: 2026-10-31
tags: [数据库, 范式, 事务, SQL]
summary: 关系模型、三范式、事务 ACID 与并发问题、SQL 分类与 CAP 定理。
cover:
parent: itjishu
---

## 一、关系模型

- 表（关系 Relation）、行（元组 Tuple）、列（属性 Attribute）。
- **键**：候选键（能唯一标识）、主键（选定其一）、外键（引用他表主键）。
- **实体完整性**：主键非空且唯一；**参照完整性**：外键须匹配被引用主键或为空。

## 二、范式（递进，必考）

| 范式 | 消除的依赖 | 要求 |
|---|---|---|
| 1NF | 属性原子性 | 字段不可再分 |
| 2NF | 部分函数依赖 | 非主属性完全依赖候选键 |
| 3NF | 传递函数依赖 | 非主属性不传递依赖于键 |

> 实际设计常到 3NF/BCNF；过度规范化会拖慢查询，需适度反规范化。

## 三、事务 ACID 与并发

- **ACID**：原子性（Atomicity）、一致性（Consistency）、隔离性（Isolation）、持久性（Durability）。
- **并发问题**：丢失修改、脏读（读未提交）、不可重复读、幻读。
- **隔离级别**：读未提交→读已提交→可重复读→串行化（由低到高）。

## 四、SQL 分类

- DDL（定义：CREATE/ALTER/DROP）
- DML（操作：SELECT/INSERT/UPDATE/DELETE）
- DCL（控制：GRANT/REVOKE）

## 五、分布式与 CAP

CAP 定理：一致性（C）、可用性（A）、分区容错（P）三者不可兼得，分布式系统必取 P，在 C/A 间权衡。

## 六、自测

- [ ] 三范式递进条件
- [ ] 事务 ACID 含义
- [ ] 四种并发问题
- [ ] DDL/DML/DCL 区分
- [ ] CAP 定理
