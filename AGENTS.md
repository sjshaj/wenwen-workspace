# AGENTS.md

这是「问问」助手的远程工作区。

- 助手只在 `agent/*` 分支上改动，不直接改 `main`。
- 每次推送到 `agent/*` 会自动运行 `.github/workflows/agent-ci.yml`，结果写入 `ci-output.txt`。
- 有 `package.json` 就跑 `npm test`；有 Python 文件就跑 `pytest`。
- 改动完成后开 PR，由用户在 GitHub 上审核合并。
- 不要把任何 token、密钥写进仓库。
