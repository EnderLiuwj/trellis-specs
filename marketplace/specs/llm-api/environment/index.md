# 环境与 API 配置

- 使用 UV：依赖写入 `pyproject.toml`，锁定版本写入 `uv.lock`，以 `uv sync` 建立环境，所有 Python 入口用 `uv run python ...`。
- 默认使用适合中国大陆访问的 PyPI 镜像；README 说明如何切换官方源。
- 统一按 OpenAI 兼容接口实现，所有服务商差异仅放在未提交的 `local.env`：

```text
LLM_BASE_URL=
LLM_API_KEY=
LLM_MODEL=
```

- 提供 `local.env.example`，只含变量名和无敏感示例。API Key 不得进入代码、配置、命令历史、Git、输出或日志。
- 改变服务商或模型时，记录模型标识、供应商和日期；将模型选择作为可覆盖参数而非代码改动。
