---
title: "AAD 项目定义"
date: "2026-05-28"
tags:
  - "#pipeline/2_paradigm"
  - "#modality/eeg"
  - "#modality/ear_eeg"
  - "#modality/audio"
  - "#method/domain_generalization"
status: "active"
---

# AAD — 听觉注意力解码

## 研究目标

从"离线验证可行"走向"在线实时可用"的听觉注意力解码系统。

## 核心问题

1. **跨被试泛化**：当前 PiMT 跨被试准确率仅 58.6%，如何提升至 ≥75%？
2. **实时性**：端到端延迟 <200ms，满足在线 BCI 要求
3. **多场景适应**：从实验室单一场景走向真实复杂音频环境

## 技术路线

```
范式设计 → 离线解码基线 → 在线适配系统 → 硬件闭环
```

### 阶段 1：范式设计

- 多场景 AAD 实验范式（SustAC/SwitAC/ConvAC）
- PsychoPy 脚本、刺激材料规范

### 阶段 2：离线解码基线

- TRF / PiMT / 深度学习（EEGNet/Mamba）对比
- 跨被试泛化评估

### 阶段 3：在线适配系统

- 快慢双系统：Foundation Model + Adapter + fast_context
- 流式输入、实时推理

### 阶段 4：硬件闭环

- NeuroSonic 耳机集成
- 边缘推理 <50ms

## 预期产出

| 产出 | 目标 |
|:---|:---|
| AAD 范式库 | 3+ 种多场景范式 |
| 离线基线 | 跨被试准确率 ≥75% |
| 在线系统 | 端到端延迟 <200ms |
| 论文 | 1-2 篇期刊/会议 |

## 相关文献

- [[2025_Beyond_Hearing_PiMT_NeuroBuds|Yoon et al. 2025 - PiMT NeuroBuds]]
- [[2026_Neural_Tracking_Mobile_EEG|Wilroth et al. 2026 - Mobile EEG AAD]]
- [[2026_From_Selective_Listening_Brain_Controlled_Hearing|Mesgarani 2026 - AAD Perspective]]
