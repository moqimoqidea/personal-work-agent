# 构建附录：通用 Agent 运行时与组件

本轮活动监测：**2026-11-12（Asia/Shanghai）**。返回[修订主报告](personal-agent-landscape-2026-11-12.md)。能力与许可说明沿用 10 月 22 日固定来源；本轮 HEAD、发行渠道与选型影响见第 5 节。未重新安装或运行组件。

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

基线为 [11 月 8 日附录](agent-building-blocks-2026-11-08.md)。Hermes 0.23.0、nanobot 0.4.1、LangGraph 1.2.20、Dify 1.19.0 已在上轮收录，本次重读范围不能当作新发布。

11 个组件重新查询默认分支 HEAD 与 Releases 前五项；相对 11 月 8 日有 10 个 HEAD 前进、Mem0 相同。能力与许可的历史章节没有被重新全部审查，以下按阅读范围说明发行变化，不等于升级验收。

| 仓库 | 11 月 8 日 SHA | 本次固定 SHA | committer 时间（UTC） | 实际读取范围 |
| --- | --- | --- | --- | --- |
| openclaw/openclaw | [6c983bb80229](https://github.com/openclaw/openclaw/tree/6c983bb8022904eb8ede66691341522943d3f61e) | [7ea57a8cba1a](https://github.com/openclaw/openclaw/tree/7ea57a8cba1aa8ada672ef967956bd87ea316558) | 2026-11-12T08:11:58Z | HEAD/发行监测；不代表全功能/许可复验 |
| NousResearch/hermes-agent | [8422e54df36f](https://github.com/NousResearch/hermes-agent/tree/8422e54df36f42371f31b8fbee653e7c801edcbd) | [8144b2ae3a34](https://github.com/NousResearch/hermes-agent/tree/8144b2ae3a3435e7e0a5fe052aef3a64f0999136) | 2026-11-12T08:12:09Z | HEAD/发行监测；不代表全功能/许可复验 |
| nanocoai/nanoclaw | [dd19240d9036](https://github.com/nanocoai/nanoclaw/tree/dd19240d9036bab13491953513cb88ec7a2980e6) | [62dc09057b79](https://github.com/nanocoai/nanoclaw/tree/62dc09057b792291c887df5caac059f57347849b) | 2026-11-11T18:36:13Z | HEAD/发行监测；不代表全功能/许可复验 |
| HKUDS/nanobot | [1e2dc02fa228](https://github.com/HKUDS/nanobot/tree/1e2dc02fa228b6c5c62b8fc84de2a2d77dd925f3) | [0ce10533d364](https://github.com/HKUDS/nanobot/tree/0ce10533d364607f1e75bb061577272e4ba80a11) | 2026-11-12T08:08:48Z | HEAD/发行监测；不代表全功能/许可复验 |
| agentscope-ai/QwenPaw | [2cf28d14a20c](https://github.com/agentscope-ai/QwenPaw/tree/2cf28d14a20c9f9c769cce2a9c0568ccf84e459c) | [dfb10114e6d8](https://github.com/agentscope-ai/QwenPaw/tree/dfb10114e6d81b67751188f7d24a49870b7b0959) | 2026-11-12T04:06:00Z | HEAD/发行监测；不代表全功能/许可复验 |
| letta-ai/letta-code | [64fdf5999441](https://github.com/letta-ai/letta-code/tree/64fdf5999441094a6f43f7a38a6d356519fea029) | [ed08ddcb8e10](https://github.com/letta-ai/letta-code/tree/ed08ddcb8e109f5e64076073294a832955ffc23e) | 2026-11-12T06:55:46Z | HEAD/发行监测；不代表全功能/许可复验 |
| langchain-ai/langgraph | [e5e37b5d70db](https://github.com/langchain-ai/langgraph/tree/e5e37b5d70dbfd93c7006bd90a658c6179a95946) | [b4cb0f19e3d8](https://github.com/langchain-ai/langgraph/tree/b4cb0f19e3d8984e8a57f85667b8d1bec018f0ab) | 2026-11-12T01:43:53Z | HEAD/发行监测；不代表全功能/许可复验 |
| mem0ai/mem0 | [f1791daa86d4](https://github.com/mem0ai/mem0/tree/f1791daa86d469249c9b002f62644d58a1eb96a0) | [f1791daa86d4](https://github.com/mem0ai/mem0/tree/f1791daa86d469249c9b002f62644d58a1eb96a0) | 2026-11-06T16:53:06Z | HEAD 相同；本轮文档重读按证据表，旧功能/许可不重审 |
| browser-use/browser-use | [b49a68e4060a](https://github.com/browser-use/browser-use/tree/b49a68e4060acb226da8f784194fef301c53a6d7) | [7fdd63c03fd3](https://github.com/browser-use/browser-use/tree/7fdd63c03fd342aab4fe44507c77c3221ffd43c6) | 2026-11-11T00:05:55Z | HEAD/发行监测；不代表全功能/许可复验 |
| n8n-io/n8n | [01bd57cddf11](https://github.com/n8n-io/n8n/tree/01bd57cddf11e8173b16adce1b22a8eb94598672) | [dd098f08ff16](https://github.com/n8n-io/n8n/tree/dd098f08ff16a1beb0223777ef37588f98ab4a91) | 2026-11-12T07:55:13Z | HEAD/发行监测；不代表全功能/许可复验 |
| langgenius/dify | [208a2489f05f](https://github.com/langgenius/dify/tree/208a2489f05f688afd701ba262a42d08289996a7) | [cc906be6f80e](https://github.com/langgenius/dify/tree/cc906be6f80eb9c260455b42b04ceada7415423c) | 2026-11-12T07:42:47Z | HEAD/发行监测；不代表全功能/许可复验 |

| 对象 | 本期证据 | 采用影响 / 未验证边界 |
| --- | --- | --- |
| Browser Use | 1.0.0 重写为持久 Python REPL + CDP；稳定列表含 1.0.2，首项 1.0.3rc1 是预发行 [U152] | 默认 `Browser()` 由本地改云，0.x API/导入和错误处理有破坏变化；锁定版本，显式选择本地，不自动沿用旧数据路径；厂商 benchmark 不作为本研究成绩 |
| Hermes | 0.23.0 的统一 Gateway 会话/Webapp 与组聊；0.23.1 修复插件目录大小上限 [U153]、[U154] | 会话所有权和客户端同步值得研究；0.23.1 API 发布时间 11 月 10 日 UTC，正文 Release Date 为 11 月 9 日；未审所有长变更 |
| QwenPaw | 2.3.0 于 11 月 11 日稳定发布，加入 Piccolo 本地审查/压缩模型与 OpenUI [U155] | 从上轮 beta 观察转稳定版验收；本地审查/压缩仍 opt-in，单 runtime 一次一个模型，不推断零云流量 |
| LangGraph | 核心 1.2.20：每次 interrupt 独立 ID、strict resume；SDK 0.4.14 暴露 strict_resume [U156] | 适合作陈旧/重复审批恢复参照；核心、SDK、CLI 是不同包，仍需业务幂等与结果检查 |
| nanobot | 0.4.1 的执行/恢复与升级说明 [U157] | 旧历史迁移保留到 0.4.x，临时 apiType 转换将在后续移除；需保存迁移配置并沿原安装方式升级，不由发布包推断应用自动更新开启 |
| OpenClaw | v2026.11.3 稳定 Highlights：私有子任务输出、取消交接、错误可见；另有 beta.2 和 9 月维护线 [U158] | 不能拿 beta 列表首项覆盖稳定渠道；只读摘要，未完整审计安全与恢复修复 |
| NanoClaw | 首五项含 v2026.11.0-beta.1，说明 stable 仍 2026.10.0 | 11 月 beta 替代未稳定的 10.1 线；仅发行开头与元数据，不能当稳定已升级 |
| Letta Code | 0.34.55/56：父上下文 fork、路由与旧监听器 no-fork 兼容 [U159] | 适合作委派上下文与兼容参照；未运行测试，不等于所有子任务都有完整上下文 |
| Dify | 1.19.0 嵌套 tracing、应用包 v2、Skills 自动化 [U160] | 新执行有更细 trace，不回填旧历史；Compose 2.35+、tracing 队列与兼容导入器需一并计划；许可仍沿用历史 |
| Mem0 / n8n | Mem0 首项仍 v2.2.1，HEAD 前进；n8n 有 2.47.4 / 1.123.94 稳定和 2.48.1 预发行 | 仅活动/元数据；未重读所有功能与许可，也不以浮动 stable 别名选择生产目标 |

## 6. 与应用选型同步的边界

- OpenBot 更新为 v1.0.2 桌面包，Personal 无独立记忆，Team 另核，本地 Intelligence 仍需免费许可，生产另有许可；HEAD 迁移与发行不同。OpenDots/OpenDuet 团队入口转向 OpenBot，独立专用流程仍需核对。
- OpenSuperBot v0.5.0 修正前轮家目录遮蔽，代码修正与运行验证分开；普通浏览器审批仍为约定。原生 Responses/Anthropic 适配可参考上下文和凭据处理，不据此外推官方所有模型限制。
- nanoMuse 预算文件与基线相同，仍限 Python runtime/Python hands；更具体的隐私说明属于新 HEAD，安装包当前仍 1.0.9。
- Dots 的 11 月 4 日产品更新已明确 Terra 加入模型家族；当前电脑页支持多电脑、每线程一台（确切变更日未标），应撤回上轮“仅 Work/Codex”结论；不推断每个回合的实际路由。
- Perplexity Teammates 已在上轮收录，本轮统一为第七个商业主样本，不能因同属 Computer 就默认继承 Mac fully local 模式；Muse Spaces 是持续交互成果，不能和开源组件混算。

所有观察均未执行产品安装、部署或账号实验。来源与发行时间见 [本轮来源索引](sources-2026-11-12.md)。
