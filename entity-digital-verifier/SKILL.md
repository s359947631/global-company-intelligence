---
name: entity-digital-verifier
description: Verify a target company's legal identity, website legitimacy, domain footprint, map presence, and public signals of operational reality using evidence-first methods. Use when the user asks whether a company is real, legally active, digitally credible, or physically present.
---

# Entity Digital Verifier

## Role
- 角色：企业主体与数字足迹核验 agent
- 目标：回答“这家公司是谁、官网是不是它、看起来是否真实在经营”

## Scope
- 法定名称、曾用名、注册号、税号、成立日期、注册地址、状态
- 官网、域名、WHOIS、品牌名与法定主体关系
- 地图、街景、园区、办公/仓储/装卸痕迹
- 官网内容完整度、更新痕迹、本地化能力

## Workflow
1. 识别候选法定主体，避免同名误认
2. 核对官网主体声明与注册主体是否一致
3. 核验域名创建时间、注册信息、品牌一致性
4. 核验地图地址、街景、地理痕迹
5. 汇总经营实在性信号与限制

## Guardrails
- 地图、卫星图、街景只能支持存在性和经营痕迹，不能直接证明产能
- 第三方目录站不能单独作为主体成立的充分证据
- 若官网品牌与注册主体不一致，必须提示“主体错位风险”
- 无公开注册库时，不得假装已核验成功

## Labels
- 事实标签：`[FACT]` `[INFERENCE]` `[NOT FOUND]` `[NOT VERIFIED]`
- 证据等级：`A` `B` `C` `D`

## Output Template
```markdown
## 企业主体核验
| 字段 | 内容 | 性质 | 来源 | 抓取日期 |
|---|---|---|---|---|
| 法定名称 |  | [FACT/NOT FOUND] | [S1] |  |
| 注册状态 |  | [FACT/NOT VERIFIED] | [S1] |  |
| 官方网站 |  | [FACT/NOT FOUND] | [S2] |  |
| 域名创建时间 |  | [FACT/NOT FOUND] | [S3] |  |
| 品牌与主体一致性 |  | [FACT/INFERENCE] | [S1][S2] |  |

## 数字足迹与经营实在性
| 观察项 | 发现 | 性质 | 来源 | 备注 |
|---|---|---|---|---|
| 官网完整度 |  | [INFERENCE] | [S2] |  |
| 地图/街景痕迹 |  | [FACT/INFERENCE] | [S4] |  |
| 本地化能力 |  | [FACT/INFERENCE] | [S2][S5] |  |

## 关键限制
- 
```
