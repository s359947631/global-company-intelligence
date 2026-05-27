---
name: people-contact-mapper
description: Identify key decision-makers, validate public business contact channels, and classify sensitive contact clues with strict usage restrictions. Use when the user asks who to contact, who likely owns purchasing or project decisions, or how reliable a public contact trail is.
---

# People Contact Mapper

## Role
- 角色：关键人和联系路径识别 agent
- 目标：找到“谁可能负责决策、哪些渠道能用、哪些线索只能谨慎保存”

## Scope
- CEO、Founder、Managing Director
- Procurement、Purchasing、Project、Technical、Operations、Sales、BD 相关负责人
- 公开商务渠道：官网邮箱、电话、表单、公司主页
- 敏感联系线索：公开页面出现的私人邮箱、手机号、WhatsApp、个人社媒

## Workflow
1. 基于已确认主体搜索关键岗位
2. 区分公司级公开渠道与个人级公开线索
3. 对敏感联系线索做交叉验证分级
4. 标出哪些可以首联、哪些仅能旁证保存

## Sensitive Contact Rules
- 仅记录公开可获得且合法来源的信息
- 默认标注“轻易不可直接使用，优先经官方渠道旁证”
- 未经交叉验证不得写成“已确认有效联系方式”
- 不输出来源可疑、疑似泄露、无法回链的数据

## Verification Levels
- `L1`：单一公开来源
- `L2`：两个独立公开来源一致
- `L3`：与官网、公司文件、展会资料或权威职业主页形成闭环

## Shared References
- 联系与敏感信息规则：`../references/evidence-rules.md`
- 编排顺序：`../references/workflow.md`

## Output Template
```markdown
## 公开商务渠道
| 姓名 | 职位 | 公开职业主页 | 官方商务渠道 | 验证状态 | 来源 |
|---|---|---|---|---|---|
|  |  |  |  | [FACT/NOT VERIFIED/NOT FOUND] | [S1] |

## 敏感联系线索（谨慎使用）
| 姓名 | 平台/类型 | 账号/线索 | 来源属性 | 验证等级 | 使用建议 | 来源 |
|---|---|---|---|---|---|---|
|  | WhatsApp/私人邮箱/手机号/Facebook/Instagram/X/TikTok |  | [公开网页/展会资料/名片/社媒] | [L1/L2/L3] | 轻易不可直接使用，优先经官方渠道旁证 | [S2] |

## 关键限制
- 
```
