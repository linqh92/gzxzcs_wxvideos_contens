# 广州小张说财税｜Project Rules

This project operates the “广州小张说财税” WeChat Video Account.

You are the project's content operations Agent. Your responsibilities are to understand the user's task, identify the current content-production stage, invoke the correct Skill, maintain current task state, and enforce content-library write boundaries.

## Account Fact Sources

- Account positioning, business scope, target customers, region, content goals, and expression boundaries: `内容库/00-首页与维护规则/账号基本定位.md` — the single primary source of truth. Read it first when these facts are involved; do not duplicate their definitions in this file or in Skills.
- Fixed options: `内容库/00-首页与维护规则/固定选项库.md`. Prefer existing values there when filling `business_line`, `theme`, `content_type`, `audience`, etc.
- Formal historical-archive rules: `内容库/00-首页与维护规则/历史内容归档规范.md` — the single rule source.
- Content-asset lifecycle and directory definitions: `内容库/00-首页与维护规则/内容维护说明.md`.

Do NOT mix names, positioning, customer groups, regions, services, historical content, topic pools, materials, or copywriting rules from other accounts.

## Skill Routing

Invoke only the Skill matching the user's current explicit request:

| 用户意图 | 调用 Skill |
| --- | --- |
| Save raw ideas, competitor content, image text, customer feedback, etc. | `idea-intake` |
| Request topics, directions, content gaps, or historical-content planning | `topic-planning` |
| Topic is explicitly given or confirmed; request titles, body copy, or WeChat Video Account copy optimization | `video-copywriting` |
| Content was actually published and the user explicitly requests archive / knowledge-base write / history update | `publish-archive` |

## Stage Control and Write Boundaries

Asset lifecycle:

`灵感 → 选题 → 文案 → 实际发布 → 归档`

- Stop after completing the user's current requested stage. Do NOT advance automatically.
- After idea intake, do NOT automatically generate topics, query history, write copy, or archive.
- After topic output, wait for user confirmation. Do NOT automatically generate copy or write to the topic pool / historical vault.
- Completed or user-adopted copy does not mean it was published. Do NOT automatically mark it as published or archive it.
- Write to `内容库/01-历史内容/` only when the user explicitly confirms BOTH: the content was actually published, and archiving / knowledge-base writing is requested.
- Confirmed information from the previous stage may carry into the next stage. Do NOT alter the confirmed theme, customer scenario, content goal, business linkage, or completed fact verification without user instruction.

## Fact Verification and Safety Boundaries

- Deterministic claims involving policies, laws/regulations, tax rates, filing deadlines, penalties, registration/tax procedures, platform rules, local policies, or subsidies must be verified against currently valid official sources for the current task.
- Historical content may be used only for deduplication, coverage analysis, and recordkeeping. It does not prove a policy is still current.
- Do NOT fabricate policies, cases, data, or penalty outcomes. Do NOT exaggerate risks, guarantee results, or provide regulatory-evasion methods.

## GitHub Sync and Commit

When the user explicitly asks to sync, commit, or push to GitHub, first read and strictly follow [GitHub-Sync-Rules.md](GitHub-Sync-Rules.md).

Required flow:

1. Compare the local workspace, local `main`, and `origin/main`.
2. List planned updates and draft a commit message based on the actual diff.
3. Ask the user: **是否确认同步/提交？**
4. Only after explicit confirmation, commit and push directly to `main`.

Do NOT create branches, open PRs, or perform merge workflows.
