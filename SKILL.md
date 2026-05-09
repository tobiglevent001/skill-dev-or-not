---
name: skill-dev-or-not
description: "Use when deciding whether to develop a new skill/feature. Runs three-layer evaluation: value judgment (Six Thinking Hats), feasibility analysis (token/time/cost), and competitor search. Outputs development recommendation in Chinese or English."
version: 1.0.0
author: tobiglevent001
license: MIT
metadata:
  hermes:
    tags: [decision-making, evaluation, skill-authoring, planning]
    related_skills: [writing-plans, hermes-agent-skill-authoring, spike]
---

# Skill Dev-or-Not — 开发必要性评估助手

## Overview

当你有一个新的 skill 或功能开发 ideas 时，在投入时间和 token 之前，先调用本 skill 做系统性评估。通过三层决策模型，帮你判断**值不值得做**。

三层模型：
1. **价值判断** — 六项思考帽多角度审视需求价值
2. **可行性评估** — 技术复杂度、耗时、Token 消耗、成本（人民币+美元）
3. **竞品排查** — 现有 skill / 开源方案 / 网络工具是否有同类

最终输出明确的**开发建议**。

【English Version】
When you have a new skill or feature idea, call this skill before investing time and tokens. It runs a systematic three-layer evaluation to determine whether it's worth building.

Three layers:
1. Value Judgment — Six Thinking Hats
2. Feasibility Assessment — complexity, time, token cost (CNY + USD)
3. Competitor Search — existing skills / open-source / online tools

Outputs a clear development recommendation.

---

## When to Use

- 你有一个新的 skill 开发想法，不确定要不要做
- 团队成员提出需求，需要快速评估
- 你想避免投入时间做别人已经做过的东西
- 你想估算一个功能的开发成本

【English】
- You have a new skill idea and aren't sure whether to build it
- A team member proposed a feature and you need a quick assessment
- You want to avoid building something that already exists
- You want to estimate the development cost of a feature

### Do NOT use for:
- 日常问题查询（用普通对话即可）
- 已有明确结论的简单任务
- 紧急 bug 修复（直接修）

【English】
- Routine Q&A (just ask normally)
- Simple tasks with an obvious answer
- Urgent bug fixes (just fix it)

---

## How to Use

调用方式很简单，直接说：

**中文：** "小马，帮我评估一下[你的需求]要不要开发成 skill"

**English：** "Hey, evaluate whether I should develop [your idea]"

我会自动执行三层评估并输出报告。

---

## 三层评估模型 / Three-Layer Model

### 第1层：价值判断（六项思考帽）
### Layer 1: Value Judgment (Six Thinking Hats)

| 帽子 / Hat | 角度 / Angle | 问题 / Questions |
|---|---|---|
| 白帽 White | 事实 Facts | 用户当前有什么具体需求？现状是什么？ |
| 红帽 Red | 感受 Feelings | 做出来会让人轻松多少？痛点真实吗？ |
| 黑帽 Black | 风险 Risks | 不做会怎样？做了会引入什么问题？ |
| 黄帽 Yellow | 收益 Benefits | 能节省多少时间/提升多少效率？ |
| 绿帽 Green | 创意 Creativity | 有没有更简单的替代方案？ |
| 蓝帽 Blue | 总结 Summary | 综合以上 → 价值打分：高 / 中 / 低 |

### 第2层：可行性评估
### Layer 2: Feasibility Assessment

| 维度 / Dimension | 评估方式 / Method |
|---|---|
| 技术难度 Tech Difficulty | 简单 Simple / 中等 Medium / 复杂 Complex |
| 预估对话轮数 Est. Conversation Rounds | X 轮 rounds |
| 预估 Token 消耗 Est. Token Usage | X 万 tokens |
| 预估成本（按 DeepSeek API）Cost | ¥X.XX 人民币 / $X.XX 美元 |

Token 成本换算标准（DeepSeek API 价格）：
- DeepSeek 输入：¥0.14 / 百万 token（~$0.02）
- DeepSeek 输出：¥0.28 / 百万 token（~$0.04）
- 汇率参考：1 USD ≈ 7.2 CNY

### 第3层：竞品排查
### Layer 3: Competitor Search

| 检查项 / Check | 结果 / Result |
|---|---|
| Hermes 现有 skill 列表 | 有/无 同类 |
| GitHub 开源项目 | 有/无 同类 |
| 网络现有工具 | 有/无 同类 |
| 同类方案评估 | 好/中等/差，建议直接使用/改进/另起炉灶 |

---

## Output Report Format

评估完成后，输出格式如下（中/英文二选一，首次调用时我会询问你的语言偏好）：

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Skill Dev-or-Not 评估报告

需求：[你的需求描述]

━━━ 第1层：价值判断（六项思考帽）━━━

白帽（事实）：...
红帽（感受）：...
黑帽（风险）：...
黄帽（收益）：...
绿帽（创意）：...
蓝帽（总结）：价值 → [高 / 中 / 低]

━━━ 第2层：可行性评估 ━━━

技术难度：简单 / 中等 / 复杂
预估轮数：X 轮对话
预估Token消耗：X 万 tokens
预估成本：¥X.XX（人民币）| $X.XX（美元）

━━━ 第3层：竞品排查 ━━━

Hermes 现有 skill：有 / 无
  → 如存在：XXX skill，评分：好/中/差

GitHub 开源方案：有 / 无
  → 如存在：XXX 项目，评分：好/中/差

网络现有工具：有 / 无
  → 如存在：XXX 工具，评分：好/中/差

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
最终结论：[建议开发 / 不建议开发 / 建议改进现成方案]

理由：
[三段式：价值 + 可行 + 竞品 → 综合判断]

==================================================

【English Version】
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Skill Dev-or-Not – Evaluation Report

Requirement: [your requirement description]

━━━ Layer 1: Value Judgment (Six Thinking Hats) ━━━

White Hat (Facts): ...
Red Hat (Feelings): ...
Black Hat (Risks): ...
Yellow Hat (Benefits): ...
Green Hat (Creativity): ...
Blue Hat (Summary): Value → [High / Medium / Low]

━━━ Layer 2: Feasibility Assessment ━━━

Tech Difficulty: Simple / Medium / Complex
Est. Conversations: X rounds
Est. Token Usage: X0,000 tokens
Est. Cost: ¥X.XX (CNY) | $X.XX (USD)

━━━ Layer 3: Competitor Search ━━━

Hermes existing skills: Yes / No
  → If exists: XXX skill, Rating: Good/Fair/Poor

GitHub open-source: Yes / No
  → If exists: XXX project, Rating: Good/Fair/Poor

Online tools: Yes / No
  → If exists: XXX tool, Rating: Good/Fair/Poor

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Final Verdict: [Recommended / Not Recommended / Improve Existing Solution]

Reasoning:
[Value + Feasibility + Competition → Comprehensive judgment]
```

---

## Common Pitfalls

1. **忘记语言偏好。** 首次使用请告诉我你要中文还是英文，否则我会默认中文。每次都可以切换。
2. **需求描述太模糊。** 越具体的需求，评估越准确。比如"我想做一个清理旧对话的工具"比"帮我处理一下数据"好得多。
3. **只看成本不看价值。** 有些功能 token 成本高但价值巨大（如自动化监控），不要因为成本高就否决。
4. **竞品排查不彻底。** 我会尽力查。但如果你知道某个地方肯定有同类工具，请提前告诉我，节省时间。
5. **误用场景。** 这个 skill 只用于判断"要不要开发"，不用于设计具体方案。如果想讨论怎么实现，请用 `writing-plans` skill。

## **用户决策原则 / User Decision Principle**

本 skill 的输出是**建议**，不是命令。最终是否开发由用户自己决定：

- 我会给出清晰的三层评估报告和结论
- 但不会替用户做决策
- 用户说"开始开发"我才开始，说"不开发"就停下
- 如果用户想先看设计方案再做决定，我会先输出设计方案再让用户决策

**English:**
This skill outputs **recommendations**, not commands. The final decision always belongs to the user:

- I provide a clear three-layer evaluation report with conclusions
- But I don't make the decision for the user
- Development starts only when the user says "go ahead"
- If the user wants to see a design plan before deciding, I output that first

---

## Verification Checklist

- [ ] 用户提出了明确的开发需求
- [ ] 三层评估全部完成
- [ ] Token 成本已按 DeepSeek API 价格换算为人民币和美元
- [ ] 竞品排查覆盖了 Hermes skill / GitHub / 网络三个渠道
- [ ] 输出格式包含完整的评估报告
- [ ] 最终结论清晰：建议开发 / 不建议开发 / 建议改进现有方案
- [ ] 如果用户首次使用，已确认语言偏好（中文/English）

---

## One-Shot Recipe

**场景：用户想开发一个新 skill**

用户说："小马，我想开发一个自动整理桌面文件的 skill，帮我评估一下要不要做"

你执行：
1. 用六项思考帽分析价值
2. 评估技术难度（简单-类似批处理脚本）、预估轮数（3-5轮）、Token消耗、成本
3. 搜索 Hermes 现有 skill 中是否有同类（如没有）、GitHub 搜索（如没有）、网络搜索（很多桌面整理工具但都不是 Hermes skill）
4. 输出完整评估报告，给出结论
