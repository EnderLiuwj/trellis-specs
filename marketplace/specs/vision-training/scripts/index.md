# 训练与评估入口

推荐入口固定为：

```text
scripts/train.sh
scripts/eval.sh
scripts/common.sh
```

- `train.sh` 与 `eval.sh` 是用户和 Agent 的唯一推荐入口；`common.sh` 放公共环境检查和变量。
- 脚本在开头提供合理默认值，并支持命令行覆盖，例如 `--gpus 0,1 --batch-size 32 --data-root /data/dataset --experiment-name baseline`。
- 启动前检查依赖、数据、GPU 可见性和输出路径；自动创建日志和实验目录。
- 脚本调用 `uv run`，将参数显式转交给 Python 入口；不要要求用户拼接冗长命令。
- 每次执行输出一行简洁的配置摘要：实验名、数据版本、GPU、配置文件和输出目录。日志应以关键阶段、关键指标和错误原因为主，避免逐 step 冗长刷屏。
