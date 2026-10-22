# 构建附录：通用 Agent 运行时与组件

核验时点：2026-10-22。返回[商业个人 Agent 与同类开源替代调研](personal-agent-landscape-2026-10-22.md)。

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
