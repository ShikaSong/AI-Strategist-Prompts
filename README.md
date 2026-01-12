# 🔥 Prometheus Cognitive Framework (PCF)

> **"We don't evolve in the daylight. We grow in the dark."**
> 
> 一套赋予 AI **“长期记忆”** 与 **“自我进化”** 能力的开源认知架构标准。

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Status: Production Ready](https://img.shields.io/badge/Status-Production%20Ready-success)]()
[![Privacy: First](https://img.shields.io/badge/Privacy-Local%20First-blue)]()

---

## 📖 简介 (Introduction)

**为什么现在的 AI 助手都是“金鱼脑”？**
它们拥有这一秒的上下文，却记不住你上个月的雄心壮志，也看不出你潜意识里的焦虑循环。

**Prometheus (普罗米修斯)** 是一个专为“AI 战略伙伴”设计的后端认知架构。与传统的 Chatbot 不同，它引入了**仿生学的记忆固化机制**：
通过每日凌晨的 **3AM 进化协议**，将用户白天碎片化的行为（L1），经过睡眠般的深层推理，转化为长期生效的人生规则（L4）。

本项目开源了该架构的核心**“大脑” (Prompts & Philosophy)**，旨在为独立开发者和隐私敏感用户提供一套可复用的认知标准。

---

## 🧠 核心架构：L1-L4 记忆模型 (The Cortex)

我们将 AI 的记忆深度划分为四个层级，模拟人类从感官输入到智慧形成的过程：

| 层级 | 名称 | 形态 | 更新频率 | 作用 |
| :--- | :--- | :--- | :--- | :--- |
| **L1** | **感官流 (Sensory)** | 原始日志/消费流水/心率 | 实时 | 混乱、包含噪音的原始数据。 |
| **L2** | **情景记忆 (Episodic)** | 结构化日报 | 每日 (3AM) | 对一天的降噪总结（"昨天发生了什么"）。 |
| **L3** | **语义记忆 (Semantic)** | **原子事实 (Atomic Facts)** | 动态 | 剥离时间背景的客观事实（"用户对咖啡因敏感"）。 |
| **L4** | **核心画像 (Rules)** | **系统指令 (Instructions)** | 不定期 | 系统的本能行为准则（"禁止在睡眠不足时安排高压任务"）。 |

👉 *[深入了解 L1-L4 架构哲学](philosophy/L1_to_L4_Model.md)*

---

## ⚙️ 核心机制：3AM 进化协议

人类海马体在深度睡眠时固化记忆。Prometheus 复刻了这一过程。
我们拒绝在白天进行昂贵的全量计算，而是通过异步批处理：

1.  **Extraction (提取)**: 扫描昨日所有数据。
2.  **Foresight (推演)**: 寻找跨数据的因果关系（如：消费支出 vs 心率波动）。
3.  **Arbitration (仲裁)**: 解决新事实与旧规则的逻辑冲突。
4.  **Directives (指令)**: 生成次日的行动指南。

👉 *[查看 3AM 协议技术细节](philosophy/3AM_Protocol.md)*

---

## 📂 核心资源导航 (Directory)

本项目包含经过生产环境验证的高精度 Prompts（基于 Jinja2 模板）：

### 1. 记忆中枢 (The Cortex)
*   **[每日进化](prompts/cortex/daily_evolution.md)**: 系统的核心心跳，执行因果推演。
*   **[记忆融合](prompts/cortex/fact_merging.md)**: 如何将碎片化信息聚类并去重。
*   **[逻辑仲裁](prompts/cortex/logic_arbitration.md)**: 基于时效性解决记忆冲突。

### 2. 战略与执行 (Strategy & Planning)
*   **[日程骨架生成](prompts/planning/skeleton_generation.md)**: 基于精力管理的日程排布。
*   **[愿景拆解](prompts/strategy/goal_breakdown.md)**: Vision -> SMART Goals。
*   **[内容深度解析](prompts/creation/content_analysis.md)**: **(热门)** 长文本 -> 视频脚本 + Anki 卡片。

### 3. 垂直领域专家 (Specialists)
*   **[财务价值审计](prompts/finance/value_audit.md)**: 不记流水账，只评判“这笔钱是否值得”。
*   **[社交破冰](prompts/hearth/rekindle.md)**: 高情商的社交重启话术。
*   **[心理洞察](prompts/insight/weekly_psychology.md)**: 分析“渴望-行动”差距。

---

## 🛡️ 隐私宣言 (Privacy Manifesto)

作为一个由独立开发者维护的项目，我们深知“信任”是唯一的护城河。

1.  **No Training (不训练)**: 你的数据属于你。我们承诺（无论是代码逻辑还是商业模式）绝不使用用户数据训练通用大模型。
2.  **Manual Mode (手动模式)**: 本架构原生支持 **"Bring Your Own Key"**。你可以通过 API 仅获取 Prompt，自行在本地或受信任的 LLM 上运行，数据完全不经过我们的服务器。
3.  **Local-First Philosophy**: 我们的长远目标是适配 Ollama 等本地模型，实现 100% 的离线数据闭环。

---

## 🧩 如何使用？ (Integration)

虽然本项目未开源后端工程代码（FastAPI/Celery），但你完全可以复用这些 Prompts 构建自己的系统：

1.  **Context Assembly**: 按照 Markdown 中的 `User Prompt` 结构，从你的数据库中提取相应数据（如日志、任务）。
2.  **Rendering**: 使用 Jinja2 渲染模板。
3.  **Execution**: 发送给支持 JSON Mode 的 LLM（推荐 GPT-4o, Gemini 1.5 Pro, DeepSeek-V3）。
4.  **Persistence**: 解析返回的 JSON，存入你的向量数据库。

👉 *[查看完整实战演示 (Full Loop Demo)](examples/full_loop_demo.md)*

---

## 🤝 贡献与反馈

这是一个探索性的认知架构。
如果你对 **"如何让 AI 理解人类隐喻"** 或 **"记忆权重的衰减算法"** 有独到见解，欢迎提交 Issue 或 PR 优化 Prompts。

*   **作者**: ShikaSong 志明与春娇（doge）
*   **应用内测**: prometheusplan.me

---

**License**: [CC BY-NC-SA 4.0](LICENSE) (署名-非商业性使用-相同方式共享)
*Prompts are the soul; Code is just the body.*
