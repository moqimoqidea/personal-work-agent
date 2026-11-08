# 2026-11-08 / 01 报告更新与差异

| 项目 | 本次记录 |
| --- | --- |
| 核验日与版本 | 2026-11-08，Asia/Shanghai，版本 2026-11-08 |
| 记录生成时间 | 2026-11-08T20:30:02+08:00 |
| 基线报告与任务开始 HEAD | 2026-11-02，`5918655bf47c3dd49fe973654c4bac216474cf04` |
| 本次 revision | 提交前为 null，三份文件 SHA-256 固定内容；最终提交和推送结果在交付回复给出 |
| 产品测试 | 公开正文、发行与静态源码检查；账号、安装、部署、验签和端到端均未执行 |

本次文档包括[主报告](../../../personal-agent-landscape-2026-11-08.md)、[来源索引](../../../sources-2026-11-08.md)和[构建附录](../../../agent-building-blocks-2026-11-08.md)。基线为 [11 月 2 日主报告](../../../personal-agent-landscape-2026-11-02.md)、[来源](../../../sources-2026-11-02.md)、[附录](../../../agent-building-blocks-2026-11-02.md)。

## 范围

复核六个核心商业产品和扩展原厂来源，新增 Perplexity Teammates 直接商业参照。原 26 仓全部取得 metadata/HEAD，15 个前进、11 个相同，八个主应用 README 按定位/依赖/交付范围阅读。OpenGrokBot 更名为 OpenSuperBot，repository id 相同，不重复计数。

五组 compare 中 OpenBot 303、nanoMuse 387 个提交元数据分页取全，标题按主题抽查。OpenBot、nanoMuse、Celesto 的文件清单达到 300 上限，关键结论追加固定文档/代码。Celesto 的 OpenMuse 子树 SHA 在两个根 tree 中相同。19 份发行列表各取前五项，说明阅读深度各自记录。新增 U72–U121 共 50 条观察，旧证据实际重读与保留日期分开。

## 变化台账

| 编号 | 类型 | 对象 | 原认识 | 新证据 | 为何影响结论 | 来源 |
| --- | --- | --- | --- | --- | --- | --- |
| G01 | 本期新增、结论调整 | Muse 语音与头像 | 主要沿用早期设计与地区资料 | 11 月 5–6 日公告美国先行 mobile/web/Mac 语音与头像，眼镜/Charm soon | 语音中途改向和后台继续工作分项验收 | U76 |
| G02 | 本期新增、结论调整 | Muse Spaces 与专用模型 | 以目标、活动和可编辑记忆为主要参照 | 11 月 6 日 Spaces 与 Wonder 训练的 Active Memory/Active Focus 专用模型 | 增加持续成果、过期记忆和遇阻恢复实验，厂商分数单列 | U77、U78 |
| G03 | 本期新增、结论调整 | Dots 模型与入口 | 只确认 Work/Codex 的 Terra，短信式入口已补证 | 11 月 4 日明确 Terra 加入 Dots，通知回复/分享、批注与 Windows 修复 | 更新模型判断，精确指向与跨端验收按资格进行 | U72、U73、U75 |
| G04 | 本期新增、结论调整 | Dots 工作区 | Enterprise 分批开放与管理员开启，未列本期预览期限 | Enterprise/Edu/Healthcare 管理员预览，11 月 18 日默认访问/计费及 UAE residency 排除 | 角色、主 dot 与委派工作计费拆分 | U73、U74 |
| G05 | 补证修正、未能核验 | Duet 用量重置 | 写获邀重置安排截至 11 月 30 日 | 当前帮助列 Pro 三次、Max/Ultra 一次，未用重置 12 月 15 日过期，修改日未标 | 价格/资格表同步，实际账号重置仍待核 | U79 |
| G06 | 本期新增、结论调整 | Perplexity Teammates | Computer 本地模式和 Automations 为扩展参照 | 11 月 4 日 Teammates 承担长期工作、协调 Computer 和其他 teammate，Max web 首发 | 新增直接商业参照和对比行，iOS soon，未扩充开源仓库数量 | U80 |
| G07 | 本期新增 | Perplexity 电商公告 | 未纳入该跨业务工作流正文 | 11 月 3 日描述 Shopify/Meta/Klaviyo 与品牌 Skills 的交付和审核约束 | 补小企业流程参照，未当作独立新套餐或全部新功能 | U81 |
| G08 | 本期新增、结论调整 | OpenBot 发行与 Personal | 发行列表首项 v0.2.0，主分支为 Beta 工作模板 | 0.3.0–0.3.3 与桌面资产，Personal/Team、归档/destructive 审批和 goal 生命周期 | 重写交付、电脑归属、授权与升级验收，保留账号/评估许可和识别缺口 | U82、U83、U84、U85、U87、U88、U89、U90、U120 |
| G09 | 本期新增、结论调整、未能核验 | OpenBot Personal 记忆与学习 | 基线以应用模板的长期记忆作统一描述，尚无 Personal 区分 | 晚于 v0.3.3 的 11 月 8 日提交关闭 Personal 记忆来源、同步、工具、API 与 loader；HEAD另有 Skills 学习审阅/自动批准，部分文档尚未同步 | Personal 先验收邮件/浏览器，长期记忆按 Team 或其他候选单独选择；新增 E13 | U86、U91、U119 |
| G10 | 本期新增、结论调整 | OpenSuperBot v0.5.0 | OpenGrokBot 0.4.0 的 Linux home 遮蔽文码差异待验证 | 同 id 更名 OpenSuperBot，0.5.0 整 home 遮蔽/工具链例外/自检，Windows 本地电脑、每同事模型与 API 录制首阶段 | 旧差异已有静态修复，E08 更新；网络/系统服务/资源和普通审批仍逐项验收 | U92、U93、U94、U95、U96、U98、U99、U100 |
| G11 | 补证修正、未能核验 | OpenSuperBot 密钥说明 | 安全表写模型密钥只在环境变量 | models 与发行说明允许 data/llm-key 和 llm-keys/id 持久连接密钥，security 表待同步 | 按实际路径/账号权限检查，不推导秘密不落盘，订阅条款仍为维护者声明 | U95、U97 |
| G12 | 本期新增、补证修正、结论调整 | nanoMuse 主分支 | 1.0.9 隐私笼统句有冲突，未列本期 Skills/恢复维护 | 387 提交区间、隐私文字修正、Skills 全局/工作区与导入/同步维护；最新发行仍1.0.9 | 文档修正和新源码分别记录，保留记录/训练条件，TestFlight build 待核，新增 E16 | U101、U102、U103、U104、U105、U106 |
| G13 | 本期新增、结论调整 | OpenDots | HEAD 与更早版本相同，审批中断恢复未纳入 | 7 提交/11 文件，5 分钟无结果 claim 可 interrupted，绑定 approval 的条件 reclaim 和显式 Retry | 新增 E14，状态恢复与外部去重分开，回执丢失仍可能重复动作 | U107、U108、U109 |
| G14 | 本期新增、复核未变 | Celesto 与未变化应用 | Celesto 前轮主要是 kernel/构建，其他主应用保留分类 | Celesto 8 提交 SDK/CLI 维护，OpenMuse 子树 SHA 相同；OpenMuse/OpenDuet/chyroc/open-instinct HEAD 相同 | SDK 更新单列，应用分类依据子树与 README 保留，外部服务状态另核 | U110、U111 |
| G15 | 本期新增、结论调整 | 构建组件 | 多项发行仍为上轮版本 | OpenClaw 2026.11.1、Hermes0.23.0、nanobot0.4.1、Letta0.34.45、LangGraph1.2.20、Dify1.19.0、n8n2.46.6 | 恢复、strict resume、旧数据迁移和安装归属分项记录，版本子包和预发行分开 | U112、U113、U114、U115、U116、U117、U118 |
| G16 | 复核未变、补证修正 | Grok Bot / Today / Muse 旧地区 | 动态日志/计费和平台目录有早期观察，Muse 新加坡上一轮未重取正文 | 本轮重读当前价目/日志、Muse 地区和 Today 中外目录；国际 Android Play Store 与中国 APK分别记录 | 更新实际访问范围，旧事件保留原日期，账号领取与安装仍待测 | S01、S03、S04、S05、S10、U02、U31、U35、U36、U121 |
| G17 | 复核未变、未能核验 | Instinct / Cue / 账号与实测 | 统一价格、完整权限与部分资格不足 | Instinct 公开定位和隐私相关段落可读；Cue 零行正文，Manus 公告补历史身份；全部产品仍未登录/部署 | 保留实测缺口，E01–E16均为方案，文档检查不作为产品成绩 | S23、S24、U20 |

## 选型与验收影响

OpenBot 邮件/浏览器原型按 Personal/Team 和 tag/HEAD 固定配置，独立长期记忆先检查 Team 或其他候选。晚于 v0.3.3 的 Personal 关闭记忆代码与当前文档差异保留。OpenSuperBot 0.5.0 的旧 home 遮蔽差异已有静态修复，E08 改为复验新门槛；模型密钥持久路径与安全表差异继续待核。

OpenDots 审批恢复与外部去重分开，nanoMuse Skills 作用域和最新发行分开。商业对照增加 Muse Spaces 与 Max 网页 Teammates，Dots 工作区预览和 Duet 新重置条件同步到比较/价格/建议。E01–E12 沿用并修订，新增 E13–E16，全部尚未执行。

## 未解决项

- Personal 独立记忆代码、发行包和部分当前文档的对齐，Intelligence 评估许可与后端实际状态。
- OpenSuperBot 两平台 home/工具链/网络实测、Windows 文件边界、持久密钥路径、录制脱敏及迁移效果。
- nanoMuse 账号记录/训练/同步实际设置、导入与 Skills 即时失效、TestFlight 具体 build；OpenDots 结果丢失后的重复副作用。
- Dots 工作区实际权限/报价与 11 月 18 日安排，Duet 用量重置和各商业账号资格；Today 安装/签名与权益领取，Instinct 完整权限和 Cue 当前资格。
- 旧许可没有统一重审，截断文件清单没有作为完整代码审计。所有成功率、成本、跨天恢复与中文成绩仍待产品实验。

## 完整差异与检查

[manifest.json](manifest.json)固定基线、版本、文件哈希、证据、仓库/发行元数据和检查结果。[report.diff](report.diff)、[sources.diff](sources.diff)、[building-blocks.diff](building-blocks.diff)由基线提交的完整文件与本次完整文件生成。

差异用于审查和版本重建，检查在临时目录完成，历史文件不参与原地应用。统一差异中的空白上下文标记按原格式保留。

引用与来源身份、Markdown 本地链接/锚点/表格/围栏、26 仓与发行范围、manifest 哈希/行数、三份 diff 的临时重建和历史完整性均已通过。缓存已忽略，产品实测状态保持未执行。本次 11 个明确文件的暂存范围与 git diff --cached --check 也已通过，实际结果写入本批 manifest。

返回[当天批次](../README.md)、[所有归档日期](../../README.md)或[更新流程](../../../UPDATE-WORKFLOW.md)。
