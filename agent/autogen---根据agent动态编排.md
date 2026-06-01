magicone 

根据task  创建 fact 然后创建 plan,
根据plan 动态选择下一个 agent plan,
然后判断 任务是否执行 完成以及下一步使用哪个 agent


1. team.run(...) / run_stream(...)
  2. MagenticOneOrchestrator.handle_start()
  3. 生成 facts
  4. 生成 plan
  5. _reenter_outer_loop()
  6. 广播完整 ledger：task + facts + plan + team
  7. 第一次 _orchestrate_step()
  8. orchestrator 生成 progress_ledger
  9. 如果未完成，发出 instruction_or_question
  10. 选中 next_speaker
  11. 给这个 agent 发 GroupChatRequestPublish()
  12. agent 开始基于“ledger + 当前指令”产出回复
  13. handle_agent_response()
  14. 把 agent 回复写入 _message_thread
  15. 再次 _orchestrate_step()
  16. orchestrator 基于最新线程重新判断：
      - 是否完成
      - 是否卡住
      - 下一步让谁做什么
  17. 重复 9-16，直到结束