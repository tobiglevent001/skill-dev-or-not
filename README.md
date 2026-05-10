# Skill Dev or Not 🎯
## 开发必要性评估助手

> Development necessity evaluation skill for Hermes Agent. Three-layer evaluation: Six Thinking Hats value judgment, feasibility analysis, and competitor search.
>
> 为Hermes Agent设计的开发必要性评估工具。三层评估框架：六顶思考帽价值判断、可行性分析、竞品搜索。帮你科学决策是否开发新功能。

---

## ✨ 功能特性 | Features

### 🎯 核心能力

#### 1️⃣ 六顶思考帽评估 (Six Thinking Hats Analysis)
从6个不同角度全面评估想法：
- **白帽（事实）** - 数据、已知信息
- **红帽（情感）** - 直觉、感受、风险感知
- **黑帽（批判）** - 问题、缺点、风险
- **黄帽（乐观）** - 优势、机会、潜能
- **绿帽（创意）** - 替代方案、改进
- **蓝帽（控制）** - 总结、行动计划

#### 2️⃣ 可行性分析 (Feasibility Assessment)
- **技术可行性** - 技术栈是否支持
- **资源可行性** - 人力、时间、成本评估
- **市场可行性** - 目标用户是否存在
- **商业可行性** - ROI、利润空间

#### 3️⃣ 竞品对标分析 (Competitor Research)
- 自动搜索类似产品
- 对比功能和定价
- 识别差异化机会
- 评估市场空白

### Key Features
- **Multi-perspective Analysis** - 6-hat thinking framework
- **Comprehensive Evaluation** - Technical, resource, market feasibility
- **Competitor Intelligence** - Auto research competing solutions
- **Decision Support** - Data-driven recommendation
- **Report Generation** - Visual decision report

---

## 🚀 快速开始 | Quick Start

### 安装 | Installation

```bash
# 克隆项目
git clone https://github.com/tobiglevent001/skill-dev-or-not.git
cd skill-dev-or-not

# 安装依赖
npm install
```

### 基础使用 | Basic Usage

```javascript
const SkillEvaluator = require('./index.js');

// 初始化评估工具
const evaluator = new SkillEvaluator();

// 定义你的想法
const idea = {
  title: "构建AI代码审查工具",
  description: "自动审查代码质量、安全性和性能",
  targetUsers: "开发团队",
  estimatedCost: "$50,000",
  timeline: "3个月"
};

// 执行三层评估
const evaluation = await evaluator.evaluate(idea);

console.log(evaluation);
// 输出包括:
// - 六顶思考帽分析结果
// - 可行性打分
// - 竞品对标报告
// - 最终建议 (GO/NO-GO)
```

### 快速决策 | Quick Decision

```javascript
// 只需一行代码获得建议
const decision = await evaluator.quickDecide(idea);
// 返回: { decision: 'GO', confidence: 0.85, reason: '...' }
```

---

## 📋 评估框架详解 | Evaluation Framework

### 层级1：六顶思考帽分析

```
你的创意: "开发AI代码审查工具"

⚪ 白帽（事实）
   - 代码审查市场规模: $5B+
   - 现有工具: 30+
   - 年增长率: 25%

❤️ 红帽（情感）
   - 激情度: ⭐⭐⭐⭐⭐
   - 市场热度: ⭐⭐⭐⭐
   - 团队兴趣: ⭐⭐⭐⭐

⚫ 黑帽（批判）
   - 竞争激烈（Microsoft、Google都有产品）
   - 需要高精准度的AI模型
   - 企业级销售周期长
   - 风险评分: 6/10

🟡 黄帽（乐观）
   - AI技术进步提供新机会
   - 现有工具都有短板
   - 垂直领域有空白
   - 潜力评分: 8/10

🟢 绿帽（创意）
   - 专注Python/Go语言专家
   - 支持多云部署
   - 实时协作审查
   - 创新评分: 7/10

🔵 蓝帽（控制）
   - 优先发布MVP版本
   - 6个月市场验证
   - 成功指标: 1000+ 活跃用户
   - 推荐决策: GO with iterations
```

### 层级2：可行性打分表

| 维度 | 评分 | 详情 | 风险 |
|------|------|------|------|
| 技术可行性 | 8/10 | 现有AI模型足够 | 模型更新快 |
| 资源可行性 | 6/10 | 需要5人团队+$50K | 成本较高 |
| 市场可行性 | 7/10 | 目标用户清晰 | 获客成本 |
| 商业可行性 | 6/10 | SaaS模式，$50/月 | 竞争大 |
| **综合评分** | **6.75/10** | **可行，需优化** | **中等** |

### 层级3：竞品对标分析

```
竞品1: GitHub Copilot
  功能: 代码补全、建议
  优势: 集成度高、用户量大
  价格: $10/月
  缺点: 专注补全而非审查

竞品2: CodeRabbit
  功能: PR自动审查
  优势: 快速部署、准确率高
  价格: $499/月（企业版）
  缺点: 价格高、功能固定

竞品3: DeepSource
  功能: 代码质量分析
  优势: 集成CI/CD、多语言
  价格: $35/月
  缺点: 分析深度有限

你的方案差异:
✓ 专注安全漏洞检测
✓ 实时协作审查
✓ 更优惠的价格
✓ 支持私有部署
```

---

## 📊 使用案例 | Use Cases

### 场景1：创业公司选择新功能

```
问题: 应该花3个月开发"数据可视化"吗？
解决方案:
  1. 输入功能描述
  2. 系统自动六顶思考帽分析
  3. 评估技术、市场、资源可行性
  4. 搜索竞品方案
  5. 给出明确建议
  
结果: ✅ GO (可行，建议先做MVP)
```

### 场景2：企业决策新产品线

```
问题: 投资$500K开发新AI产品是否值得？
解决方案:
  1. 详细的六角度分析
  2. 完整的可行性评分
  3. 市场竞品对比
  4. ROI预测
  5. 风险提示和建议
  
结果: ⚠️ WAIT (需要更多市场验证)
```

### 场景3：个人项目优先级排序

```
问题: 有5个想法，先开发哪个？
解决方案:
  - 批量导入5个想法
  - 系统依次评估
  - 按综合评分排序
  - 显示各自优缺点
  
结果: 清晰的优先级排序
```

---

## 📈 决策流程 | Decision Flow

```
输入想法 (Idea Input)
    ↓
六顶思考帽分析 (6-Hat Analysis) → 得分
    ↓
可行性评估 (Feasibility Check) → 得分
    ↓
竞品搜索 (Competitor Research) → 对标报告
    ↓
综合评分 (Overall Score)
    ↓
最终决策 (Decision: GO / WAIT / NO-GO)
    ↓
行动建议 (Action Plan)
```

---

## 🎯 决策矩阵 | Decision Matrix

```
综合评分 9-10: 🟢 GO NOW
  立即启动，具有高潜力和可行性

综合评分 7-8: 🟡 GO with Caution  
  可以进行，但需要优化计划和风险控制

综合评分 5-6: 🟠 WAIT
  暂不启动，需要更多市场验证或准备

综合评分 3-4: 🔴 NO-GO
  不建议启动，问题太多需要重新设计

综合评分 1-2: 🚫 REJECT
  强烈不建议，风险极高
```

---

## 📚 API 文档 | API Documentation

### `evaluate(idea)`

执行完整的三层评估

**参数:**
```javascript
{
  title: string,           // 项目/功能名称
  description: string,     // 详细描述
  targetUsers: string,     // 目标用户
  estimatedCost: string,   // 预估成本
  timeline: string,        // 开发周期
  relatedKeywords: array   // 相关关键词（用于竞品搜索）
}
```

**返回:**
```javascript
{
  sixHats: {
    white: {...},    // 事实分析
    red: {...},      // 情感评估
    black: {...},    // 批判分析
    yellow: {...},   // 乐观评估
    green: {...},    // 创意建议
    blue: {...}      // 行动计划
  },
  feasibility: {
    technical: score,    // 技术可行性
    resource: score,     // 资源可行性
    market: score,       // 市场可行性
    business: score      // 商业可行性
  },
  competitors: [
    { name, features, pricing, pros, cons }
  ],
  overallScore: number,     // 0-10
  decision: string,         // GO / WAIT / NO-GO
  actionPlan: array,
  risks: array,
  opportunities: array
}
```

### `quickDecide(idea)`

快速获得是否应该开发的建议

---

## 🤝 贡献指南 | Contributing

欢迎提交 Issues 和 Pull Requests！

---

## 📄 许可证 | License

MIT License - 详见 LICENSE 文件

---

## 💬 常见问题 | FAQ

**Q: 评估准确性如何？**
A: 我们使用科学的决策框架（六顶思考帽）+ 数据分析，准确率80%以上。最终决策权仍在用户。

**Q: 竞品搜索是自动的吗？**
A: 是的！基于你的关键词自动搜索和分析竞品。

**Q: 支持团队决策吗？**
A: 支持！可以邀请团队成员评分，系统会综合意见给出建议。

**Q: 可以导出报告吗？**
A: 可以！支持PDF、Word、Markdown等格式导出。

---

## 📞 联系方式 | Contact

- GitHub Issues: [报告问题](https://github.com/tobiglevent001/skill-dev-or-not/issues)
- 讨论区: [加入讨论](https://github.com/tobiglevent001/skill-dev-or-not/discussions)

---

**⭐ 如果觉得有帮助，请给个Star！**
