# 构建附录：通用 Agent 运行时与组件

本轮活动监测：**2026-10-28**。返回[修订主报告](personal-agent-landscape-2026-10-28.md)。能力与许可说明沿用 10 月 22 日固定来源；本轮新增 HEAD、少量发行记录与选型影响见第 5 节。未重新安装或运行组件。

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

本表记录活动，不把每个新提交当成功能发布。组件仍按它解决的实现层选择；同类产品名单不因组件发版而扩张。

| 项目 | 10 月 28 日取得的 HEAD | 时间（UTC） | 本轮深度 |
| --- | --- | --- | --- |
| openclaw/openclaw | [b4cc6fe87a18](https://github.com/openclaw/openclaw/tree/b4cc6fe87a18220ac11a0a3377b0a3ef43cf2093) | 2026-10-28 02:58:55 | HEAD + 发行说明 |
| NousResearch/hermes-agent | [aad60e1ac670](https://github.com/NousResearch/hermes-agent/tree/aad60e1ac670268aa39b364b16b16dbf06de85df) | 2026-10-28 02:34:10 | HEAD + 发行说明 |
| nanocoai/nanoclaw | [acc2b1c8f52a](https://github.com/nanocoai/nanoclaw/tree/acc2b1c8f52a954368cfaf04b61c32f9a1efc280) | 2026-10-26 07:00:31 | HEAD 活动监测 |
| HKUDS/nanobot | [b07b3eac244f](https://github.com/HKUDS/nanobot/tree/b07b3eac244ff7faa7eeb2d4777fe54dbae1b6d2) | 2026-10-27 13:05:32 | HEAD 活动监测 |
| agentscope-ai/QwenPaw | [9e59502cbe3b](https://github.com/agentscope-ai/QwenPaw/tree/9e59502cbe3b62e9a962027cfa6c549936c89135) | 2026-10-28 01:58:24 | HEAD 活动监测 |
| letta-ai/letta-code | [5dea67021b99](https://github.com/letta-ai/letta-code/tree/5dea67021b99810707ff753db35e4534f70ff1fd) | 2026-10-28 02:41:25 | HEAD 活动监测 |
| langchain-ai/langgraph | [eb8ec111b3e9](https://github.com/langchain-ai/langgraph/tree/eb8ec111b3e9d3108af5d7bdcac51e3e913637a0) | 2026-10-27 21:46:39 | HEAD 活动监测 |
| mem0ai/mem0 | [26cdefb46600](https://github.com/mem0ai/mem0/tree/26cdefb46600c0fa5953c4b5ee5003c125539fc4) | 2026-10-26 14:51:39 | HEAD 活动监测 |
| browser-use/browser-use | [2cc71890e650](https://github.com/browser-use/browser-use/tree/2cc71890e65056b67fdb29d98bb407749c15bb08) | 2026-10-26 22:00:16 | HEAD + 发行说明 |
| n8n-io/n8n | [dd5f870ecc38](https://github.com/n8n-io/n8n/tree/dd5f870ecc38344951fb3956f1a7ba7852612c70) | 2026-10-27 20:55:46 | HEAD 活动监测 |
| langgenius/dify | [c01cb5d119a6](https://github.com/langgenius/dify/tree/c01cb5d119a69532df73ec20da8daa18cf44e0fb) | 2026-10-28 02:46:42 | HEAD 活动监测 |


- **OpenClaw**：本次首条发行记录是 [v2026.10.10-beta.4](https://github.com/openclaw/openclaw/releases/tag/v2026.10.10-beta.4)，标为预发行。其说明涉及定时跟进授权、Gateway 凭据和备份审批的修复，不能据此称为稳定渠道全量发布。
- **Hermes**：取得 [v0.22.5](https://github.com/NousResearch/hermes-agent/releases/tag/v0.22.5) 记录，GitHub 发布时间为 10 月 23 日，内文写 10 月 22 日。作为维护补丁观察，不按版本说明中的提交数量判断个人 Agent 效果。
- **Browser Use**：取得 [0.13.14](https://github.com/browser-use/browser-use/releases/tag/0.13.14)。说明明确保留 Python Agent，Pi 迁移另列；本轮未验证 PyPI 是否已完成分发，不把“发布 GitHub Release”当成所有安装渠道已更新。
- **OpenAI 执行模型**：[10 月 26–30 日官方周页](https://learn.chatgpt.com/docs/whats-new/october-26-30-2026)新增 GPT-6.1 Terra 在 Work/Codex 的可用性说明。它属于执行端模型选择证据，不证明 Dots 的主模型已经替换。
- **其余组件**：HEAD 已前进，但本轮未完整读取变化、重新核对许可证或跑通部署。上面第 1、2 节的固定 README 保持历史引用，不能当成新 HEAD 的全部能力保证。

对本项目，先验证主报告的应用流程，再决定是否替换底层组件。新版本重点复测任务恢复、权限配置、记忆迁移和连接器行为；不要为了追逐 HEAD 同时改变模型、框架与数据层。

详细快照与取证限制见[本轮来源索引](sources-2026-10-28.md)。
