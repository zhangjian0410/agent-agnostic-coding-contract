# Version & Provenance

**状态：V0（执行身份与交付完整性修订）已完成本地生效核验，并经独立 PO 授权远端发布。** 原实施授权仅覆盖限定实施、检查、实际只读独立复核、Finding 处置、轻量 Eval、本地 Commit 和符合条件的 main Fast-forward；原授权与核验记录保留于[原本地 Result Package](/Users/archer/Documents/Codex/outputs/agent-agnostic-coding-contract-v0-20261101/execution-identity-handoff-patch-01/RESULT.md)。精确候选 `49625cab3c6d5e652257c3e8e33c963ce6266925` 后经独立 PO 发布授权推送至现有私有 origin/main，远端及四文件摘要回读见[发布回执](/Users/archer/.codex/visualizations/2026/11/01/01a1959f-ad7a-7800-8690-f671a601e34e/aac-publication-receipt-49625ca.md)。项目采用须分别批准；本次状态勘误不验证或授予 Contract GA。本文件记录来源和维护机制，不建立第二份项目 Delta、任务规格或 Finding 真源。

## 设计及落地依据

初始 V0／HE-01 建设会话：01a194c1-0f2f-7571-8407-1fae97343b1a。本次修订维护会话：01a1959f-ad7a-7800-8690-f671a601e34e。

| 依据 | 固定记录 |
|---|---|
| 已批准精简 Architecture Decision Pack | message msg_037dd8500c6ce81e016ae6aa660aa08191b018b9171713ab46；原文快照 SHA-256 c8f147261aa9186d9eb42f74e9932f36e1496259a83d21091370540878644260 |
| PO Architecture Closure | message msg_01a1950c-6e53-7c70-820d-0c44a8126ebe；确认两份公共契约、Delta 划分及版本治理，未恢复原 P1 |
| PO Repair Return 补充 | message msg_01a194e8-5c84-7480-925a-9aa0ef259e01；已纳入批准正文 P-05 |
| 本次四文档落地授权 | message msg_01a19511-bc09-7450-9b23-c9b16ba49159；AAC-V0-DOCS-AUTH-01 |
| PO 最小 Git 集成与版本生效批准 | message msg_01a1951e-96e9-7c23-86cb-4fcb1bbce7a1；PO Decision｜AAC-V0 · Main Integration & Version Activation；最终身份及检查回执保存于原 Result Package |
| PO HE-01 最小修订及版本生效批准 | message msg_01a19549-b53a-7f73-a96b-0e1dbb7ecb56；PO Decision｜AAC-V0 · HE-01 Minimal Patch & Activation；固定基线 0fe6b520ebb089b7402827f1c0015c63e8e8b1ef；仅 P-07 Recovery Return 正文及必要版本说明 |
| PO 执行身份与交付完整性修订批准 | message msg_01a19628-7fa8-7622-b595-6c31d346a3a0；PO Decision｜AAC · Execution Identity & Handoff Completeness Patch；固定基线 0f5e9f4f89631163fe5c62c1efe59590667dac73；仅 P-02、P-04 及必要版本说明，35 分钟独立任务额度；只授权本地集成与条件式生效 |
| PO 精确候选远端发布批准 | message msg_01a1963a-baba-7d30-8e45-df281b1bb79c；仅批准 `49625cab3c6d5e652257c3e8e33c963ce6266925` 推送至现有私有 origin/main，前置远端基线 `0f5e9f4f89631163fe5c62c1efe59590667dac73`；回读与摘要见发布回执；不含 Tag、Release 或项目升级 |
| PO 版本状态勘误批准 | message msg_01a19673-9c8b-7d32-b5b5-fd72f91413a4；PO Decision｜AAC · Version State Metadata Reconciliation；仅 README.md、PROVENANCE.md 状态及必要来源引用，独立预算 10 分钟、最后 3 分钟保护核验与交证；允许核验后的本地 Commit 与非强制 Push；不含公共规则修改、Contract GA 或项目采用 |

初始 V0 的原生记录、完整批准原话及快照绑定保存在 [初始任务 SOURCE-BINDINGS.json](/Users/archer/Documents/Codex/outputs/agent-agnostic-coding-contract-v0-20261101/minimal-docs-01/SOURCE-BINDINGS.json)。这是本机证据路径，其他环境不可访问时保留证据缺口，不把路径本身当作核验结果。

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
| P-07 | 两项目证据判定、历史兼容性和已批准 ADP；本次 PO 批准的 HE-01 Recovery Return 补充 |

Project Delta 划分与差异分析保留在 [已批准 ADP 原文第三部分](/Users/archer/Documents/Codex/outputs/agent-agnostic-coding-contract-v0-20261101/minimal-docs-01/inputs/approved_adp.md)。项目内维护自身 Delta，公共仓库不复制其现行规则正文。童迹 C 的单 Reviewer、禁子审、Manifest 候选及外部 Receipt 接受等继续沿任务级合同，不提升为所有童迹任务默认值。

## 最小版本与采用机制

1. **唯一权威。** 独立私有 agent-agnostic-coding-contract Repo 持有公共 WORKFLOW 与 PROTOCOL，PO／Archer 负责版本批准。本次批准仅使独立 Repo 中的公共 V0 在最终核验通过后生效，项目现行合同继续有效。
2. **固定版本。** 用 PO 明确批准的完整 Commit 和内容摘要识别公共版本。项目持有固定快照及版本引用，不跟随 latest；快照是分发副本，不在项目内另改公共正文。本有效版本的摘要清单由 Result Package 保存，不新增机器接口或发布机制。
3. **Delta 只写差异。** 项目记录所针对的公共版本／条款、保留或收紧内容、原因和批准来源；入口引用公共合同、Delta 和任务授权，不重复公共规则。任务级例外继续由有效任务授权控制。
4. **受控升级。** 公共变更说明条款差异、兼容性和受影响项目。项目核对本地 Delta 后决定采用，记录批准及适用新任务起点；公共更新不自动升级项目或迁移在途任务。
5. **防止漂移。** 在采用、升级和实际任务交接时核对固定引用与 Delta。冲突只处理受影响部分；共同修订回公共源，项目特例留 Delta。沿既有任务记录留证，不另建平台、定期强制 Review 或新增质量门禁。
6. **来源与未知。** 区分项目原条款、PO 决定和公共抽象。历史 Workflow origin 无法证实则保持 UNKNOWN，不能用 OpenSpec 工具版本推断。

## 历史与证据边界

本次版本状态勘误以已发布的 `49625cab3c6d5e652257c3e8e33c963ce6266925` 为基线，仅修正 README.md、PROVENANCE.md 的发布状态及来源引用；WORKFLOW.md、PROTOCOL.md 保持原字节。原本地授权、独立发布授权及历史交付证据保留；下述“本次修订”仍指原执行身份与交付完整性修订。本次勘误的最终 Commit、准确 Diff、Gate、四文件摘要和远端回读见[独立 Result Package](/Users/archer/.codex/visualizations/2026/11/01/01a1959f-ad7a-7800-8690-f671a601e34e/aac-version-state-metadata-01/RESULT.md)。墨水星球 B1、童迹 B2 的固定公共版本、候选、预算、授权和历史证据不变。

本次修订在 P-02 统一执行配置三个时点及 DISPATCH READY 三项交付，在 P-04 明确全部实际执行角色的身份来源和配置变更追溯。WORKFLOW 及 P-01、P-03、P-05 至 P-07 保持上述基线原字节。原生批准、实际 Diff、只读 Review、Eval、最终本地候选和预算保存在本次 Result Package。First Review／Re-review 策略保持有效项目／任务合同；B1 不追补历史 Draft、不重复派发；B2 下一次有效 Ready 的三项交付沿 PO 任务决定落实。项目现行授权、Receipt、预算及候选不变，新公共修订不自动被项目采用。

以下两段保留 HE-01 及初始 V0 的历史范围说明，其中“本次”指各自历史阶段，不作为当前修订范围声明。

本次 HE-01 修订仅在 P-07 增加有条件触发的 Recovery Return，并更新必要版本与批准说明。WORKFLOW 及 P-01 至 P-06 保持基线字节。以下首段保留初始 V0 落地时的历史范围，不作为本次 PROTOCOL 未变的声明。

本次只把已批准文字落地，WORKFLOW 和 PROTOCOL 正文逐段保留批准原文，仅增加文档标题。旧 14 文件工程草稿、AC、BLOCKED、Receipt 02、权限预检、UNKNOWN、Review 与预算记录均为历史证据，未被本次落地覆盖或重新裁决。未实施 Schema、校验器、自动化测试、Runtime Profile、跨项目接入、正式 Review 或项目采用。

已核实的来源版本不能证明历史 Workflow 的最初出处、未来运行效果或跨 Harness 加载。原联合 Gate／DM 缺口及其他在途任务状态保持原合同。
