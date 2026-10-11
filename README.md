# 用 Python 写 Agent 内核 · OpenHands SDK 费曼精读

> 个人学习仓：用费曼学习法精读 [OpenHands software-agent-sdk](https://github.com/OpenHands/software-agent-sdk)（Python 写的 coding agent 内核，SWE-Bench 77.6），目标是吃透"Agent = 循环 + 工具"并最终亲手写一个 300 行迷你内核。

## 📌 背景

- 起点：想搞懂日常用的 ZCode 内核能否用 Python 重写 → 实证结论：ZCode 100% TypeScript（全仓 0 个 `.py`），但**内核形态完全可以且值得用 Python 学**——OpenHands 就是工业级活证据（litellm + pydantic + fastmcp，与我的 DGA 项目同技术栈）
- OpenHands 已于 2025-08 拆仓：主仓 = Agent Canvas（TS 控制台 90.5k★），Python 内核在独立仓 software-agent-sdk
- 学习方式：费曼四步（定界 → 外化 → 诊断 → 重构），新概念先讲后考

## 🗺️ 学习地图与进度

| 单元 | 主题 | 状态 |
|------|------|------|
| U1 | 全景：agent = while 循环 + 工具箱；hello world 逐行 | 🔵 已开讲，2 道检验题待收 |
| U2 | 会话与事件流：Conversation 与事件 = ODS 不可变明细账 | ⬜ |
| U3 | LLM 调用层：litellm = JDBC；messages = 带角色的对话账本 | ⬜ |
| U4 | 一轮 step 解剖：压缩→调模型→解析→执行→回填 | ⬜ |
| U5 | 工具系统：ToolDefinition + register_tool = UDF 注册 | ⬜ |
| U6 | 状态机与兜底：STUCK / 审批门 / 预算 | ⬜ |
| U7 | （进阶·轻讲）condenser 压缩、并行工具执行 | ⬜ |
| U8 | 收官：自写 300 行迷你内核 | ⬜ |

## 📂 内容导航

| 文件 | 是什么 |
|------|--------|
| `OpenHands解读.md` | 源码总解读：双仓演变时间线、目录地图（数仓分层类比）、主循环解剖、依赖对照表 |
| `OpenHands解读.html` | 图解卡：时间线 / 分层架构图 / 主循环流程图 / 自测卡（单文件零依赖） |
| `费曼带学提示词-Python-Agent内核.md` | 定制费曼带学提示词，新会话粘贴即用（含学生画像、教学规则、八单元地图、教材路径） |
| `学习记录/` | 每单元一篇：讲解要点 + 检验题 + 语法债 + 本轮学习记录 |

## 🔧 用法

上下文不足或换机器时：新开会话，把 `费曼带学提示词-Python-Agent内核.md` 中"提示词正文"整段粘贴给 AI 编程助手即可接续带学。

## 📜 出处与声明

- 精读对象源码：[OpenHands/software-agent-sdk](https://github.com/OpenHands/software-agent-sdk)（MIT）与 [OpenHands/OpenHands](https://github.com/OpenHands/OpenHands)，本仓**不含**其源码，只放本人原创学习笔记
- 源码快照（2026-10-11，浅克隆）存于本人本地知识库，不入本仓
- 本仓为 private 个人学习仓
