---
name: daily-video-account-planning
description: Plan, draft, publish, and archive lead-generation content for the Guangzhou Xiaozhang Finance & Tax WeChat Video Account. Use when users collect competitor copy, request topic options, confirm a topic, request copywriting, report publication, or request archive.
---

# 视频号内容工作流入口

账号服务广州本地创业者、中小微企业与经营者，以公司注册、代理记账和企业基础财税服务获客为核心。内容必须落到真实经营场景，能自然承接公司注册、代理记账或基础财税咨询；不为播放量偏离获客目标。

本技能只负责路由。按用户当前动作读取对应模块，不重复模块细节：

| 用户动作 | 必读模块 | 结果 |
| --- | --- | --- |
| 独立录入灵感：提供图片或文字 | [灵感采集](references/idea-intake-workflow.md) | 仅建立一篇灵感笔记后结束 |
| 要求选题，或要求给几个方向 | [知识库读取说明](references/obsidian-history-vault.md) + [选题流程](references/topic-selection-workflow.md) | 输出 5 个可选方案 |
| 确认选题后要求写文案 | [原始文案生成指南](references/original-copywriting-guide.md) | 生成并检查文案 |
| 说明内容已发布，或要求归档 | [发布与归档流程](references/publish-and-archive-workflow.md) + `内容库/00-首页与维护规则/历史内容归档规范.md` | 预览或执行归档与回流 |

## 全局边界

- 灵感录入是独立流程：只建立单条灵感笔记，不自动触发选题、候选入池、文案生成或归档。用户提供图片时，只提取可读文字写入笔记，不保存、嵌入或链接图片。
- 不调用热点 API，不把平台热度、排名或跨平台出现次数作为选题依据。
- 不按早、中、晚安排内容。每次选题均由用户需求触发，统一提供 5 个互不重复的方案。
- 历史内容库是已发布内容、去重和覆盖判断的唯一事实来源；灵感库与选题池是候选资产，不替代历史库。
- 用户只确认选题或文案时，不写入历史内容库。只有“实际发布”与“明确归档/写入”两个条件同时满足时，才能归档。
- 政策、税率、期限、处罚、平台规则和办理流程等确定性结论，必须核验当前官方来源。
- 不编造政策、案例、数据或处罚结果；不夸大风险、承诺结果或传播规避监管方法。
