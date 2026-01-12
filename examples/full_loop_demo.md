# 全链路实战演示 (Full Loop Demo)

为了让你直观理解 Prometheus 框架的威力，我们模拟了一个完整的用户故事。
看 AI 如何从**混乱的日常琐事**中，提炼出**深刻的生存智慧**。

---

## 🎬 场景背景
*   **用户**: Alex，一名独立开发者。
*   **状态**: 最近感到焦虑，效率低下，正在尝试通过喝咖啡提神。
*   **时间**: 2025年11月14日。

## 📥 输入数据 (L1: Sensory Stream)
> *这是 Alex 在一天中产生的碎片化数据，散落在 Log、Task 和 Finance 模块中。*

```json
{
  "logs": [
    "[09:30] 困死了，去星巴克买了个特大杯冷萃，希望能醒醒脑。",
    "[11:00] 还是写不出代码，心跳好快，感觉手在抖，甚至有点想吐。",
    "[14:00] 彻底摆烂了，刷了两个小时推特，我是个废物。",
    "[23:00] 躺在床上睡不着，脑子里全是今天没写完的代码，焦虑。"
  ],
  "tasks": [
    {"title": "完成支付接口开发", "status": "failed", "reason": "无法集中注意力"},
    {"title": "阅读技术文档", "status": "skipped", "reason": "心情烦躁"}
  ],
  "finance": [
    {"merchant": "Starbucks", "amount": 38.0, "notes": "提神续命"}
  ],
  "biometrics": {
    "avg_heart_rate_morning": 95, // 异常偏高 (平时 70)
    "sleep_score": 55 // 严重不足
  }
}
```

---

## ⚙️ 3AM 处理过程 (The Black Box)
> *AI 引擎介入，执行 `Daily Evolution Protocol`。*

1.  **关联分析**: AI 发现 `Starbucks (Finance)` 与 `手抖/心跳快 (Logs/Bio)` 之间的时间相关性。
2.  **因果推演**: 推断“咖啡因”是导致“生理焦虑”和“任务失败”的直接原因。
3.  **规则生成**: 判定这是一个需要干预的生理特质。

---

## 📤 输出数据 (L3 & L4 Artifacts)
> *这是 AI 生成并存入数据库的 JSON 结果。*

```json
{
  "evolution_score": 45, // 评分较低，因为状态失控
  "daily_summary": "典型的'咖啡因诱导焦虑'案例。试图通过咖啡因解决睡眠不足，反而引发了生理应激反应，导致全天崩盘。",

  "memory_consolidation": {
    "new_atomic_facts": [
      {
        "category": "bio_rhythm",
        "content": "用户对高浓度咖啡因（如冷萃）耐受度极低，摄入后会出现心悸、手抖等躯体化焦虑症状。",
        "confidence": 0.98,
        "implications": {
          "action_type": "constraint",
          "advice": "在睡眠不足状态下，绝对禁止摄入咖啡因，应通过补觉恢复。"
        },
        "cluster_tag": "Caffeine_Sensitivity",
        "supporting_evidence": "Log[11:00] '手抖想吐' + Bio[HR:95]"
      }
    ],
    "updated_system_rules": [
      // L4 级别的新增规则
      "Constraint: 当检测到用户前一晚睡眠分数 < 60 时，Planner 必须自动屏蔽所有‘咖啡/提神’类建议，并强制安排午休。"
    ]
  },

  "planning_directives": {
    "focus_mode": "recovery",
    "context_injection": "检测到昨日因咖啡因导致严重焦虑，今日建议执行‘低多巴胺’恢复计划，避免任何刺激性饮食。"
  }
}
```

## 🔮 结果反馈 (The Payoff)
第二天早上，当 Alex 打开应用生成计划时，AI **不再** 建议他“喝杯咖啡开始工作”，而是：

> **🌞 早安，Alex。**
> 鉴于你昨晚睡得不好且昨天对咖啡因反应强烈 **[Fact: Caffeine Sensitivity]**，今天的策略是**“温和启动”**。
> 
> *   🚫 **已移除**：早晨的高难度编码任务。
> *   ✅ **已添加**：10:00 - 10:30 户外散步（阳光有助于调节皮质醇）。
> *   🍵 **建议**：早餐请选择花草茶或温水。

**这就是 Prometheus 的价值：它记住了你的痛苦，并帮你避免重蹈覆辙。**
