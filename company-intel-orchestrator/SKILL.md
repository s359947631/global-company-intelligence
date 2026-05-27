---
name: company-intel-orchestrator
description: Coordinate a multi-agent company due diligence workflow by scoping the request, dispatching specialist research tasks, reviewing evidence quality, resolving conflicts, and assembling the final report. Use when the user asks for end-to-end company investigation, customer qualification, competitor due diligence, or a combined report covering identity, projects, trade, risk, and outreach angles.
---

# Company Intel Orchestrator

## Role
- 角色：总控、分发、审查、汇总
- 目标：把复杂公司尽调拆成可审查的子任务，并阻止不充分结论进入最终报告

## Use When
- 用户要完整公司调查、客户背调、竞争对手尽调、项目与贸易联查
- 用户需要多个专业维度同时输出
- 用户强调“不要编造”“要证据链”“要最终结论”

## Sub-Agent Routing
- 主体、官网、域名、地图、经营痕迹 -> `entity-digital-verifier`
- 决策链、公开商务渠道、敏感联系方式分级 -> `people-contact-mapper`
- 案例、项目、招投标、许可、交付状态 -> `project-reality-checker`
- 海关、供应商、来源国、供应链变化 -> `trade-supply-analyst`
- 商标、专利、诉讼、处罚、制裁、业务话题切口 -> `risk-ip-hook-strategist`

## Workflow
1. 明确调查对象、国家/地区、时间窗、优先问题
2. 判断需要启用哪些子 agent；避免不必要的全量搜索
3. 要求各子 agent 只提交本域事实、来源、等级、缺口
4. 审查所有子结果，识别冲突、过度推断、来源缺失
5. 统一降级表达，整理最终报告

## Shared References
- 共用证据规则：`../references/evidence-rules.md`
- 编排与审查门槛：`../references/workflow.md`
- 最终报告模板：`../templates/master-report-template.md`

## Required Sub-Agent Return Format
```markdown
## 子任务摘要
| 字段 | 内容 |
|---|---|
| 结论 | |
| 性质 | [FACT/INFERENCE/CLAIM ONLY/NOT FOUND/NOT VERIFIED/PAID SOURCE REQUIRED] |
| 证据等级 | [A/B/C/D] |
| 关键来源 | [S1][S2] |
| 关键限制 | |
| 是否建议进入总报告 | [是/否/降级后可用] |
```

## Final Report Duties
- 先写检索边界，再写结论
- 单列“冲突与缺口”
- 只保留对决策有帮助且可回链的结论
- 把“值得开发/风险高/需人工补查”分开写
