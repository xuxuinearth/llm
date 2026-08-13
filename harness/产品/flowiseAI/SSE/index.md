#各类SSE事件明细

| 序号 | 事件名称 | 范围 | 标识 | 简要说明 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | streamCustomEvent | - | - | 自定义事件 | |
| 2 | streamStartEvent | 单 | start | 单智能体开始 | |
| 3 | streamTokenEvent | 单多 | token | 输出token信息 | |
| 4 | streamSourceDocumentsEvent | 单多 | sourceDocuments | 检索到的文档片段 | |
| 5 | streamArtifactsEvent | 单多 | artifacts | 图片/工件输出 | 无法验证 |
| 6 | streamUsedToolsEvent | 单多 | usedTools | 使用工具 | |
| 7 | streamCalledToolsEvent | 多 | calledTools | agent节点使用的工具 | |
| 8 | streamFileAnnotationsEvent | 单多 | fileAnnotations | 文件连接/注解 | 无法验证 |
| 9 | streamToolEvent | 助手 | tool | openAI助手工具事件 | 无法验证 |
| 10 | streamAgentReasoningEvent | 多 | reasoning | 某些模型推理过程 | 无法验证 |
| 11 | streamNextAgentEvent | 多 | nextAgent | 执行下一个智能体 | 未验证出来 |
| 12 | streamAgentFlowEvent | 多 | agentFlowEvent | 流程状态（INPROGRESS/FINISHED/ERROR/STOPPED） | |
| 13 | streamAgentFlowExecutedDataEvent | 多 | agentFlowExecutedData | 节点的输入输出结果 | |
| 14 | streamNextAgentFlowEvent | 多 | nextAgentFlow | 节点执行状态（INPROGRESS/FINISHED） | |
| 15 | streamActionEvent | 多 | action | 人工介入下一步操作 | |
| 16 | streamAbortEvent | 单多 | abort | 停止回答 | |
| 17 | streamEndEvent | 单 | 无 | 结束标志 | |
| 18 | streamErrorEvent | 单多 | error | 执行错误信息 | |
| 19 | streamMetadataEvent | 单多 | metadata | 用户输入信息元数据 | |
| 20 | sreamUsageMetadataEvent | 多 | usageMetadata | token使用用量 | |