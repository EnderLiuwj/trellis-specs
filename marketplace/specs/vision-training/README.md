# 视觉训练项目规范

本模板面向视觉模型训练、评估和实验迭代。它不绑定 Ultralytics、MMDetection、Lightning 或其他框架；项目应在 `src/` 内自行选择实现。

## 目录导航

- `project/`：项目目标、目录和 Git 约定。
- `environment/`：UV、国内镜像和模型缓存。
- `data/`：数据位置、版本与划分。
- `scripts/`：训练和评估的固定 shell 入口。
- `experiments/`：输出、权重、日志与实验记录。
- `evaluation/`：指标、基线和验收。

安装后，先将其中的路径、指标、数据划分和实际命令改为当前项目的真实情况；删除不适用的条目。
