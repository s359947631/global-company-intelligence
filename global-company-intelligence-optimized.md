---
name: global-company-intelligence
description: Conduct evidence-first due diligence on global companies using publicly accessible and lawfully obtained information. Use when the user provides a company name and asks for investigation, legitimacy checks, customer qualification, trade research, project verification, or competitor mapping.
always_apply: false
---

# Global Company Intelligence

单文件整合版入口。适合不启用多 agent、但仍希望沿用同一套证据规则和报告模板的场景。

## Use When
- 用户只想要单次完整尽调，不打算显式调度多个子 agent
- 需要一份统一报告，但仍要保留证据边界和降级表达

## Workflow
1. 先说明检索日期、范围、司法辖区、是否使用付费源、关键限制。
2. 依次核验主体、数字足迹、关键人、项目真实性、贸易可见度、风险/IP、话题切口。
3. 对高风险字段严格使用共用标签和证据等级。
4. 按最终报告模板输出，并保留“冲突与缺口”。

## Canonical References
- 共用证据规则：`references/evidence-rules.md`
- 编排与审查门槛：`references/workflow.md`
- 最终报告模板：`templates/master-report-template.md`

## Hard Rules
- 营收、付款习惯、产能、完整海关清单、私人联系方式、项目落地状态等字段，证据不足时不得写成确定事实。
- 官网宣传、项目案例页、效果图、销售材料默认不能单独证明项目已落地。
- 私人联系方式默认只能作为敏感线索，轻易不可直接使用。
