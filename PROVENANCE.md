# Version & Provenance

**状态：首个公共有效 V0。** 本次 PO 已批准最小 Git 集成及条件式版本生效；最终 Commit、四文件摘要、实际差异、工作区和分支状态全部核验通过后，以 Result Package 记录的完整 Commit 识别本版本。 本文件记录来源和维护机制，不建立第二份项目 Delta、任务规格或 Finding 真源。

## 设计及落地依据

当前会话：01a194c1-0f2f-7571-8407-1fae97343b1a。

| 依据 | 固定记录 |
|---|---|
| 已批准精简 Architecture Decision Pack | message msg_037dd8500c6ce81e016ae6aa660aa08191b018b9171713ab46；原文快照 SHA-256 c8f147261aa9186d9eb42f74e9932f36e1496259a83d21091370540878644260 |
| PO Architecture Closure | message msg_01a1950c-6e53-7c70-820d-0c44a8126ebe；确认两份公共契约、Delta 划分及版本治理，未恢复原 P1 |
| PO Repair Return 补充 | message msg_01a194e8-5c84-7480-925a-9aa0ef259e01；已纳入批准正文 P-05 |
| 本次四文档落地授权 | message msg_01a19511-bc09-7450-9b23-c9b16ba49159；AAC-V0-DOCS-AUTH-01 |
| PO 最小 Git 集成与版本生效批准 | message msg_01a1951e-96e9-7c23-86cb-4fcb1bbce7a1；PO Decision｜AAC-V0 · Main Integration & Version Activation；最终身份及检查回执保存于原 Result Package |

原生记录、完整批准原话及快照绑定保存在 [本任务 SOURCE-BINDINGS.json](/Users/archer/Documents/Codex/outputs/agent-agnostic-coding-contract-v0-20261101/minimal-docs-01/SOURCE-BINDINGS.json)。这是本机证据路径，其他环境不可访问时保留证据缺口，不把路径本身当作核验结果。

## 项目来源与提炼映射

| 来源 | 固定身份与文件 | 用途 |
|---|---|---|
| 墨水星球 | Commit d33bb7ed97daa29fdf8432a8ce854af72fa4b51c；AGENTS.md、docs/planning/IMPLEMENTATION_HANDOFF.md | 角色、阶段授权、工作区交接、候选、两层 Review 的项目要求、预算和修复重交 |
| 童迹 | 冻结 Manifest SHA-256 e510804cd18cdaada65a705d5bc8454824867040dc5486e0ec28478ea557a1eb；Source Baseline 31e9a689e8d69097a399add0b628fbc12a84c08d | AGENTS、delivery-workflow、verification、product-governance、native-workflows 的公共职责及项目差异 |
| AIOS 预算／修复合同，补充来源 | Commit 95e31a9ec82b2702a4a8a05dcc49ec3f7f63dc6e；rules/coding-verification.md、config/coding-workflow-protocol.json | 已批准的预算累计、预留、去重及修复交接语义；不作为第二个公共维护源 |
| PO 已确认 V0 R1 与精简 ADP | 以上批准记录及原文快照 | Review 适用性、三种模式、历史保护、单一权威和受控采用 |

来源文件的逐项摘要及本次比对见 [source-verification.json](/Users/archer/Documents/Codex/outputs/agent-agnostic-coding-contract-v0-20261101/minimal-docs-01/checks/source-verification.json)。来源候选不等于已生效公共版本；抽象后的公共正文由本仓库单独维护。

| 公共内容 | 提炼依据 |
|---|---|
| WORKFLOW；P-01、P-02 | 两项目的角色、阶段和交接；保留各自 Receipt 接受方式 |
| P-03 | 两项目候选交付；公共支持 Commit 与 Diff／Manifest，项目限制留 Delta |
| P-04 | 两项目验证合同及 V0 R1：Review 是否必需、层次和独立性沿有效项目／任务合同 |
| P-05 | PO Repair Return 补充及既有 Repair-to-Review Fast Path |
| P-06 | 两项目预算约束及已批准预算合同 |
| P-07 | 两项目证据判定、历史兼容性和已批准 ADP |

Project Delta 划分与差异分析保留在 [已批准 ADP 原文第三部分](/Users/archer/Documents/Codex/outputs/agent-agnostic-coding-contract-v0-20261101/minimal-docs-01/inputs/approved_adp.md)。项目内维护自身 Delta，公共仓库不复制其现行规则正文。童迹 C 的单 Reviewer、禁子审、Manifest 候选及外部 Receipt 接受等继续沿任务级合同，不提升为所有童迹任务默认值。

## 最小版本与采用机制

1. **唯一权威。** 独立私有 agent-agnostic-coding-contract Repo 持有公共 WORKFLOW 与 PROTOCOL，PO／Archer 负责版本批准。本次批准仅使独立 Repo 中的公共 V0 在最终核验通过后生效，项目现行合同继续有效。
2. **固定版本。** 用 PO 明确批准的完整 Commit 和内容摘要识别公共版本。项目持有固定快照及版本引用，不跟随 latest；快照是分发副本，不在项目内另改公共正文。本有效版本的摘要清单由 Result Package 保存，不新增机器接口或发布机制。
3. **Delta 只写差异。** 项目记录所针对的公共版本／条款、保留或收紧内容、原因和批准来源；入口引用公共合同、Delta 和任务授权，不重复公共规则。任务级例外继续由有效任务授权控制。
4. **受控升级。** 公共变更说明条款差异、兼容性和受影响项目。项目核对本地 Delta 后决定采用，记录批准及适用新任务起点；公共更新不自动升级项目或迁移在途任务。
5. **防止漂移。** 在采用、升级和实际任务交接时核对固定引用与 Delta。冲突只处理受影响部分；共同修订回公共源，项目特例留 Delta。沿既有任务记录留证，不另建平台、定期强制 Review 或新增质量门禁。
6. **来源与未知。** 区分项目原条款、PO 决定和公共抽象。历史 Workflow origin 无法证实则保持 UNKNOWN，不能用 OpenSpec 工具版本推断。

## 历史与证据边界

本次只把已批准文字落地，WORKFLOW 和 PROTOCOL 正文逐段保留批准原文，仅增加文档标题。旧 14 文件工程草稿、AC、BLOCKED、Receipt 02、权限预检、UNKNOWN、Review 与预算记录均为历史证据，未被本次落地覆盖或重新裁决。未实施 Schema、校验器、自动化测试、Runtime Profile、跨项目接入、正式 Review 或项目采用。

已核实的来源版本不能证明历史 Workflow 的最初出处、未来运行效果或跨 Harness 加载。原联合 Gate／DM 缺口及其他在途任务状态保持原合同。
