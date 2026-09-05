# A股启动前潜伏选股 Skill V3.2

研究规则改进版，尚未完成历史样本外回测，不能据此宣称提高收益或胜率。

V3.1将主观成熟度百分比改为可核验的阶段状态；提供统一指标窗口、试盘/回踩代理、加速排除、成本后空间门槛、五维等权研究评分和验证协议。所有数值均为待验证研究初值。V3.0的原始提交保留在Git历史中。

V3.2补充宏观与跨市场情景、持仓和多周期约束、观察转布局条件及公开仓库隐私边界；保留原筛选阈值，不将单次股票案例或仓位建议固化为规则。仍未完成策略有效性验证。

从 ChatGPT 对话中整理、固化的 Codex Skill，用于研究资金已经试盘但尚未明显加速的 A 股候选。

核心框架：

> 强题材里的弱关注 + 强趋势里的低位置 + 资金试盘后的缩量潜伏 + 上方筹码干净

决策顺序为：数据资格 → 市场与板块趋势 → 量价证据 → 位置与压力 → 承接 → 阶段 → 空间与排序。

## 安装

将仓库克隆到 Codex skills 目录：

```bash
git clone https://github.com/Mrrabbitan/a-share-prelaunch-stock-skill.git ~/.codex/skills/a-share-prelaunch-stock-skill
```

之后可用 `$a-share-prelaunch-stock-skill` 显式调用，也可通过“全市场选股”“待启动潜力股”“低位潜伏”等请求触发。

## 文件

- `SKILL.md`：入口、决策流程与输出要求
- `references/scoring-and-filters.md`：资格门槛、五维评分和证据等级
- `references/measurement-and-execution.md`：指标、阶段状态、交易成本与执行约束
- `references/validation.md`：时间切分、对照实验、消融与成交验证
- `references/data-and-evidence.md`：行情、事件和风险证据要求
- `references/macro-and-cross-market.md`：议息情景、美股映射和事件时间
- `references/portfolio-and-timeframes.md`：持仓核对、多周期、风险预算与隐私边界
- `agents/openai.yaml`：Codex 界面信息

本项目只用于研究和观察池整理，不构成投资建议，不连接券商或自动下单。
