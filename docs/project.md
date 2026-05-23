# 项目概览

Owner: `One Person Lab`
Purpose: `project`
State: `active_truth`
Machine boundary: 本文是人读项目定位；机器真相以 `.codex-plugin/plugin.json`、`skills/opl-doc-governance/SKILL.md`、`scripts/opl_doc_doctor.py` 和测试为准。

`opl-doc-governance` 是 OPL-native 开发文档生命周期治理工具。它的目标是让 AI 在长时间自主软件开发中稳定维护当前唯一 Active Truth：理想目标由用户维护，当前完成进度、现状与理想态差距、下一轮 Agent prompt、文档分层、退役规则、验证闭环和归档策略由治理流程根据 live repo truth 刷新。

本仓提供：

- Codex plugin manifest。
- `opl-doc-governance` skill。
- 只读 CLI doctor。
- OPL series 文档治理 workflow，默认覆盖 OPL、MAS、MAG、RCA、OMA，并可扩展到其他 OPL-compatible repo。
- 自动开发文档回路：用户维护理想态，治理流程根据 live repo truth 自动刷新完成进度、差距和下一轮 Agent prompt。
- Active Truth plan 推荐模板：当目标 repo 没有稳定 active owner 时，给当前完成进度、功能/结构差距、测试/证据差距、下一轮 Agent prompt 和 foldback target 一个最小形状。
- 轻量 doctor guard：只提示结构风险；Active Truth 内容治理由 Codex 按 skill 和 live repo truth 主动判断。
- 测试覆盖。

本仓不持有 OPL series 的 domain truth、runtime truth、quality verdict、artifact authority 或 owner receipt。
