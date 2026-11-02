# 2026-11-02 / 01：报告更新与差异

| 项目 | 本次记录 |
| --- | --- |
| 截止日与版本 | 2026-11-02（Asia/Shanghai，查询时），版本 2026-11-02 |
| 基线报告 | 2026-10-28，提交 `c69eb962dd73f0d7b2958818703ab67a7b3866f1` |
| 任务开始 HEAD | `897b0241b92d0bda97a8a5d25c439bd4ca0e8758`，该提交更新流程与旧 gap，非另一个报告版本 |
| 本次 revision | 提交前为 null，以三份文件 SHA-256 固定；不把最终提交自身 SHA 递归写回 |
| 实测状态 | 公开资料、版本化文档和静态源码；未登录、部署或运行产品，未执行隔离探针 |

本次三份文档：[主报告](../../../personal-agent-landscape-2026-11-02.md)、[来源索引](../../../sources-2026-11-02.md)、[构建附录](../../../agent-building-blocks-2026-11-02.md)。

基线三份文档：[主报告](../../../personal-agent-landscape-2026-10-28.md)、[来源索引](../../../sources-2026-10-28.md)、[构建附录](../../../agent-building-blocks-2026-10-28.md)。

## 范围

复核六个核心商业产品及相关扩展原厂资料；查询原 25 仓 metadata/HEAD，16 个前进、9 个相同；补入 OpenDuet，合计 26 仓与八个直接应用样本。取得八份主样本 README 并阅读关键段落，读取六组 compare 元数据与文件清单，按重要变化追加固定文档及源码。十九个 Releases 列表各取前五项，说明按全文或节选分别标记。

OpenBot 比较文件列表达到 300 上限；nanoMuse 179 commits / 280 files 没有逐提交审计。组件主要做活动与发行监测。未重读的旧许可、原厂页面和背景证据不改写日期；具体成功、失败、替代入口与范围见来源索引。

## 变化台账

| 编号 | 类型 | 对象 | 原认识 | 新证据 | 为何影响结论 | 来源 |
| --- | --- | --- | --- | --- | --- | --- |
| G01 | 补证修正 | Grok Bot | 基线日志录到 v0.77.0 | 10 月 27 日 v0.78.1 已有购物、订单和订阅模板 | 补齐既有能力，不把早于基线的事件算本期发布 | U30 |
| G02 | 补证修正 | Muse | 已确认美国、加拿大、新加坡，漏日本 | 日本官方 10 月 23 日开始提供，部分本地功能另定 | 扩大已证实地区，保留各区功能和连接器差异 | U31、U02 |
| G03 | 补证修正、未能核验 | Dots 联系渠道 | 主报告侧重 ChatGPT/Slack/Teams | 周页明确美国 Pro iMessage/RCS beta，当前页有 iOS widget/Shortcuts；精确发布时刻未标 | 纳入低摩擦联系比较，不外推群聊、第三方电话或其他短信读取 | U32、U33 |
| G04 | 补证修正 | Duet | 资格只列美国 Pro/Max | 当前帮助列 Pro/Max/Ultra，说明项目外聊天搜索；Ultra 加入日未标 | 同步资格与记忆实验，仍需候补，限制与共享配额保留 | U34 |
| G05 | 补证修正、未能核验 | Today | 中国站超时，权益和 Android 入口待核 | 首页与目录可读，列注册权益及 Mac/Windows/Linux/iOS/Android 入口 | 缩小取证缺口，不将目录等同安装可用或全球统一权益 | U35、U36 |
| G06 | 本期新增、结论调整 | OpenBot | 以每 Bot 独立/共享电脑概述，Gmail 为首要验收 | 主分支变为每人电脑、条件式 Isolated、Recorder/Browser、退款审批与审计修复 | 重写比较与迁移检查；同电脑无强隔离；v0.2.0 仍与源码分开 | U41、U42、U43、U44、U45 |
| G07 | 本期新增、结论调整、未能核验 | OpenGrokBot | v0.3.0 以 Docker 与只读 watch 为重点 | v0.4.0 增本机电脑；Linux bubblewrap 参数没有同样的 SECRET_DIRS 遮蔽，和安全文共同表述不一致 | 本地命令默认关闭，真实资料优先验收 Docker；差异仅静态，未复现泄露 | U46、U47、U48 |
| G08 | 本期新增、结论调整 | nanoMuse | 发行记录到 1.0.7；强调记录与自带密钥 | 1.0.8/1.0.9 发版，跨设备审批、桌面修复、Python 预算；版本化隐私含 relay 0.31 训练条件 | 扩展跨设备验收；预算不覆盖所有引擎/费用；记录、同步、训练分别检查 | U49、U50、U51、U52、U53、U54、U55 |
| G09 | 补证修正、结论调整 | CopilotKit/OpenDuet | 没有确认 Duet 完整直接参照 | 补入 10 月 21 日 UTC 创建的早期应用模板；晨报、分拣、Tasks/Make、MIT 应用代码 | 八个直接应用样本；共用 OpenBot 基础，不等于独立运行栈或本周新首发 | U62、U63、U64、U65 |
| G10 | 本期新增、复核未变 | chyroc/open-muse | HEAD 与更早版本相同，分类为托管 MA 客户端 | 5 commits / 16 files；抽查 Windows 听写停止和系统语音条件 | 记录客户端维护，完整后台开放分类不变，未验收 Windows 分发 | U56、U57 |
| G11 | 本期新增、结论调整 | open-instinct | 以 Inkbox/Maritime/Composio 为重点 | 增加 WhatsApp/Baileys 和 Keenable 路径，18 commits / 44 files | 新增可选入口但非官方 API；不把维护者说明当实际送达、身份或账号可持续性成绩 | U58、U59、U60 |
| G12 | 补证修正、结论调整 | Perplexity | Mac fully local 只取得目录；Automations 正文缺失 | 正文确认硬件/订阅/36 GB 建议、授权转云，另有事件触发与跨轮历史 | 可加入本地资料和持续研究扩展对照；旧事件不算本期发布 | U39、U40 |
| G13 | 本期新增 | Town / Gemini | Town 仅录到共同编辑；Gemini 以 Tasks 入口为重点 | 10 月 29 日 1Password 条件式接入及 Gemini 文件编辑公告 | 补登录与成果编辑参照，保留账号、格式和端侧限制 | U37、U38 |
| G14 | 本期新增、复核未变 | Celesto / 未变化应用 | 前轮收紧 Celesto 为本地 QEMU 预览，其他保留分类 | Celesto 7 commits / 32 files，未见 open-muse/ 路径；9 个旧仓 HEAD 相同 | kernel/构建维护不算个人助理能力升级；相同 HEAD 不证明托管依赖不变 | U61 |
| G15 | 本期新增、复核未变 | 构建组件 | 多数组件只监测 HEAD，部分发行到旧版本 | 记录 OpenClaw stable/beta、nanobot 0.4.0、LangGraph 1.2.19、QwenPaw beta.2、Letta 0.34.38；其余按元数据 | 稳定/预发行/维护线分开；新日志、持久性和升级仍需实测，不重盖许可日期 | U66、U67、U68、U69、U70、U71 |
| G16 | 复核未变、未能核验 | Instinct / Cue / 账号与实测 | 价格、完整审批与部分资格证据不足 | Instinct 官网和隐私已复核；cue.im 仍无可读正文；所有候选未登录或部署 | 不编造价格/权限矩阵，不把公开页面和文档检查写成端到端验收 | S23、S24、U20 |


## 选型与验证的变化

工作原型保留 OpenBot 无附件邮件路径，新增 OpenDuet 的分拣—晨报—Tasks/Make 对照。只读监测继续看 OpenGrokBot，真实执行先验收 Docker；本地命令默认关闭，Linux 参数与安全文的静态差异以临时资料验证后再决定。nanoMuse 1.0.9 先核对账号、中继、训练与预算引擎范围。硬件和订阅满足时，将 Perplexity fully local 加入本地资料扩展对照。

E01–E06 沿用前轮，新增 E07–E12 覆盖电脑归属、Linux/macOS 边界、手机重复审批、分引擎预算、50 封邮箱覆盖、短信式入口与转云。全部尚未执行，不与每产品 90 次基础设计混算。

## 未解决项

- OpenGrokBot 的静态差异尚未运行验证，不称已复现泄露，也不以 self-check 代替宿主目录检查。
- Muse 新加坡正文本轮未完整取回，沿用历史 U02；日本本次读到正文，仍不能证明所有地区功能全量。
- Dots 周页没有精确 texting 发布时刻，Duet Ultra 加入日未明；各账号实际资格和配额未测。
- Today 权益领取与各平台功能/安装签名、Cue 当前资格、Instinct 价格和完整权限仍有缺口。
- 各项目的成功率、跨天恢复、计费、删除与真实授权一致性继续待测；旧许可证没有被统一重审。

## 逐行差异与检查

- [manifest.json](manifest.json)：基线、当前哈希、证据、仓库/发行快照与实际检查结果。
- [report.diff](report.diff)、[sources.diff](sources.diff)、[building-blocks.diff](building-blocks.diff)：从基线报告提交的完整文件与新版完整文件生成的全部统一差异。

diff 用于审查和重建不同日期文件，不承诺直接对当前工作区执行 git apply。检查在临时目录重建三个目标；不拿历史文件原地试应用。归档 diff 的空白上下文标记保持原样，普通 Markdown 仍检查空白。

检查状态：引用、Markdown 本地链接/锚点/表格/围栏、26 仓快照、manifest 哈希/行数和三个 diff 的临时重建均通过；旧研究文件保持原样，缓存已忽略。本次 11 个明确文件的暂存范围与 git diff --cached --check 亦通过，记录在 manifest。检查不包含产品运行。

返回[当天批次](../README.md)、[所有归档日期](../../README.md)或[更新流程](../../../UPDATE-WORKFLOW.md)。
