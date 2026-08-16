# Trellis 算法研发 Spec 模板

这是一套面向个人 AI 算法研发的 Trellis Spec registry，提供两个自包含模板：

- `vision-training`：视觉模型训练、验证与实验迭代。
- `llm-api`：基于大模型 API 的应用、批处理与评估。

二者都使用 UV、国内优先的依赖与模型来源、固定 shell 脚本入口、独立日志与可复现实验记录；不预置具体训练或 Agent 框架。

本仓库只保存可复用规范，不保存项目任务、个人日志、密钥、数据或模型权重。

## 本地试用

在一个新的 Git 项目中执行：

```bash
trellis init --codex -u enderliu \\
  --registry gh:enderliu/trellis-specs/marketplace \\
  --template vision-training
```

将仓库推送到 GitHub 后，上述命令即可使用。推送前，可在临时项目中将对应 `marketplace/specs/<模板名>/` 复制到 `.trellis/spec/` 验证内容。

已有项目补充缺失的 Spec 文件时使用 `--append`；它不会替你解决既有规范与模板规范的冲突，应当先审阅再合并。
