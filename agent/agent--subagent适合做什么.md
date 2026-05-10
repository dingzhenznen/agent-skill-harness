https://mp.weixin.qq.com/s/cIQYl9Wr1Eov4ma-_bYh-w?scene=1



一、Agent Loop 的基本运转方式

二、为什么 Harness 比模型更关键
三、上下文工程为什么决定稳定性
四、工具设计决定 Agent 能做什么
五、记忆系统如何设计
七、多 Agent 如何组织


子 Agent 适合做什么

子任务里的搜索、试错和调试过程，不该污染主 Agent 的上下文，主 Agent 真正需要的只是结论，探索细节留在子 Agent 自己的消息历史里。

多agent 编排

1  oh-my-claude  通过提示词注入 让 主agent 来做编排
   2 使用skill 的时候 通过skill 提示词来注入  实现技能编排
  
2  agency-agent 创建一个 编排agent ,通过提示词来 切换到这 编排agent
3  superpower 通过skill 注入提示词来编排


为什么多 agent  
比如 omy-claude  的工作原理

### Typical Agent Workflow

```
explore --> analyst --> planner --> critic --> executor --> verifier
(discover)  (analyze)   (sequence)  (review)   (implement)  (confirm)
```

explore 搜索会上下文爆炸
必须要隔离
