# Brain-Lab

EEG-BCI 研究团队共享知识库

## 项目概览

| 项目 | 目录 | 核心目标 |
|:---|:---|:---|
| 听觉注意力解码 | `Public/AAD/` | 在线实时 AAD 系统 |
| 在线降噪 | `Public/Denoising/` | 任务特征保真的 EEG 降噪 |
| 持续学习运动想象 | `Public/Continual_Learning_MI/` | 解决 MI 离线-在线断崖 |

## 目录结构

```
Brain-Lab/
├── CLAUDE.md
├── Public/
│   ├── AAD/
│   ├── Denoising/
│   └── Continual_Learning_MI/
├── Private/
│   ├── LiaoYuan/
│   ├── HanQiushi/
│   └── HuHaoqi/
└── README.md
```

## 文件夹定义

### Public/ — 团队共享区

项目相关的所有共享内容，按项目划分。

#### 项目文件夹（AAD / Denoising / Continual_Learning_MI）

| 文件/目录 | 用途 |
|:---|:---|
| `proposal.md` | 项目定义：研究目标、核心问题、技术路线、预期产出 |
| `progress.md` | 进展看板：里程碑状态、当前阶段、阻塞项、下一步行动 |
| `Literature/` | 项目相关文献笔记（按 SOP 5 标准解读） |
| `Paradigm/` | 实验范式设计（PsychoPy 脚本、刺激材料规范） |
| `Baseline_Models/` | 离线基线模型（传统方法 + 深度学习） |
| `Online_System/` | 在线解码系统（流式推理、延迟测试） |
| `Evaluation/` | 评估指标、benchmark 结果汇总 |
| `Data_Protocol/` | 数据采集协议、标注规范（Denoising） |
| `Model_Architecture/` | 模型架构设计文档（Denoising） |
| `Verification_Framework/` | 验证框架（Denoising） |
| `Deployment/` | 在线推理、边缘部署方案（Denoising） |
| `Offline_Benchmark/` | 离线基线（Continual Learning MI） |
| `Simulation_Platform/` | 仿真验证平台（Continual Learning MI） |
| `Online_Adaptation/` | 在线适配系统（Continual Learning MI） |
| `Continual_Learning/` | 持续学习策略（Continual Learning MI） |

### Private/ — 个人工作区

每位成员的私有工作空间，存放个人笔记、草稿和实验记录。

| 文件/目录 | 用途 |
|:---|:---|
| `README.md` | 个人简介：角色、研究方向、技能栈、负责项目 |
| `Contribution_Log.md` | 贡献记录：按时间线记录对各项目的贡献 |
| `00_Inbox/` | 碎片想法、待处理材料（处理后清空） |
| `01_Lab_Journal/` | 实验日志、会议笔记、调试记录 |
| `02_Literature/` | 个人文献阅读笔记（可提炼后同步到 Public） |
| `03_Knowledge_Base/` | 个人知识沉淀、方法论总结 |
| `05_Scripts/` | 个人脚本工具 |
| `07_Assets/` | 个人 PDF、原始材料 |

### 根目录

| 文件 | 用途 |
|:---|:---|
| `CLAUDE.md` | 团队 Agent 指令集：标签系统、SOP、格式规范、防虚构规则 |
| `README.md` | 本文件：仓库说明和文件夹定义 |

## 快速开始

1. 阅读 `CLAUDE.md` 了解团队工作规范和标准操作流
2. 进入你的 `Private/{姓名}/` 目录，填写 `README.md` 个人简介
3. 阅读各项目 `proposal.md` 了解研究目标
4. 查看 `progress.md` 了解当前进展
5. 从 `00_Inbox/` 开始，按 SOP 1 处理碎片信息

## 贡献者

- LiaoYuan
- HanQiushi
- HuHaoqi
- ZhangYicheng
- SunYixiang
