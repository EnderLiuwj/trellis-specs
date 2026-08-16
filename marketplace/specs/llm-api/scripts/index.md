# 运行与评估入口

固定入口：

```text
scripts/run.sh
scripts/eval.sh
scripts/common.sh
```

- 脚本提供合理默认值并支持 `--model`、`--input`、`--max-samples`、`--concurrency`、`--dry-run` 等参数覆盖。
- `common.sh` 负责加载本地环境变量、检查必需变量和公共参数；缺失 API Key 或模型配置时应清晰失败，绝不打印 Key。
- 所有入口调用 `uv run`；不要求用户拼接冗长 Python 命令。
- `--dry-run` 只验证输入、抽样、预计请求数和参数，不发起任何 API 请求。
- 每次运行在 `logs/` 写独立且简洁的日志，仅保留阶段、数量、耗时、token 汇总和错误类型。
