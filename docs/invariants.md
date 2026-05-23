# 硬约束

Owner: `One Person Lab`
Purpose: `invariants`
State: `active_truth`
Machine boundary: 本文是人读硬约束；守门以测试和 review 执行。

1. 本仓只治理开发相关文档生命周期和工程闭环。
2. 不替代任何 domain repo 的 truth、quality verdict、artifact authority 或 owner receipt。
3. OPL series 文件治理不迁移到 OpenArc/OpenSpec/Spec Kit 默认路径。
4. active docs 是当前唯一 Active Truth 的重写面，表达当前完成进度、当前差距和下一轮 Agent prompt；过程材料进入 history；退役内容进入 tombstone/provenance。
5. 已退役模块、接口、测试和文档入口不保留兼容 alias。
6. Markdown 完整性不能替代 contracts、tests、CLI/read-model 或 runtime ledger。
7. doctor 默认只读，不能写目标 repo。
8. repo-native 指读取目标 repo 自己已有的开发入口，不指向目标 repo 安装本仓 CLI 或生成治理工具目录。
9. OPL family 自动开发治理必须把 ideal-state reference 当输入，把当前完成进度、现状与理想态差距、下一轮 Agent prompt 当派生输出；不能让用户手工维护这些派生状态。
10. active docs 不能保存执行日志、时间线、完成流水或长历史清单；这些内容只能压缩进入 history/tombstone，以免污染 Active Truth。
