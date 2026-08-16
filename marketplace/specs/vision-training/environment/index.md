# 环境、依赖与模型来源

- 使用 UV 管理 Python 环境与依赖：依赖写入 `pyproject.toml`，锁定版本写入 `uv.lock`；新环境以 `uv sync` 创建。
- Python 命令统一通过 `uv run python ...` 执行，不要求手动激活虚拟环境。
- 默认使用适合中国大陆访问的 PyPI 镜像；README 中保留切换至官方源的方法。不要把某台机器的本地路径写进版本控制文件。
- 模型下载默认优先 ModelScope；模型不存在或版本不完整时才使用 Hugging Face，并采用可访问的镜像或显式下载脚本。
- 权重缓存位置由 `MODEL_CACHE_DIR` 或项目 `local.env` 配置。记录模型名称、版本/commit、来源和许可证；权重本体不进入 Git。
- `local.env` 只保存本机路径和私密变量，必须加入 `.gitignore`；提供不含私密值的 `local.env.example`。
