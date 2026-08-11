#llm训练整体思路
整体思路包括三步：
 1、数据整理：数据整理包括两部分
 2、transformer架构搭建
 3、模型训练算法选择与执行



##数据 数据类型分为海量文本信息或海量QA对。
##模型 transformer架构中的decoder架构
##训练
###预训练 (Pre-training)：数据类型为海量文本信息。模型是transformer架构中的decoder架构。训练目标是根据输入的文本预测下一个token的生成
###sft（Supervised Fine-Tuning）监督微调：数据类型为海量QA对。模型是transformer架构中的decoder架构。训练目标是根据输入Q预测A的生成。
###最终模型
####PPO算法

####DPO算法
####GRPO算法