# Agent-Agnostic Coding Protocol V0

**P-01｜授权与权威**

项目产品要求、公共规则、Project Delta 和任务授权分别承担各自职责。实际授权必须覆盖对象、Scope／AC、Owner、动作、权限、预算和停止条件。技术能力、文件存在、Receipt 或质量 PASS 均不产生授权。

公共合同不覆盖产品承诺和有效任务例外。发生实质冲突时停止依赖步骤，由有权责任方处理；不能通过自行选择较低要求或额外叠加 Review 消除冲突。

**P-02｜交接与 Receipt**

交接包引用唯一权威来源，至少包含：

- Task、需求／AC、授权及后续更正；
- Owner、工作区、实际环境、允许动作与保护范围；
- Source Baseline、Dispatch HEAD、候选及输入身份；
- 必要检查、适用 Review、预算累计、停止条件和回传位置。

执行配置按三个时点区分：

- Prepare / Handoff：Planner 提供推荐的 Coding Agent、Runtime、Model 及必要的 Reasoning Effort，区分推荐值与 PO 已批准值并引用批准来源；尚不能确定时提供候选范围及待裁决事项。不要求预先取得尚未创建的 Session ID。
- PO Dispatch：PO 明确批准的执行配置或允许范围、Implementation Owner、授权动作及停止条件。Planner 的推荐不自动构成批准。
- Implementation Receipt：接收者核验实际 Coding Agent、Runtime、Model、Session、权限、工作区和有效授权，记录身份来源并核对批准约束，包括受约束的 Reasoning Effort。不符合批准约束时返回 BLOCKED，不自行更换受限制的配置。

Planner 返回 DISPATCH READY 时，同时提供：

1. Ready Report：准备完成及核验依据。
2. Launch Packet：完整、固定、可追溯的下游任务输入。
3. PO Dispatch Draft：PO 可直接复制转发的最小授权草稿。

Draft 可放在 Ready Report 回复末尾或现有 Launch Packet 内，不强制新增文件；仅包含接收者、待批准动作、固定 Handoff 引用和必要限制，不重复技术规格、预算明细与项目规则；预算和停止条件可引用固定 Launch Packet，不重复维护。Draft 明确标记 DRAFT / NOT DISPATCHED，不产生授权；只有 PO 审阅批准并实际发送后才构成 Dispatch。

尚未生成的 Session ID 不阻断 Prepare。接收者仍待指定时应如实标记，实际绑定后更新受影响的 Draft，不虚构身份；实际 Dispatch 时仍须明确接收者及批准配置。

凡现行 Workflow 中需要 PO 裁决并向下游 Agent 转发的交接，**交出本次结果的责任方必须在正常交付时，随现有交付物附上完整、最小、可直接转发的 PO Decision / Dispatch Draft**。Draft 写明接收角色、待批准动作、固定输入或候选、适用配置及必要限制。已有规格、证据、预算、停止条件和回传位置可用固定引用。确需 PO 选择时，上游列明选项和建议，PO 选定后由上游补齐受影响的正文。PO 只需审阅、批准和转发，无需编写 Prompt、补配参数或整理证据。

- **Planner** 在 Plan 交付中附下一步 Prepare 的 Decision Draft。在 `DISPATCH READY` 时沿用现有 Ready Report、Launch Packet 和实施 Dispatch Draft。需要独立 Review 时，由 Planner 给出 Reviewer 配置建议或待选范围，区分推荐值与 PO 已批准值。
- **Implementation Owner** 在 Result Package 中附首次送审 Draft。修复或补证后需要 PO 转交复核时，随同一次交付附复审 Draft，绑定实际候选、原 Finding 和相应证据。Reviewer 配置只引用 Planner 的建议或 PO 已批准的配置与来源，Implementation 不得自行选定或更换。Implementation 沿用既定 Review 计划，不重新规划 Review；配置或计划存在缺口时，列明待裁决事项并交回 Planner／PO。
- **Independent Reviewer** 在 Review Report 中附与结论相符的下一步 Draft。需要修复时引用 P-05 Repair Return，需要补证或恢复时引用已有的 P-07 Recovery Return；可接受且需下游集成或收尾时，给出供 PO 裁决的相应草稿。Reviewer 不得自行批准修复或集成。其他角色在 Receipt 等现有载体中触发同类交接时，由交出方随附 Draft。

集成及收尾责任方在需要 PO 决定并向下游转发时，随现有交付附下一步授权草稿，绑定实际集成结果、交付证据及待批准动作。

适用时，Draft 附经核验的 Agent 启动命令，注明目标工作区、执行配置、输入入口及核验依据与限制。命令应与推荐或已批准配置一致；参数核验与实际启动验证分别说明。无法核实时由上游说明缺口并补齐，不要求 PO 编写命令或补配技术参数。

Draft 标记 `DRAFT / NOT DISPATCHED`。PO 审阅批准并实际转发后，下游才按有效合同接收。已有授权足以继续、无需 PO 再次派发的动作，沿原授权执行。

接收者核对实际状态后返回 ACCEPTED 或 BLOCKED。**谁有权接受 Receipt，由有效项目／任务合同决定**；公共层同时容纳接收者接受和指定外部责任方接受，不统一改写为自接受。

**P-03｜候选身份**

Source Baseline 是判断累计变更范围的固定来源；Dispatch HEAD 是实际派发时的仓库版本，两者分别记录。

公共层支持完整 Commit，以及获准的冻结 Diff／Manifest。项目可以限制候选形式。候选必须覆盖实际变更、明确纳入的未跟踪输入、文件摘要和必要依赖；不能用 HEAD 掩盖 dirty 内容。

新候选重新绑定检查、Finding 和结论。相同 SHA 下输入发生变化属于漂移，不能按“仅补证”处理。

**P-04｜Review 与 Evidence**

是否需要 Review、是否允许子审、具体独立性要求和接受责任，由有效项目／任务合同决定。两层 Review 都被要求时，分别交证，不互相抵充；不能因公共合同描述了接口而新增一轮审查。

三种模式分别声明：

- **盲审**：首轮结论封存前不接收实现者推理或其他审查发现。
- **披露式独立 Review**：披露已知 Finding 或修复声明，Reviewer 仍独立核验。
- **定向复审**：围绕指定 Finding、变更和受影响回归复核，同时满足原合同仍要求的检查。

执行身份追溯适用于 Planner、Implementation Owner、Reviewer 等实际执行角色。统一记录实际 Agent、Runtime、Model、Session、适用的 Reasoning Effort、输入、权限、覆盖和限制。身份字段按证据区分原生核验、可靠引用、执行者自报与 UNKNOWN，保留可定位来源及限制；推荐值、批准值或配置声明不冒充实际运行证据。角色名、工具名或新会话本身不能代替证据。亲自执行、引用日志、待验证主张分别标记；未知身份、成本和未运行检查如实保留。

Session 优先记录原生 ID 及来源；不具备原生 ID 时，允许使用可靠的 Task / Conversation 引用，不要求 Codex 式 Session UUID。无可靠来源时保留 UNKNOWN，依据有效任务的身份与独立性要求判断能否继续；必要条件无法核验时返回 BLOCKED。Session ID 不等同于 Implementation Owner，也不自动产生授权。

Agent、Runtime、Model、Session 或受约束的 Reasoning Effort 发生变化时，在现有任务记录中增量记录变更前后真实身份、来源、执行区间及授权影响，保留历史。原授权仍有效且实际条件满足时，仅补受影响核验；超出授权范围时停止受影响动作并取得必要批准，不默认完整 Prepare。预算仍按 P-06 累计；Review 的独立性及会话策略仍沿有效项目／任务合同。

**P-05｜Repair Return**

正式 Independent Review 返回 FAIL 时，在原 Review Report 或交付摘要中提供可直接引用的 Repair Return，至少包含：

1. 稳定 Finding ID 和原始报告引用；
2. 受审候选身份及 Review Subject；
3. 对应 Requirement／AC／Criterion；
4. 实际失败行为、复现步骤、环境和证据；
5. 期望行为及接受条件；
6. 必要修复范围及受影响回归检查；
7. 未解决的授权、Owner、权限、预算等阻塞。

无法复现或证据不完整时明确标记缺口；建议与已确认 Finding 分列。Repair Return 引用原 Finding 真源，不建立第二份问题账本，不改写原始证据。

Repair Return 不授予写权限、不解除 BLOCKED。接收修复时仍须核验当前候选、工作区、授权覆盖及预算。修复后关联原 Finding、新候选、修复证据和必要回归；复验沿有效送审授权执行，不继承旧候选整体 PASS。

**P-06｜预算与停止**

各侧从首个获授权任务动作起算，包含必要读取、接收、检查及交证。失败、重试、修复、换会话／工具／候选均累计，不重置。

实施及其内部 Review、另行独立验收、规划分别按批准额度管理。保护必要验证与收尾预留，不自行转额；预留不等于启动权限。

同一主体重叠去重，不同主体累计与整体墙钟分列；父汇总已含子用量时不重复计入。等待不冒充主动工时，未知在途消费不提前释放。下一动作及必要收尾无法获得预算覆盖时停止。

**P-07｜判定与历史保护**

BLOCKED 表示执行／接收受阻，与质量 PASS／FAIL／UNKNOWN 分轴。必要条件已证实失败为 FAIL；无有效 FAIL 但必要证据不足为 UNKNOWN；必要条件全部有最终候选证据才可 PASS。

仅在必要条件缺失、阻断后续动作或需要下游继续处理时，对 UNKNOWN／BLOCKED 项在现有 Receipt、Review Report 或 Result Package 中提供可直接引用的 Recovery Return。非阻断性的 UNKNOWN 观测不单独触发恢复交接。Recovery Return 至少包含：

1. 受影响 Task、候选、Review Subject 和 Criterion；
2. 已确认事实、缺失证据或阻断原因；
3. 需要补充的内容和具体动作；
4. 负责提供、处理或裁决的角色；
5. 恢复条件、必要授权、权限和剩余预算；
6. 恢复后需要执行的接收核验、检查或复验范围；
7. 恢复类型：同候选补证、环境恢复、修复新候选，或需要新的批准／准备。

候选、Review Subject、Criterion 等字段按实际阶段适用；尚未形成的对象明确标记 N/A 并说明原因，不虚构身份。其他无法确认的信息保留 UNKNOWN，不虚构责任人或恢复条件。

Recovery Return 是现有交付报告内的交接内容，不新增 Workflow 阶段或独立管理系统，也不产生实施、修复、复审或恢复授权。原 Scope／AC、Owner、环境、权限、有效授权及预算仍满足要求时，只补受影响的核验，不强制重新执行完整 Prepare；实质变化只补必要的批准或准备。候选重新绑定、Review 独立性及预算累计分别沿 P-03、P-04、P-05、P-06，原始证据和历史裁决保持不变。

范围内结果与联合 Gate 分列。范围外缺口是否构成整体门槛，依据有效合同判断，不能仅因“范围外”而忽略。

新公共版本只在明确采用边界生效，不追溯改变历史 Review、在途任务、预算、候选形式或既有例外。
