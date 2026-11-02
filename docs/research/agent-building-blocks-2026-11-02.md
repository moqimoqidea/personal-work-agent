# 构建附录：通用 Agent 运行时与组件

本轮活动监测：**2026-11-02（Asia/Shanghai）**。返回[修订主报告](personal-agent-landscape-2026-11-02.md)。能力与许可说明沿用 10 月 22 日固定来源；本轮 HEAD、发行渠道与选型影响见第 5 节。未重新安装或运行组件。

本附录保存实现背景，不进入商业个人 Agent 的直接替代主表。判断对标关系应看用户拿到的产品、任务闭环与依赖范围；不能因为项目有 memory、cron 或 tools，就与 Muse、Grok Bot、Dots、Duet 并列。

## 1. 通用个人 Agent 运行时

这些项目部分也有完整应用或渠道入口，具有独立价值；但本轮重点是明确复刻或对位特定商业个人 Agent 的应用，因此将它们放在实现资料层。

| 项目 | 可研究的实现问题 | 与本轮直接对标应用的区别 | 已核验来源 |
| --- | --- | --- | --- |
| OpenClaw | 多渠道 Gateway、工具、插件、设备节点与执行隔离 | 是较通用的个人助理运行体系；本轮优先研究 OpenMuse/OpenGrokBot 的产品组合 | [固定 README](https://github.com/openclaw/openclaw/blob/92be346dfcab87bcca34ac232d5a0793fc3b8da0/README.md) |
| Hermes Agent | 长期记忆、历史检索、从工作经验形成 Skills、调度 | 适合运行与学习机制研究，不能替代 Muse/Grok Bot 的逐项产品对比 | [固定 README](https://github.com/NousResearch/hermes-agent/blob/81a55437f3f31a9f12a30c53b6c5d49d420898aa/README.md) |
| NanoClaw | 每 Agent 容器、按需渠道、可定制 fork | 主要参考执行隔离与定制方式，不把容器运行时等同完整商业体验 | [固定 README](https://github.com/nanocoai/nanoclaw/blob/0be4e941a842f63c8cd737c74ef18e52f13dee9c/README.md) |
| nanobot | Python 核心、消息入口、记忆、调度、MCP、API | 适合原型和内部机制实验；主分支与稳定包能力需分开 | [固定 README](https://github.com/HKUDS/nanobot/blob/be43d2a5f8bfd01cec31f5d6508d68acfc1d34be/README.md) |
| QwenPaw（原 CoPaw 路径） | 中文渠道、本地模型、ReMe、插件和工作空间 | 作为中文部署与集成的补充研究，不自动视为 Today/Muse 的同等复刻 | [固定 README](https://github.com/agentscope-ai/QwenPaw/blob/0db9a8e625e73917a0d113e255b3147134022db8/README.md) |
| Letta Code | 有状态 Agent、可演化记忆、MemFS、Skills 与持续工作 | 用于研究个人身份和记忆实现；应使用当前仓库而非旧 V1 server | [固定 README](https://github.com/letta-ai/letta-code/blob/035bb8c8917b5dd94a3989d4adf04860a2ce8fea/README.md) |

## 2. 单层组件与应用构建平台

| 项目 | 所在层 | 不能直接替代什么 | 许可 / 来源 |
| --- | --- | --- | --- |
| LangGraph | 持久执行、状态、检查点、人类介入 | 个人助理成品的客户端、身份、设备、应用授权、通知和运维 | MIT；[固定 README](https://github.com/langchain-ai/langgraph/blob/3cd57c038ad827d05f80c6488adea9994156c58c/README.md) |
| Mem0 | 长期记忆提取与检索 | 完整任务协调、执行电脑和用户产品 | Apache-2.0；[固定 README](https://github.com/mem0ai/mem0/blob/2c81af3bbe27d9bccb09c772d583df9e9be72ee5/README.md) |
| Browser Use | 浏览器执行 | 持续个人身份、记忆、目标、通知与授权体系 | MIT；[固定 README](https://github.com/browser-use/browser-use/blob/aa093a843da5edbf323c0b4145c9b6a0db3ecde8/README.md) |
| n8n | 集成、事件管道、可视化工作流与 Agent 编排 | 个人关系层和商业个人 Agent 的完整连续体验 | Sustainable Use / Enterprise；[README](https://github.com/n8n-io/n8n/blob/d85f857823167d395266ec6bb9b3ad00ed070054/README.md)、[许可](https://github.com/n8n-io/n8n/blob/d85f857823167d395266ec6bb9b3ad00ed070054/LICENSE.md) |
| Dify | Agent、RAG、工作流与应用构建 | 一个已经组合好个人记忆、电脑、主动性与设备的助理成品 | 修改版 Apache-2.0；[README](https://github.com/langgenius/dify/blob/405c39692da2e1bd7945290ee8f3a310e6a9438a/README.md)、[许可](https://github.com/langgenius/dify/blob/405c39692da2e1bd7945290ee8f3a310e6a9438a/LICENSE) |

Mem0 的托管基准包含开源 SDK 没有的优化，不能套用为本地安装成绩。n8n 和 Dify 的许可也不能无条件视为与标准 MIT 项目相同；按具体交付方式复查原文。

## 3. 命中产品名也可能属于其他类型

[Shashankss1205/OpenDots](https://github.com/Shashankss1205/OpenDots/blob/de37e7445418ace9862daf33b7ac7014064790de/README.md) 提供目标、事件、heartbeat、项目文件编辑与检查，可通过 CLI、API 或本地模型运行。其主要使用方式围绕自己的项目目录与编码工作，不按名称就视为 OpenAI Dots 的通用个人助理复刻。

同样，提示词合集、awesome 清单、模型绑定工具、共享 Claude Code 会话的工具，都不能替代一款个人 Agent 应用。发现工具与识别同类产品是不同步骤。

## 4. 何时再回到这些组件

先选择主报告中的同类产品，走通“请求—持续工作—审批—结果—后续更新”。当具体产品缺少一层能力时，再评估是否用这里的组件补充。这样才能知道是在修补明确短板，还是无意中重造一整套产品。

## 5. 本轮动态与采用边界

查询 11 个组件的 metadata、默认分支 HEAD 与 Releases 前五项；除 NanoClaw 外，10 个 HEAD 前进。时间是 **UTC**。下表是活动监测；第 1、2 节的能力与许可仍引用 10 月 22 日固定来源，没有替换成未审过的新版本保证。

| 仓库 | 基线固定 SHA | 本次固定 SHA | 提交时间（UTC） | 本次范围 |
| --- | --- | --- | --- | --- |
| openclaw/openclaw | [b4cc6fe87a18](https://github.com/openclaw/openclaw/tree/b4cc6fe87a18220ac11a0a3377b0a3ef43cf2093) | [2777468d26e5](https://github.com/openclaw/openclaw/tree/2777468d26e5f21455b67591a045a40c770aee13) | 2026-11-02 09:17:48 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| NousResearch/hermes-agent | [aad60e1ac670](https://github.com/NousResearch/hermes-agent/tree/aad60e1ac670268aa39b364b16b16dbf06de85df) | [b425edd28617](https://github.com/NousResearch/hermes-agent/tree/b425edd286179eaa2419ca13f9cbf6706845e8ab) | 2026-11-02 09:09:07 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| nanocoai/nanoclaw | [acc2b1c8f52a](https://github.com/nanocoai/nanoclaw/tree/acc2b1c8f52a954368cfaf04b61c32f9a1efc280) | [acc2b1c8f52a](https://github.com/nanocoai/nanoclaw/tree/acc2b1c8f52a954368cfaf04b61c32f9a1efc280) | 2026-10-26 07:00:31 | HEAD 相同；HEAD + Releases 前五项，能力/许可沿用历史 |
| HKUDS/nanobot | [b07b3eac244f](https://github.com/HKUDS/nanobot/tree/b07b3eac244ff7faa7eeb2d4777fe54dbae1b6d2) | [8b37976d36c2](https://github.com/HKUDS/nanobot/tree/8b37976d36c2812c62b464321e729a88872b60f9) | 2026-10-31 03:55:13 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| agentscope-ai/QwenPaw | [9e59502cbe3b](https://github.com/agentscope-ai/QwenPaw/tree/9e59502cbe3b62e9a962027cfa6c549936c89135) | [d09c34f6c4be](https://github.com/agentscope-ai/QwenPaw/tree/d09c34f6c4be3939931c90f2623ae3cbc93c6cc4) | 2026-11-02 09:10:41 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| letta-ai/letta-code | [5dea67021b99](https://github.com/letta-ai/letta-code/tree/5dea67021b99810707ff753db35e4534f70ff1fd) | [6155d9f562f1](https://github.com/letta-ai/letta-code/tree/6155d9f562f13eb1f352240a7fd07a87933ac76a) | 2026-11-02 06:58:30 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| langchain-ai/langgraph | [eb8ec111b3e9](https://github.com/langchain-ai/langgraph/tree/eb8ec111b3e9d3108af5d7bdcac51e3e913637a0) | [ee3c043bddcc](https://github.com/langchain-ai/langgraph/tree/ee3c043bddcc514012885167dd5916b15d6e4731) | 2026-11-02 04:33:29 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| mem0ai/mem0 | [26cdefb46600](https://github.com/mem0ai/mem0/tree/26cdefb46600c0fa5953c4b5ee5003c125539fc4) | [753496cf1435](https://github.com/mem0ai/mem0/tree/753496cf1435d76c3a711f3af51303f7fdcb6420) | 2026-10-30 21:35:34 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| browser-use/browser-use | [2cc71890e650](https://github.com/browser-use/browser-use/tree/2cc71890e65056b67fdb29d98bb407749c15bb08) | [b49a68e4060a](https://github.com/browser-use/browser-use/tree/b49a68e4060acb226da8f784194fef301c53a6d7) | 2026-10-30 04:28:48 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| n8n-io/n8n | [dd5f870ecc38](https://github.com/n8n-io/n8n/tree/dd5f870ecc38344951fb3956f1a7ba7852612c70) | [db28d8b94db4](https://github.com/n8n-io/n8n/tree/db28d8b94db48cc0b2c137fb94a76c592b8a3047) | 2026-11-02 08:58:30 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |
| langgenius/dify | [c01cb5d119a6](https://github.com/langgenius/dify/tree/c01cb5d119a69532df73ec20da8daa18cf44e0fb) | [8c5e2efb9966](https://github.com/langgenius/dify/tree/8c5e2efb996617da715677cd6d621b5ba15c250e) | 2026-11-02 08:54:45 | HEAD 前进；HEAD + Releases 前五项，能力/许可沿用历史 |

| 对象 | 本轮发行观察 | 对采用的影响 |
| --- | --- | --- |
| OpenClaw | [U66 稳定 v2026.10.9](https://github.com/openclaw/openclaw/releases/tag/v2026.10.9)，10 月 29 日 15:54:35 UTC；[U67 beta.5](https://github.com/openclaw/openclaw/releases/tag/v2026.10.10-beta.5)，10 月 30 日 03:57:14 UTC，prerelease=true | 稳定摘要涉及工作区约束、凭据、数据恢复与升级回滚；beta 摘要含 Node 兼容、流式及 cron 恢复。只读 Highlights/相关摘要，未核验所有修复或安装分发；不能以 beta 首项覆盖稳定渠道 |
| Hermes / NanoClaw | Hermes 首项仍 v0.22.5；NanoClaw 首项 rc.2、前五项含稳定 v2026.10.0，且 HEAD 未变 | 只复查元数据，不把旧版本重新算本期发布；主分支、rc 和稳定包分开 |
| nanobot | [U68 v0.4.0](https://github.com/HKUDS/nanobot/releases/tag/v0.4.0)，10 月 28 日 10:50:17 UTC，晚于基线报告提交 | Highlights 描述 SQLite 历史导入、更新确认、安装归属与恢复。大幅改动持久历史时应验收迁移与当前数据保留，不能由维护者说明推断已无丢失；未遍历长清单或验证 PyPI |
| QwenPaw | [U70 v2.3.0-beta.2](https://github.com/agentscope-ai/QwenPaw/releases/tag/v2.3.0-beta.2)，11 月 2 日 06:08:12 UTC，预发行 | 前部说明涉及插件、技能、媒体与模型启动；只作 beta 观察，不据新 HEAD 称稳定能力已经升级 |
| Letta Code | [U71 v0.34.38](https://github.com/letta-ai/letta-code/releases/tag/v0.34.38)，11 月 2 日 07:09:09 UTC | 说明全文涉及子任务进度输出与完整 JSONL 日志，适合作为任务可观察性参照；没有运行对照 |
| LangGraph | [U69 1.2.19](https://github.com/langchain-ai/langgraph/releases/tag/1.2.19)，10 月 30 日 22:23:43 UTC；同页列表另有 SDK/checkpoint-sqlite 标签 | 说明涉及流事件 namespace、暂停工具和 awaited task 返回；不能将不同子包版本号混用。首次 API 连接错误重试已成功 |
| Mem0 / Browser Use / Dify | Releases 前五项首项分别仍 v2.2.1、0.13.14、1.18.0 | 仅发行元数据与 HEAD；旧功能、托管基准、Python/Pi 分界和许可不重新盖日期 |
| n8n | 前五项同时有 1.123.92 稳定维护线、2.46.4 预发行、stable 别名和 2.45.7 非预发行 | 不能按列表首项或别名选定升级目标；本轮没有读取全部发行说明和重审 Sustainable Use/Enterprise 许可 |

## 6. 与应用选型同步的边界

- **本地执行不是一个统一能力。** OpenGrokBot v0.4.0 的 Linux 命令参数与安全文有静态差异；采用前先用临时资料验证，不能仅凭有 Seatbelt/bubblewrap 就认定两平台密钥隔离等价。见主报告 U47/U48 与 E08。
- **预算须按引擎确定。** nanoMuse 1.0.9 的预算只适用 Python runtime/Python hands，不覆盖原生 Android 和桌面聊天引擎，也不保证第三方账单封顶。见 U52/U53 与 E10。
- **应用模板仍有外部基础。** 新增 OpenDuet 是应用层参照，依赖仓内 OpenBot、Intelligence、模型和连接服务；不把应用 MIT 许可扩展为所有依赖许可。
- **Perplexity fully local 是商业执行路径。** 官方正文给出 Apple silicon、订阅与建议内存条件，也允许授权转云；它不属于本表的开源组件。见 U39。
- **执行模型与主协调模型分开。** OpenAI [10 月 26–30 日周页](https://learn.chatgpt.com/docs/whats-new/october-26-30-2026)本次重读仍将 Terra 用于 Work/Codex；Dots 主页仍描述 GPT-6 Astra，不能相互替换。

先验收主报告的应用闭环，再决定是否替换运行时、记忆或浏览器层。所有发行与源码观察均未执行部署、账号或端到端实验。完整证据、查询范围和失败替代入口见[本轮来源索引](sources-2026-11-02.md)。
