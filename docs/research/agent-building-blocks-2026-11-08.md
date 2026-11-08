# 构建附录：通用 Agent 运行时与组件

本轮活动监测日期为 **2026-11-08（Asia/Shanghai）**，记录生成时间为 **2026-11-08T20:30:02+08:00**。返回[修订主报告](personal-agent-landscape-2026-11-08.md)。能力与许可说明沿用 10 月 22 日固定来源；本轮 HEAD、发行渠道与选型影响见第 5 节。未重新安装或运行组件。

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

查询 11 个组件的 metadata、默认分支 HEAD 和 Releases 前五项，10 个 HEAD 前进，Browser Use 相同。第 1、2 节能力和许可仍使用 10 月 22 日固定来源。下表属于活动监测，时间为 UTC；发行说明读取深度另列。

| 仓库 | 基线固定 SHA | 本次固定 SHA | committer 时间（UTC） | 实际范围 |
| --- | --- | --- | --- | --- |
| openclaw/openclaw | [2777468d26e5](https://github.com/openclaw/openclaw/tree/2777468d26e5f21455b67591a045a40c770aee13) | [6c983bb80229](https://github.com/openclaw/openclaw/tree/6c983bb8022904eb8ede66691341522943d3f61e) | 2026-11-08 12:10:51 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| NousResearch/hermes-agent | [b425edd28617](https://github.com/NousResearch/hermes-agent/tree/b425edd286179eaa2419ca13f9cbf6706845e8ab) | [8422e54df36f](https://github.com/NousResearch/hermes-agent/tree/8422e54df36f42371f31b8fbee653e7c801edcbd) | 2026-11-08 12:05:12 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| nanocoai/nanoclaw | [acc2b1c8f52a](https://github.com/nanocoai/nanoclaw/tree/acc2b1c8f52a954368cfaf04b61c32f9a1efc280) | [dd19240d9036](https://github.com/nanocoai/nanoclaw/tree/dd19240d9036bab13491953513cb88ec7a2980e6) | 2026-11-08 10:55:12 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| HKUDS/nanobot | [8b37976d36c2](https://github.com/HKUDS/nanobot/tree/8b37976d36c2812c62b464321e729a88872b60f9) | [1e2dc02fa228](https://github.com/HKUDS/nanobot/tree/1e2dc02fa228b6c5c62b8fc84de2a2d77dd925f3) | 2026-11-08 08:32:20 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| agentscope-ai/QwenPaw | [d09c34f6c4be](https://github.com/agentscope-ai/QwenPaw/tree/d09c34f6c4be3939931c90f2623ae3cbc93c6cc4) | [2cf28d14a20c](https://github.com/agentscope-ai/QwenPaw/tree/2cf28d14a20c9f9c769cce2a9c0568ccf84e459c) | 2026-11-06 10:38:59 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| letta-ai/letta-code | [6155d9f562f1](https://github.com/letta-ai/letta-code/tree/6155d9f562f13eb1f352240a7fd07a87933ac76a) | [64fdf5999441](https://github.com/letta-ai/letta-code/tree/64fdf5999441094a6f43f7a38a6d356519fea029) | 2026-11-08 07:40:05 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| langchain-ai/langgraph | [ee3c043bddcc](https://github.com/langchain-ai/langgraph/tree/ee3c043bddcc514012885167dd5916b15d6e4731) | [e5e37b5d70db](https://github.com/langchain-ai/langgraph/tree/e5e37b5d70dbfd93c7006bd90a658c6179a95946) | 2026-11-06 16:08:12 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| mem0ai/mem0 | [753496cf1435](https://github.com/mem0ai/mem0/tree/753496cf1435d76c3a711f3af51303f7fdcb6420) | [f1791daa86d4](https://github.com/mem0ai/mem0/tree/f1791daa86d469249c9b002f62644d58a1eb96a0) | 2026-11-06 16:53:06 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| browser-use/browser-use | [b49a68e4060a](https://github.com/browser-use/browser-use/tree/b49a68e4060acb226da8f784194fef301c53a6d7) | [b49a68e4060a](https://github.com/browser-use/browser-use/tree/b49a68e4060acb226da8f784194fef301c53a6d7) | 2026-10-30 04:28:48 | HEAD 相同；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| n8n-io/n8n | [db28d8b94db4](https://github.com/n8n-io/n8n/tree/db28d8b94db48cc0b2c137fb94a76c592b8a3047) | [01bd57cddf11](https://github.com/n8n-io/n8n/tree/01bd57cddf11e8173b16adce1b22a8eb94598672) | 2026-11-08 02:29:38 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |
| langgenius/dify | [8c5e2efb9966](https://github.com/langgenius/dify/tree/8c5e2efb996617da715677cd6d621b5ba15c250e) | [208a2489f05f](https://github.com/langgenius/dify/tree/208a2489f05f688afd701ba262a42d08289996a7) | 2026-11-08 09:39:21 | HEAD 前进；metadata、HEAD、Releases 前五项；能力/许可沿用历史 |

| 对象 | 本轮发行观察 | 对采用的影响与读取边界 |
| --- | --- | --- |
| OpenClaw | [U112 v2026.11.1](https://github.com/openclaw/openclaw/releases/tag/v2026.11.1)，11 月 5 日 09:48:37 UTC，稳定；列表另有 v2026.11.5-beta.1 | Highlights 涉及秘密配置保存、渠道回复、历史/子任务恢复、更新回滚。只读摘要与开头 Changes，未重验全部补丁；发布日和数字版本顺序分开 |
| Hermes | [U113 v0.23.0](https://github.com/NousResearch/hermes-agent/releases/tag/v0.23.0)，11 月 5 日 21:32:33 UTC | Highlights 增加 Gateway 提供 Webapp、单 Gateway 持有会话等主题；说明汇总 0.22.x，未把全部条目算本期首创，未因新 UI 将其自动改列某家产品的直接复刻 |
| NanoClaw / QwenPaw | 前五项首项分别仍 rc.2、beta.2，包含较早稳定标签；HEAD 均前进 | 本轮仅元数据，不给旧发行或许可赋新的全文核验日期 |
| nanobot | [U114 v0.4.1](https://github.com/HKUDS/nanobot/releases/tag/v0.4.1)，11 月 6 日 15:55:22 UTC | 说明全文包含 0.3.5 可直接升级、0.4.x 保留历史导入、临时 apiType 转换的最后支持版、应用内自动安装未启用。升级需按原安装渠道并验收旧数据、消息和再次重启 |
| Letta Code | [U115 v0.34.45](https://github.com/letta-ai/letta-code/releases/tag/v0.34.45)，11 月 8 日 07:49:26 UTC | 说明全文列退役默认模型改为需要密钥/额度、父 vault 刷新、MemFS 空格路径修复；未做真实凭据或模型调用 |
| LangGraph | [U116 1.2.20](https://github.com/langchain-ai/langgraph/releases/tag/1.2.20)，11 月 5 日 02:20:53 UTC；SDK/CLI 各有子包标签 | 说明全文列 interrupt 独立 ID、strict resume 拒绝过期回答。可作为审批绑定版本和重放的机制参照，实际持久状态仍需配置与验收 |
| Dify | [U117 1.19.0](https://github.com/langgenius/dify/releases/tag/1.19.0)，11 月 4 日 07:36:16 UTC | Highlights 有嵌套 Workflow Tool tracing 与 package v2，历史 traces 不回填；未读全部升级步骤，修改版 Apache 许可仍按旧固定来源 |
| n8n | [U118 2.46.6](https://github.com/n8n-io/n8n/releases/tag/n8n%402.46.6)，11 月 4 日 13:10:07 UTC；列表另有 stable 及 2.47.x 预发行 | 说明正文仅确认 npm 跨平台安装修复，未运行包安装；多维护线、别名和安装归属需分别核对 |
| Mem0 / Browser Use | 首项仍 v2.2.1 / 0.13.14；Mem0 HEAD 前进，Browser Use HEAD 相同 | 只观察元数据，保留既有 SDK/托管成绩、Python/Pi 和许可边界 |

## 6. 与应用选型同步的边界

- **应用交付分 edition 和版本。** OpenBot 已有 Personal 桌面发行，本地 Intelligence 仍有账号和评估许可。晚于 v0.3.3 的 Personal 源码关闭独立记忆，Skills 学习单独存在。主报告 U87/U91/U119 分开记录，长期记忆按 E13 验收。
- **本地文件隔离有了修复依据。** OpenSuperBot 0.5.0 在 macOS/Linux 改为整 home 遮蔽和只读工具链例外，旧版 Linux 文码差异已有静态修复。网络、系统服务、资源上限及 Windows 无本地命令另验，见 U95/U96 与 E08。
- **持久状态仍需业务结果核对。** OpenDots 的过期 claim 恢复与显式重试无法单独证明外部动作只发生一次；LangGraph strict resume 针对旧回答是另一层控制。见 U108/U109/U116 与 E14。
- **预算与 Skills 按引擎和作用域。** nanoMuse Python 预算范围继续保留，新主分支 Skills 全局/工作区关闭需覆盖 discovery/get/provider，尚未进入 1.0.9 发行承诺。见 U102/U105/U106 与 E16。
- **应用与组件分层。** Muse Spaces、Perplexity Teammates 是商业产品参照，OpenDuet 继续依赖 Intelligence 与其仓内 OpenBot。新功能不统一增加开源底层生态数量。
- **协调模型已有新直接证据。** OpenAI [11 月 2–6 日周页](https://learn.chatgpt.com/docs/whats-new/november-2-6-2026)明确 Terra 加入 Dots 模型家族，撤回上版只能确认 Work/Codex 的时点限制。模型实际选择按任务记录。

本轮范围为资料、发行与静态实现检查。账号、部署、安装签名和产品实验状态保存在[来源索引](sources-2026-11-08.md)，完整变化与逐行差异保存在[本轮 gap](gaps/2026-11-08/01/README.md)。
