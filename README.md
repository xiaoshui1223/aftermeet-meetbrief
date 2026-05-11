# AfterMeet MeetBrief｜会后有数

高效制定会议纪要，沉淀复用会议资产。

把没人想重看的会议回放，整理成可检索、可复用的知识资产。

AfterMeet MeetBrief is an Agent-native Skill for Feishu/Lark meeting workflows. It does more than summarize transcripts: it classifies the meeting type, previews the writing strategy, captures key visual moments, and turns long meetings into structured briefs with mind maps, screenshots, knowledge cards, speaker insights, quotes, and action guides.

It is built for meetings where the screen matters: courses, live sessions, product demos, tool walkthroughs, interviews, project reviews, competition briefings, and team syncs. Instead of asking people to rewatch long recordings, AfterMeet MeetBrief helps teams keep the parts that are actually worth reusing.

如果这个 Skill 对你有帮助，欢迎点个 Star。

## 核心能力｜What It Does

- 会议类型识别：先判断这场会议属于分享、课程、比赛动员、项目推进、方案评审等哪一类。
- 成稿策略预览：正式生成前，先给用户看会议类型、文档结构、截图数量区间、金句数量和清理策略。
- 关键画面捕捉：优先通过浏览器捕捉飞书妙记里的重点画面、投屏演示、工具界面和关键截图。
- 图文同步沉淀：把截图时间点附近的逐字稿/字幕内容一起读完，整理成对应的概念解释、讲解要点和操作步骤。
- 结构化文档生成：把长会议整理成思维导图、会议概览、核心观点、知识卡片、嘉宾观点、金句和行动指南。
- 飞书文档沉淀：将结果写回飞书文档，方便团队复盘、分享、归档和二次查阅。
- 本地素材清理：任务结束后询问用户是清理、保留，还是继续修改本次任务产生的临时素材。

## 适用场景｜Supported Meeting Scenarios

| 中文场景 | English Scenario | 适合沉淀的内容 |
| --- | --- | --- |
| 嘉宾分享 / 主题分享 | Guest Sharing / Theme Talk | 观点拆解、案例、金句、嘉宾观点 |
| 播客 / 访谈 | Podcast / Interview | 话题地图、对谈观点、人物表达、关键句 |
| 训练营 / 课程回放 | Training Camp / Course Replay | 学习路径、步骤截图、作业要求、练习指南 |
| 比赛动员 / 活动宣讲 | Competition Mobilization / Event Briefing | 时间节点、奖金权益、提交方式、参赛清单 |
| 产品演示 / 工具实操 | Product Demo / Tool Practice | 操作路径、界面截图、步骤说明、注意事项 |
| 项目推进 / 待办同步 | Project Progress / Task Sync | 决策、负责人、截止时间、风险和阻塞 |
| 工作汇报 / 阶段复盘 | Work Report / Stage Review | 阶段成果、关键数据、问题原因、下一步计划 |
| 需求讨论 / 方案评审 | Requirement Discussion / Solution Review | 方案对比、判断标准、结论、后续跟进 |

## 产出内容｜Output Assets

AfterMeet MeetBrief 目前会优先产出这些内容：

- 会议类型判断与成稿策略
- 思维导图式结构梳理
- 会议概览与最值得记住的结论
- 重点画面、投屏演示和关键截图
- 核心观点拆解与知识卡片
- 嘉宾观点与金句整理
- 行动指南与后续待办
- 可写回飞书文档的图文版会议资产

## 适合谁用｜Who It Is For

AfterMeet MeetBrief 适合已经在使用 AI 编程工具或 Agent 工具的人，例如：

- Codex 用户
- Claude Code 用户
- Cursor 用户
- 经常开飞书会议、直播课、训练营、访谈、项目会和复盘会的团队
- 想把会议内容从“看完就散”变成“可检索、可复用、可分享资产”的创作者和工作流搭建者

## 安装要求｜Requirements

使用前需要准备：

- `lark-cli`
- 飞书 / Lark CLI Skills
- 可读取飞书妙记、会议纪要，并写入飞书文档的授权
- 支持浏览器自动化的 AI Agent 环境，用于捕捉会议中的关键画面

Skill 会在运行前检查依赖和授权。如果缺少飞书 CLI、相关 Skills 或权限，它会先说明用途，再询问是否安装、升级或授权。

## 安装方式｜Install

如果你的 AI Agent 支持 Skill 安装，可以直接安装：

```bash
npx skills add https://github.com/XshuiAi/aftermeet-meetbrief -g -y
```

如果还没有安装飞书 CLI：

```bash
npm install -g @larksuite/cli
npx skills add larksuite/cli -g -y
```

如果还没有登录飞书 CLI：

```bash
lark-cli auth login
```

## 使用方式｜Usage

把飞书会议或妙记链接发给你的 AI Agent，然后这样说：

```text
使用 AfterMeet MeetBrief（会后有数），把这个飞书妙记链接整理成一份结构化图文会后文档：
https://example.feishu.cn/minutes/xxxx
```

AfterMeet MeetBrief 会先给出一份生成策略，包括：

- 这场会议判断为什么类型
- 推荐使用精简版还是详细版
- 预计保留多少张关键截图
- 预计整理多少条嘉宾观点或金句
- 文档会包含哪些模块
- 本次任务产生的本地临时素材如何处理

你确认方案后，它再开始正式生成文档。

## 仓库结构｜Repository Layout

```text
aftermeet-meetbrief/
├── README.md
├── skills/
│   └── aftermeet-meetbrief/
│       ├── SKILL.md
│       ├── agents/openai.yaml
│       └── references/
├── examples/
│   └── mini-camp/
└── docs/public/
```

私有过程文档、内部规则和未来方向不会放进公开仓库，默认保留在本地并被 Git 忽略。

## 作者｜Creator

Created by 小水。

我是一个 AI 创作者和工作流构建者，关注如何让 AI 工具真正进入实际工作：内容生产、会议工作流、飞书自动化，以及 Agent-native Skills。

AfterMeet 是我正在构建的一个产品线，用来探索会议结束之后，如何把会议变成文档、思维导图、可沉淀的知识资产。

联系我：`xshui7726`

## 项目状态｜Status

AfterMeet MeetBrief 目前处于 MVP 开发阶段。当前重点是把飞书会议到结构化图文会后文档的流程打磨成稳定、可安装、可复用的 Skill。

## License

MIT
