# 架构

Owner: `One Person Lab`
Purpose: `architecture`
State: `active_truth`
Machine boundary: 本文是人读架构；可执行行为以 `scripts/opl_doc_doctor.py` 和 skill 为准。

## 分层

1. Skill 层
   - 给 Codex 提供文档生命周期工作流、OPL series治理规则和硬边界。
2. Doctor 层
   - 只读扫描 repo docs，输出 profile、repo-native surfaces、canonical docs 状态和轻量 findings。
3. Repo-native surface 层
   - 识别目标 repo 自己已有的 agent guidance、canonical docs、machine truth surface 和验证入口，不向目标 repo 安装治理工具。
4. Change packet 层
   - 为非平凡开发提供 active change 包，完成后 fold back 到 canonical docs 或 history。
5. Verification 层
   - 通过 repo-native 测试、diff check、doctor 输出和最终 main checkout 验证闭环。

## 自动开发文档回路

用户只需要维护 ideal-state / target-state reference。治理流程必须从 live source、contracts、tests、CLI/read-model 和当前 docs 中重写三个派生输出：当前完成进度、现状与理想态差距、下一轮 Agent prompt。通常落点是各 repo 的 single Active Truth plan；若 repo 使用其他 canonical active plan，需要显式映射，不能新增第二套计划文档。

当目标 repo 缺少稳定 active owner 时，skill 可使用 `templates/active-truth-plan.md` 的最小形状：ideal-state reference、current completion progress、functional/structural gaps、test/evidence gaps、next-round Agent prompt 和 history/tombstone foldback。该模板只定义文档形状，不承担语义判断。

CLI 不承担 Active Truth 语义治理。doctor 只提示明显结构风险；真正的文档内容判断由 Codex 按 skill 读取 live repo truth、ideal-state reference、active plan 和 machine-readable evidence 后执行。

## 边界

doctor 只读，不执行清理、不修改目标仓、不生成 owner receipt。skill 可以指导 Codex 修改目标仓文档，但必须先读取目标 repo 约束并运行对应验证。
