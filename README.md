# Global Company Intelligence

多 agent 企业尽调技能仓库。目标是把“主体核验、关键人识别、项目真实性、海关供应链、风险/IP、对话切口”拆成可审查的独立模块，再由总控 agent 汇总成最终报告。

## Structure
- [company-intel-orchestrator/SKILL.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/company-intel-orchestrator/SKILL.md): 总控、分发、审查、汇总
- [entity-digital-verifier/SKILL.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/entity-digital-verifier/SKILL.md): 主体、官网、域名、地图、经营痕迹
- [people-contact-mapper/SKILL.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/people-contact-mapper/SKILL.md): 决策链、公开商务渠道、敏感联系线索
- [project-reality-checker/SKILL.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/project-reality-checker/SKILL.md): 项目真实性与交付状态
- [trade-supply-analyst/SKILL.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/trade-supply-analyst/SKILL.md): 海关、贸易、供应链结构
- [risk-ip-hook-strategist/SKILL.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/risk-ip-hook-strategist/SKILL.md): IP、法律风险、业务话题切口
- [templates/master-report-template.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/templates/master-report-template.md): 最终报告模板
- [references/evidence-rules.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/references/evidence-rules.md): 统一证据标签、等级、敏感信息边界
- [references/workflow.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/references/workflow.md): 推荐编排顺序、审查门槛、仓库约定
- [global-company-intelligence-optimized.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/global-company-intelligence-optimized.md): 单文件整合版入口

## Recommended Flow
1. `company-intel-orchestrator` 接收任务，确定国家、时间窗、优先问题。
2. `entity-digital-verifier` 先确认主体和官网，避免后续同名误认。
3. `people-contact-mapper` 在已确认主体上找关键人和联系路径。
4. `project-reality-checker` 核验项目是否只是宣传、概念或真实交付。
5. `trade-supply-analyst` 判断贸易可见度、供应链结构和同类供应商线索。
6. `risk-ip-hook-strategist` 做风险排查，并从公开业务信息提炼对话切口。
7. `company-intel-orchestrator` 按模板汇总，保留冲突与缺口。

## Shared Standards
- 所有 agent 共用 [references/evidence-rules.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/references/evidence-rules.md)。
- 最终报告统一按 [templates/master-report-template.md](/Users/chingchingsze/Documents/Codex/2026-05-26/agent-skill-markdown-name-global-company/templates/master-report-template.md) 输出。
- 项目落地、私人联系方式、海关金额、营收、付款习惯、产能等高风险字段必须降级表达，不能补猜。

## Repo Conventions
- `SKILL.md` 只保留本职流程和边界，不重复大段共用规则。
- 共用规则和模板放 `references/`、`templates/`。
- 若增加行业专用 agent，优先复用证据规则，不要各写一套标签体系。
