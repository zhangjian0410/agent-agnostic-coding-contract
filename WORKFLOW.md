# Agent-Agnostic Coding Workflow V0

本 Workflow 规定角色、阶段转换和交接责任。具体工具、模型、工作区及执行方法由有效项目／任务合同确定。

四类职责为：**PO／授权责任方**决定范围、权限、预算和裁决；**Planner**形成计划并完成获准准备；**Implementation Owner**承担唯一实施写入责任；**Independent Reviewer**在获准范围独立审查，不参与受审候选实现。角色可以跨工具承担，工具名称不代表资格或授权。

沿用既有阶段，不增加新阶段：

| 阶段 | 完成条件与交接 | 权限边界 |
|---|---|---|
| Plan | 引用权威需求和 AC，明确范围、依赖、风险及方法 | 计划不授予准备或实施权限 |
| Prepare | 完成获准且必要的准备，交付真实 Ready Report 和交接包 | 已有有效准备可以复用；不强制重建 Issue、Worktree 或材料 |
| Dispatch | 授权方确定接收者、范围、运行方式、预算和停止条件 | 准备完成不等于派发；人工转发是有效方式 |
| Implement | 按项目规定取得 Receipt ACCEPTED，再实施、检查并交付绑定候选的 Result Package | 不扩大 Scope／AC，不自动集成、发布或进入下一任务 |
| Review | **仅在有效合同要求且已授权时执行**；交付逐项结论、Finding 和证据 | 不取得修复或后续派发权限；PO 作最终裁决 |

Receipt、Result Package、Repair Return 是阶段内的交接内容，不另设阶段。

必要步骤是：确认权威需求与授权、核验接收条件、控制唯一写入责任、完成适用检查、固定候选并如实交证。独立 Review 的适用性及层次沿项目／任务合同。TDD、Matt、Superpowers、Orca、子 Agent 等属于受控方法选择，不成为公共强制路线。

正式 Review 返回 FAIL 后，按 Protocol 提供 Repair Return。原 Scope／AC、Owner、授权、环境、权限和预算仍有效时，PO 可直接交回原 Implementation Owner；接收者核验后修复、形成新候选并按有效送审授权复验。仅因 SHA 改变，不重新执行完整 Prepare。实质变化只补受影响的准备或批准。

授权撤销、候选／输入漂移、并发 Writer、必要权限或证据缺失、预算不足时，停止受影响动作并交证。保留当前文件、候选、原始结果和进程状态；停止不自动触发清理、替代派发或续额。
