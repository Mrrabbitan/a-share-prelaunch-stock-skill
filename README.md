# A股启动前潜伏选股 Skill V3.0

从 ChatGPT 对话中整理、固化的 Codex Skill，用于研究资金已经试盘但尚未明显加速的 A 股候选。

核心框架：

> 强题材里的弱关注 + 强趋势里的低位置 + 资金试盘后的缩量潜伏 + 上方筹码干净

决策顺序为：市场与板块趋势 → 资金介入 → 位置 → 上方筹码 → 承接 → 启动成熟度 → 技术确认。

## 安装

将仓库克隆到 Codex skills 目录：

```bash
git clone https://github.com/Mrrabbitan/a-share-prelaunch-stock-skill.git ~/.codex/skills/a-share-prelaunch-stock-skill
```

之后可用 `$a-share-prelaunch-stock-skill` 显式调用，也可通过“全市场选股”“待启动潜力股”“低位潜伏”等请求触发。

## 文件

- `SKILL.md`：入口、决策流程与输出要求
- `references/scoring-and-filters.md`：硬过滤、板块评分、个股评分和启动成熟度
- `references/data-and-evidence.md`：行情、事件和风险证据要求
- `agents/openai.yaml`：Codex 界面信息

本项目只用于研究和观察池整理，不构成投资建议，不连接券商或自动下单。
