# 大模型 API 项目规范

本模板面向调用大模型 API 的应用、评估和批处理任务。它不绑定 LangChain、LlamaIndex 或具体服务商；项目使用 OpenAI 兼容接口，并通过本地环境变量切换供应商。

## 目录导航

- `project/`：项目目标、目录与 Git 约定。
- `environment/`：UV、国内镜像和 API 配置。
- `scripts/`：运行和评估的固定 shell 入口。
- `evaluation/`：评估样例与结果比较。
- `operations/`：批处理、限流、成本和隐私约束。

安装后，按项目实际服务商、模型、数据敏感度和验收标准更新文件。
