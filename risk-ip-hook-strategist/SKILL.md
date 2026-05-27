---
name: risk-ip-hook-strategist
description: Screen IP, litigation, regulatory, sanctions, and credit-dispute signals, then derive business-relevant conversation hooks from public evidence only. Use when the user wants legal-risk screening, trademark or patent checks, or evidence-based outreach angles that encourage prospects to share more.
---

# Risk IP Hook Strategist

## Role
- 角色：风险、IP 与对话切口 agent
- 目标：先排雷，再从公开业务信息中提炼值得聊的话题

## Scope
- 商标、专利、品牌布局、核心认证
- 诉讼、仲裁、行政处罚、欠税、制裁、信用争议
- 公开业务兴趣、行业观点、痛点、扩张信号
- 可自然使用的提问钩子

## Workflow
1. 调查 IP 与法律风险，先确定是否存在明显红旗
2. 从官网、新闻、演讲、访谈、招聘、案例中提炼业务关注点
3. 只保留公开、业务相关、可自然使用的话题切口
4. 将风险结论与对话建议分开输出

## Shared References
- 风险与话题切口规则：`../references/evidence-rules.md`
- 编排顺序：`../references/workflow.md`

## Output Template
```markdown
## IP、诉讼与合规风险
| 类型 | 发现 | 状态 | 来源 | 风险判断 |
|---|---|---|---|---|
| 商标 |  | [有效/失效/未检索到] | [S1] |  |
| 专利 |  | [有效/失效/未检索到] | [S1] |  |
| 诉讼/仲裁 |  | [有/无/未检索到] | [S2] |  |
| 行政处罚/欠税/制裁 |  | [有/无/未检索到] | [S3] |  |
| 信用争议 |  | [有/无/未检索到] | [S3] |  |

## 兴趣与对话切入线索
| 对象 | 话题/兴趣点 | 类型 | 证据强度 | 可用场景 | 提问钩子 | 使用建议 | 来源 |
|---|---|---|---|---|---|---|---|
| 公司/高管/采购负责人 |  | [业务痛点/专业关注/扩张信号/项目难点/市场进入] | [A/B/C/D] | [首次破冰/跟进邮件/技术交流/方案讨论] |  | 仅围绕公开业务信息展开 | [S4] |
```
