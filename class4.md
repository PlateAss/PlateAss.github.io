# 第四课:XTuner 大模型单卡低成本微调实战
1. Finetune简介
两种微调模式：
- 增量预训练：让模型学到新知识
- 指令跟随：学会对话
2. 指令跟随微调的角色：
- System：上下文
- User:提问者
- Asistant：AI
不同大语言模型对话模板不同
3. 增量预训练微调
System和User留空，只需要Asistant
4. LoRA & QLoRA
LoRA不更新底模。
QLoRA量化4-bit，自动在cpu和gpu之间调度
5. XTuner
支持多个大预言模型
6. 快速上手
