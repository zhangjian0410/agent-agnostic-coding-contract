# Agent-Agnostic Coding Workflow / Protocol V0

**状态：首个公共有效 V0。** 依据 PO Decision｜AAC-V0 · Main Integration & Version Activation，在最终 Commit、四文件摘要、实际差异及分支状态全部核验通过后生效；最终版本身份见本次 Result Package。墨水星球、童迹或其他项目的采用仍须分别批准。

本仓库是公共契约的单一维护源，Repo Owner 为 PO／Archer。公共契约只维护跨项目共性；Project Delta 在各项目内维护，任务级例外继续由有效任务授权控制。项目现行合同在明确采用前保持有效。

## 文档入口

| 文档 | 职责 |
|---|---|
| [WORKFLOW.md](WORKFLOW.md) | 公共角色、既有阶段及转换、必要／可选步骤、修复返回和停止机制 |
| [PROTOCOL.md](PROTOCOL.md) | P-01 至 P-07：授权、交接、Receipt、候选、Review、Evidence、Repair Return、预算与历史保护 |
| [PROVENANCE.md](PROVENANCE.md) | 批准与来源、规则提炼映射、固定版本及项目受控采用机制、UNKNOWN |

## 使用边界

本 V0 已获 PO 条件式生效批准；完成本次授权要求的最终核验后，以 Result Package 中的完整 Commit 和四文件 SHA-256 固定版本。后续公共版本仍须由 PO 明确批准并固定。阅读本仓库、出现本地 Commit、分支名称或文档检查通过，不产生实施、Review、集成、发布或项目采用权限。实际任务仍核对已采用公共版本、项目 Delta 和有效任务授权。

本次仅落地上述公共契约及来源说明。项目 Delta 正文、项目入口及采用记录未修改；原 14 文件工程方案保持暂停。这里不包含 Schema、通用校验器、自动化测试框架、Runtime Profile 或执行引擎，也不声称跨 Harness 加载验证通过。

## 候选身份

候选完整 Commit、四文件 SHA-256、写回与检查证据及预算保存于仓库外的本次 Result Package。文档不嵌入自身摘要或尚未产生的候选 Commit，避免循环绑定。公共版本的生效决定与项目采用决定分别记录。
