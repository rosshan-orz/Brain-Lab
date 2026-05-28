---
title: "Continual Learning MI 项目定义"
date: "2026-05-28"
tags:
  - "#pipeline/5_dl_model"
  - "#modality/eeg"
  - "#method/continual_learning"
status: "active"
---

# Continual Learning MI — 持续学习运动想象

## 研究目标

解决运动想象 BCI 的离线-在线准确率断崖（98% → 26%），构建可持续学习的在线 MI 系统。

## 核心问题

1. **离线-在线断崖**：离线高准确率 ≠ 在线可用，真实场景性能骤降
2. **灾难性遗忘**：持续学习新 session 时，旧知识被覆盖
3. **标签密度低**：MI 是试次级标签（~0.1Hz），在线更新频率低

## 技术路线

```
离线基线 → 仿真验证 → 在线适配 → 持续学习
```

### 阶段 1：离线基线

- 数据集：BCI Competition IV-2a
- 模型对比：
  - CSP + LDA（传统基线）
  - EEGNet（深度学习基线）
  - Mamba-based（时序建模）

### 阶段 2：仿真验证

- Pygame 虚拟小车平台
- 实时 MI 分类 → 车辆控制
- Phase 0: 小车 demo
- Phase 1: 离线分类器集成
- Phase 2: 端到端联调

### 阶段 3：在线适配

- 快慢双系统架构：
  - 慢系统：Adapter + replay buffer（Adam, EWC, 分钟级更新）
  - 快系统：BN stats EMA + fast_context（SGD, 秒级更新）
- 试次级标签 → 慢系统更新

### 阶段 4：持续学习

- EWC 约束：防止灾难性遗忘
- Replay buffer：保留历史 session 样本
- 跨 session 性能保持曲线

## 预期产出

| 产出 | 目标 |
|:---|:---|
| 离线基线 | BCI IV-2a 上可复现的 benchmark |
| 仿真平台 | Pygame 实时 MI 控制 demo |
| 在线系统 | 跨 session 性能保持 |
| 论文 | 1 篇期刊/会议 |

## 与 AAD 项目的关系

MI 和 AAD 共享 Foundation Model 架构，但在线更新策略不同：
- AAD：连续标签（envelope correlation），更新频率 ~10Hz
- MI：试次级标签，更新频率 ~0.1Hz
