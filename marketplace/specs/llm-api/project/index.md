# 项目与目录约定

项目保持简单、按职责分层：

```text
src/          # API 客户端与业务逻辑
scripts/      # run.sh、eval.sh、common.sh
configs/      # 非敏感配置与提示词模板
eval_cases/   # 可提交、已脱敏的评估样例
outputs/      # 已脱敏的运行结果与汇总
logs/         # 运行日志
tests/        # 快速测试（按需）
```

- 业务代码不得硬编码服务商、模型名、API 地址或密钥。
- `README.md` 写清 `uv sync`、本地环境变量、最小运行命令和评估命令。
- `pyproject.toml` 与 `uv.lock` 必须提交；`local.env`、原始输入、完整敏感响应和日志不得提交。
