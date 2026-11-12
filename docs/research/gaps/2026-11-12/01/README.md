# 2026-11-12 / 01：报告更新与差异

基线为远端已交付 2026-11-08 报告，提交 `09e8b1e0607af28d435c3e427dc8db31726c26ce`。任务最初本地 HEAD 为 `5918655bf47c3dd49fe973654c4bac216474cf04`，发现后同步并改用远端基线。日期按 Asia/Shanghai；current.revision 提交前为 null，以文件 SHA-256 固定。

本次 [主报告](../../../personal-agent-landscape-2026-11-12.md)、[来源](../../../sources-2026-11-12.md)、[构建附录](../../../agent-building-blocks-2026-11-12.md)。基线 [主报告](../../../personal-agent-landscape-2026-11-08.md)、[来源](../../../sources-2026-11-08.md)、[附录](../../../agent-building-blocks-2026-11-08.md)。

## 范围和边界

七个商业主样本含上轮已加入的 Teammates，26 仓与八个直接应用；相对11月8日15个HEAD前进、11个相同。19份Releases列表各前五项；五组增量compare，OpenBot达300文件上限。U122–U179为58条新观察身份，不代表58个新功能。U01–U121及E01–E16保持身份，本轮新增E17–E20。旧资料和许可的日期不因本次重排而刷新。

未登录、安装、部署、验签、计费或执行产品/隔离测试。原目录.git不可写、标准fetch遇DNS故障，使用连接器取回原远端对象，在临时克隆逐项校验blob/tree/commit一致后fast-forward。修改AGENTS与更新流程，使后续任务必须先同步并确认最新报告基线。

## 变化台账

| 编号 | 类型 | 对象 | 原认识 | 新证据 | 为何影响结论 | 来源 |
| --- | --- | --- | --- | --- | --- | --- |
| G01 | 本期新增、旧资料补证 | Grok Bot | 上轮日志只录到 10 月 27 日 | 11 月 11 日会议/团队治理；5–6 日条目补证 | 新发布与旧遗漏分开，按套餐/管理员验收 | U122 |
| G02 | 本期发版、结论调整 | OpenBot | 0.3.3 桌面和较新 HEAD，Personal 无独立记忆 | v1.0.2、许可与审批升级；tag/HEAD 都仍禁用 Personal 独立记忆 | 更新部署/升级门槛，长期记忆不外推桌面 Personal | U133、U134、U135、U136、U169、U170、U173、U174、U175 |
| G03 | 本期维护、结论调整 | OpenDots / OpenDuet | 独立模板及上轮恢复补证 | 社区 starter，团队入口转 OpenBot skin | 平台和专用流程分开，保留原恢复证据和实验编号 | U137、U138、U176、U177 |
| G04 | 当前页变化、事件日期未标 | Dots 多电脑 | 一台个人电脑 | 多台已授权电脑，每线程同时一台 | 同步主表、正文和多线程实验，不猜修改日 | U171 |
| G05 | 本期源码、旧资料补证、复核未变 | OpenSuperBot / nanoMuse | 0.5.0 更名/隔离修正；1.0.9 与 Skills/隐私补证 | 分别 33 / 120 commits；原生协议补读、隐私/预算复核 | 不重复计算既有发布，源码/tag/包和运行验证分开 | U141、U142、U143、U144、U145、U146、U147、U148、U149、U178、U179 |
| G06 | 本期发版、结论调整、复核未变 | 构建组件 | 0.x Browser Use、Hermes0.23、QwenPaw beta | Browser Use1.0、Hermes0.23.1、QwenPaw2.3稳定及近期发行 | 迁移默认流量、会话和稳定渠道；上轮已有发行仅复核 | U152、U153、U154、U155、U156、U157、U158、U159、U160 |
| G07 | 复核未变、研究分类调整 | Muse / Dots / Duet / Teammates | 语音/Spaces/Terra/企业预览/重置/Teammates 已收录 | 当前正文重读，Teammates统一第七主样本 | 不称本期新增，历史模型/资格/计费结论保留 | U123、U124、U125、U126、U127、U128、U150、U151 |
| G08 | 复核未变、未能核验 | Today / Instinct / 旧样本 | 账号/权限/安装仍有缺口 | 当前正文和15变/11同仓库快照 | 保留实际资格、费用和端到端缺口，不更改旧许可日期 | U129、U130、U131、U132、U167 |
| G09 | 流程修正 | 仓库与报告基线 | 本地未同步，误以11月2日作最近交付 | 先取得并校验11月8日远端，累计引用/实验身份和差异重建 | AGENTS/流程加入先同步再读取基线、提交前再检查远端 | 本仓基线、AGENTS 与 UPDATE-WORKFLOW |

## 结论与未解决项

OpenBot新版仍保留Personal独立记忆排除；优先验收邮件/浏览器和部署，长期记忆按edition选择。OpenDots/OpenDuet的团队维护入口转向OpenBot，保留专用流程；OpenSuperBot旧修复继续待运行验证。Muse专用模型、nanoMuse Skills与OpenDots恢复采用11月8日已交付证据，不丢弃或重算。

实际账号、签名、许可续期、产品成功率、费用和跨天恢复均未实测。Dots多电脑改变的绝对日期未标，11月18日默认开放/计费仍是未来节点。

## 完整差异与检查

[manifest.json](manifest.json)、[report.diff](report.diff)、[sources.diff](sources.diff)、[building-blocks.diff](building-blocks.diff)均从11月8日完整提交重建，非节选。统一差异在临时目录应用并核对哈希，不改旧报告。

检查状态：引用、Markdown 本地链接/锚点/表格/围栏、26 仓快照、manifest 哈希/行数和三个 diff 的临时重建均通过；旧研究文件保持原样，缓存已忽略。暂存范围和暂存差异检查在提交前另记 manifest。检查不包含产品运行。

返回[当天索引](../README.md)、[总索引](../../README.md)、[更新流程](../../../UPDATE-WORKFLOW.md)。

## 提交与推送状态

本地在已同步的隔离检出提交。原目录 Git 元数据只读、shell 无法解析 GitHub，连接器 create-tree 返回 HTTP 403 Resource not accessible by integration；远端引用没有修改，不能把本地提交当作已推送。最终交付单独报告真实本地 SHA，并提供 Git bundle 保存提交。
