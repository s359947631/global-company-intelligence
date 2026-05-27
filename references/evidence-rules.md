# Evidence Rules

## Fact Labels
- `[FACT]`: 可由高质量来源直接支持
- `[INFERENCE]`: 基于多条事实的合理推断
- `[CLAIM ONLY]`: 仅企业自述或营销材料宣称
- `[NOT FOUND]`: 未检索到公开证据
- `[NOT VERIFIED]`: 有信息但不足以确认
- `[PAID SOURCE REQUIRED]`: 公开源通常不够，需要付费库或线下核验
- `[SOURCE MISSING]`: 无法回到原始出处

## Evidence Grades
- `A`: 官方登记、政府公告、监管文件、法院文书、业主/总包正式披露
- `B`: 官网、官方社媒、官方文件、权威数据库、可回链主流媒体
- `C`: 行业目录、招聘站、地图标注、第三方聚合站、展会页
- `D`: 二手转载、论坛转述、不可回链内容

## High-Risk Fields
以下字段默认高风险，证据不足时必须降级：
- 营收、付款习惯、信用水平、真实产能
- 完整海关清单、年度进口额、完整产品流向
- 私人邮箱、手机号、WhatsApp 可直接使用性
- 项目是否已落地、已交付、在运营

## Contact Rules
- 只记录公开、合法来源的信息。
- 公开商务渠道优先于私人联系线索。
- 私人邮箱、手机号、WhatsApp、个人社媒未交叉验证时不得写成“已确认有效联系方式”。
- 敏感线索默认标注“轻易不可直接使用，优先经官方渠道旁证”。

### Contact Verification Levels
- `L1`: 单一公开来源
- `L2`: 两个独立公开来源一致
- `L3`: 与官网、公司文件、展会资料或权威职业主页形成闭环

## Project Reality Rules
- 证据等级低于 `B`，不得写“已落地”“已交付”“在运营”。
- 官网案例、宣传册、效果图、销售材料、转发新闻，不等于独立交付证明。
- 项目状态建议使用：
  - `[CLAIM ONLY]`
  - `[CONCEPT ONLY]`
  - `[BIDDING/STUDY]`
  - `[UNDER CONSTRUCTION]`
  - `[DELIVERED]`
  - `[HISTORICAL]`

## Trade Rules
- 若只有零散贸易记录，不得包装成完整供应链画像。
- HS 近似品类不能自动等同于完全同类产品。
- 无可靠贸易源时必须写 `[PAID SOURCE REQUIRED]`。

## Conversation Hook Rules
- 仅收集公开、合法、与业务相关的话题。
- 可围绕交付周期、认证合规、供应链、本地化、扩张、项目难点设计提问钩子。
- 不得收集或输出家庭、婚姻、住址、宗教、政治、健康、非公开偏好等内容。
