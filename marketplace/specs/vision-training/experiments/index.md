# 实验、权重与日志

每次训练使用独立的实验目录：

```text
outputs/<experiment-name>/
├── checkpoints/
│   ├── best.pt
│   └── last.pt
├── config.yaml
├── metrics.jsonl
└── summary.json
```

- `best.pt` 按已声明的验证指标保存，`last.pt` 保存最后一个可恢复状态；不要无界保存每个 epoch 的权重，除非项目明确要求。
- 每次运行在项目根目录 `logs/` 生成一个独立、易读的日志文件，例如 `logs/<experiment-name>.log`。
- 运行开始时复制实际生效的配置到 `outputs/<experiment-name>/config.yaml`；记录随机种子、数据版本、代码 commit、硬件/GPU 和启动参数。
- `metrics.jsonl` 记录关键训练/验证指标；`summary.json` 记录最佳 epoch、最终指标、耗时和权重路径。
- 根目录可维护 `experiments.csv` 或 `experiments.md`，汇总实验名、主要变量、最佳指标和一句结论。没有日志与配置快照的数值不得作为正式结果。
