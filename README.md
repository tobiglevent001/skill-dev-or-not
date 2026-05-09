# Skill Dev-or-Not — 开发必要性评估助手

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Hermes Agent Skill](https://img.shields.io/badge/Hermes-Agent%20Skill-blue)](https://hermes-agent.nousresearch.com)

> 当你有一个新的 skill 或功能开发 ideas 时，先别急着写代码——让我帮你评估一下值不值得做。

## 📖 简介

**Skill Dev-or-Not** 是一个 Hermes Agent Skill，通过 **三层决策模型** 帮你系统性地评估一个新的 skill 或功能是否值得开发：

1. **价值判断** — 六项思考帽多角度审视需求价值
2. **可行性评估** — 技术复杂度、耗时、Token 消耗、成本
3. **竞品排查** — 现有 skill / 开源方案 / 网络工具是否有同类

最终输出明确的 **开发建议**，帮你节省时间和不必要的投入。

## 🎯 使用场景

- 你有一个新的 skill 开发想法，不确定要不要做
- 团队成员提出需求，需要快速评估
- 你想避免投入时间做别人已经做过的东西
- 你想估算一个功能的开发成本

## 🚀 快速开始

在 Hermes Agent 中直接说：

**中文：**
```
小马，帮我评估一下[你的需求]要不要开发成 skill
```

**English：**
```
Hey, evaluate whether I should develop [your idea]
```

我会自动执行三层评估并输出报告。

## 🏗️ 三层评估模型

### 第1层：价值判断（六项思考帽）

| 帽子 | 角度 | 问题 |
|------|------|------|
| 白帽 | 事实 Facts | 用户当前有什么具体需求？现状是什么？ |
| 红帽 | 感受 Feelings | 做出来会让人轻松多少？痛点真实吗？ |
| 黑帽 | 风险 Risks | 不做会怎样？做了会引入什么问题？ |
| 黄帽 | 收益 Benefits | 能节省多少时间/提升多少效率？ |
| 绿帽 | 创意 Creativity | 有没有更简单的替代方案？ |
| 蓝帽 | 总结 Summary | 综合以上 → 价值打分 |

### 第2层：可行性评估

| 维度 | 评估方式 |
|------|---------|
| 技术难度 | 简单 / 中等 / 复杂 |
| 预估对话轮数 | X 轮 |
| 预估 Token 消耗 | X 万 tokens |
| 预估成本 | ¥X.XX (CNY) / $X.XX (USD) |

### 第3层：竞品排查

| 渠道 | 检查内容 |
|------|---------|
| Hermes 现有 skill | 是否有同类 |
| GitHub 开源 | 是否有同类项目 |
| 网络工具 | 是否有现成方案 |

## 📝 输出示例

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Skill Dev-or-Not 评估报告

需求：[你的需求描述]

━━━ 第1层：价值判断（六项思考帽）━━━
白帽（事实）：...
红帽（感受）：...
...
蓝帽（总结）：价值 → 高

━━━ 第2层：可行性评估 ━━━
技术难度：中等
预估轮数：3-5轮
预估Token消耗：2万 tokens
预估成本：¥0.03 (CNY) | $0.004 (USD)

━━━ 第3层：竞品排查 ━━━
Hermes 现有 skill：无同类
GitHub 开源方案：无同类
网络现有工具：有类似但非 Hermes skill

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
最终结论：建议开发

理由：价值高 + 技术可行 + 无直接竞品
```

## ⚙️ 安装

将 `SKILL.md` 放到 `~/.hermes/skills/skill-dev-or-not/` 目录下，或在 Hermes Agent 中使用 `skill_manage` 加载。

## 📄 License

MIT
