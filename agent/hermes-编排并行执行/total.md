一. 创建三个专家 profile
快速演示，直接克隆主智能体的配置文件，大家也可以选择不  clone，手动进行配置
hermes profile create coder --clone
hermes profile create writer --clone
hermes profile create analyst --clone

每个命令执行后，Hermes 会自动注册同名快捷命令（coder / writer / analyst）


二. 更新 Agent 的 SOUL.md



三. 一个复合任务，并行调度三个专家

我下周要做一个内部分享，主题是"用 AI 提升团队效率"。帮我准备三样东西：一个 Python 自动化脚本做案例演示，一段 200 字的开场介绍文案，再帮我分析一下这组数据——引入 AI 工具前后的工单处理量：引入前月均 320 单，引入后月均 580 单，共 6 个月数据分别是 310、325、330、540、600、580。