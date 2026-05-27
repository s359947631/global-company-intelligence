# Workflow

## Orchestration Order
1. 确认调查对象、国家/地区、时间窗、优先问题。
2. 先跑主体核验，再跑联系人和项目，避免同名误判。
3. 海关、风险、话题切口基于已确认主体与项目事实继续展开。
4. 最终由 orchestrator 统一审查、降级和汇总。

## Review Gates
- 不得把子 agent 的推断提升为事实。
- 不得把企业自述项目自动写成已落地。
- 不得把未经交叉验证的私人联系方式写成可直接使用。
- 不得把零散贸易记录写成完整供应链结论。
- 若结论冲突，进入“冲突与缺口”，并降级为 `[NOT VERIFIED]`。
- 若关键字段缺失，明确写 `[NOT FOUND]` 或 `[PAID SOURCE REQUIRED]`。

## Expected Sub-Agent Output
各 agent 应尽量只交付本域结构化结果：

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

## Repository Guidance
- `SKILL.md` 保持短小，主要写本职边界、流程、输出格式。
- 大段通用规则放 `references/`，最终模板放 `templates/`。
- 若增加新 agent，先判断能否复用现有证据标签与模板，而不是复制粘贴一整份总规则。
