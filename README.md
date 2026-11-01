# Agent-Agnostic Coding Workflow / Protocol V0

**状态：V0（执行身份与交付完整性修订）已完成本地生效核验，并经独立 PO 授权远端发布。** 原 PO Decision｜AAC · Execution Identity & Handoff Completeness Patch 仅批准本地实施与条件式生效，核验及候选身份保留于[原本地 Result Package](/Users/archer/Documents/Codex/outputs/agent-agnostic-coding-contract-v0-20261101/execution-identity-handoff-patch-01/RESULT.md)。后续独立发布授权已将精确候选 `49625cab3c6d5e652257c3e8e33c963ce6266925` 推送至 GitHub 私有仓库 main，并完成远端及四文件摘要回读，见[发布回执](/Users/archer/.codex/visualizations/2026/11/01/01a1959f-ad7a-7800-8690-f671a601e34e/aac-publication-receipt-49625ca.md)。项目采用仍须分别批准；远端发布和本次状态勘误均不构成 Contract GA 通过结论。

本仓库是公共契约的单一维护源，Repo Owner 为 PO／Archer。公共契约只维护跨项目共性；Project Delta 在各项目内维护，任务级例外继续由有效任务授权控制。项目现行合同在明确采用前保持有效。

## 文档入口

| 文档 | 职责 |
|---|---|
| [WORKFLOW.md](WORKFLOW.md) | 公共角色、既有阶段及转换、必要／可选步骤、修复返回和停止机制 |
| [PROTOCOL.md](PROTOCOL.md) | P-01 至 P-07：授权、交接、Receipt、候选、Review、Evidence、Repair Return、预算与历史保护 |
| [PROVENANCE.md](PROVENANCE.md) | 批准与来源、规则提炼映射、固定版本及项目受控采用机制、UNKNOWN |

## 使用边界

本地生效与远端发布分别依据原实施授权和后续精确候选发布授权，原授权边界及历史记录保持不变。本次只勘误版本状态和来源引用；勘误 Commit 不产生新的公共规则，不改变任何项目的固定采用版本。后续公共版本仍须由 PO 明确批准并固定。阅读本仓库、出现本地 Commit、分支名称或文档检查通过，不产生实施、Review、集成、发布或项目采用权限。实际任务仍核对已采用公共版本、项目 Delta 和有效任务授权。

本次仅落地上述公共契约及来源说明。项目 Delta 正文、项目入口及采用记录未修改；原 14 文件工程方案保持暂停。这里不包含 Schema、通用校验器、自动化测试框架、Runtime Profile 或执行引擎，也不声称跨 Harness 加载验证通过。

## 候选身份

候选完整 Commit、四文件 SHA-256、写回与检查证据及预算保存于仓库外的本次 Result Package。文档不嵌入自身摘要或尚未产生的候选 Commit，避免循环绑定。公共版本的生效决定与项目采用决定分别记录。
