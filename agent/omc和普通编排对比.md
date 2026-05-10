🎯Skills-Behavior-Injection最终总结   必读

omc ---- ARCHITECTURE深度分析.md
### 10.3 与其他编排系统的区别

```
传统编排：
Orchestrator → Agent A → Agent B → Agent C → Done

OMC 编排：
用户输入 → Hook 检测 → Skill 选择 → Agent 组合 → 
上下文重置? → 恢复 State → 继续工作 → Done




Skills-Behavior-Injection深度解释.md


## 六、架构层面：Agent vs Skill vs Behavior

### 6.1 三层架构

```
┌────────────────────────────┐
│ Behavior Layer (行为)       │
│ ─────────────────────      │
│ Skill 注入这一层            │
│ • 阶段顺序                 │
│ • 循环次数                 │
│ • 并行策略                 │
│ • 验证规则                 │
└────────────────────────────┘
         ↓ (指挥)
┌────────────────────────────┐
│ Agent Layer (执行)          │
│ ─────────────────────      │
│ 19 个专门化 Agent          │
│ • 每个做一件事             │
│ • 职责明确                 │
│ • 可组合                   │
└────────────────────────────┘
         ↓ (驱动)
┌────────────────────────────┐
│ Tool Layer (工具)           │
│ ─────────────────────      │
│ Read, Edit, Write, Bash... │
└────────────────────────────┘
```