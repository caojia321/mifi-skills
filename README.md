# mi-car-trial

小米汽车（SU7 / YU7 系列）贷款聚合试算 Agent Skill。

通过自然语言描述（车型名、总车价、首付金额或首付比例、期数），调用小米天星金融 **af-portal-api 免登录聚合试算接口**，自动返回所有可选产品方案及每个方案的试算结果，并给出评分与推荐组合。

> **仅适用于小米汽车**（小米 SU7 / SU7 Pro / SU7 Max / SU7 Ultra / YU7 系列等），**不适用于小鹏 / 蔚来 / 理想** 等其他品牌。

---

## 免责声明

- 本 Skill 是社区工具，**非小米集团官方产品**，所有信息以小米汽车 App / 小米天星金融官方渠道为准。
- 调用的接口为小米天星金融对外公开的聚合试算接口，若被小米关闭、限流或变更，本 Skill 可能停止工作。
- 试算结果仅供参考，实际利率、费用、审批结果以金融机构审批为准。

---

## 安装

### 1. 通过 [skills.sh](https://skills.sh)（所有主流 agent host）

```bash
npx skills add caojia321/mifi-skills
```

### 2. 通过 `gh skill`（GitHub CLI ≥ 2.90.0）

```bash
gh extension install github/gh-skill
gh skill install caojia321/mifi-skills mi-car-trial --agent opencode
# 也支持 --agent claude-code / cursor / codex / gemini
```

### 3. 通过 ClawHub

```bash
clawhub skill install caojia321/mifi-skills
```

### 4. 手动（适合二次开发）

```bash
git clone https://github.com/caojia321/mifi-skills.git
# 把 skills/mi-car-trial/ 链接或拷贝到你 agent 的 skills 目录，例如：
#   ~/.config/opencode/skills/mi-car-trial/
#   ~/.claude/skills/mi-car-trial/
```

---

## 环境要求

- **Python 3.7+**，**仅标准库**（`urllib`、`json`），无 pip 依赖
- 能访问公网域名 `afs.airstarfinance.net`（企业 VPN 可能拦截）

---

## 触发词

`试算`、`贷款方案`、`聚合试算`、`我想买`、`小米 SU7`、`小米 YU7`、`购车方案`、`月供` 等。

Agent 在检测到上述关键词或明显购车试算意图时，自动调用本 Skill。

---

## 使用（CLI 子命令）

所有子命令均通过统一入口 `scripts/cli.py` 调用：

| 子命令 | 说明 |
|---|---|
| `terms` | 列出当前支持的期数选项（12/24/36/48/60…） |
| `car-models` | 列出支持的车型清单（SU7 各配置 + YU7 各配置） |
| `match <车型名>` | 模糊匹配用户输入 → 标准车型 ID |
| `calc-down <总价> <比例或金额>` | 计算首付金额 |
| `aggregate <车型> <总价> <首付> <期数>` | 调用聚合试算接口，返回所有可选方案 |
| `evaluate <aggregate 输出>` | 对方案排序、挑选推荐组合、输出人类可读摘要 |

完整参数参考 `skills/mi-car-trial/scripts/cli.py`。

### 典型调用链（Agent 内部）

```
用户自然语言
  → match (车型归一化)
  → calc-down (首付金额换算)
  → aggregate (聚合试算 HTTP 调用)
  → evaluate (打分 & 摘要)
  → 输出给用户
```

### 从 repo 根直接跑示例

```bash
# 查看车型清单
python skills/mi-car-trial/scripts/cli.py car-models

# 查看期数
python skills/mi-car-trial/scripts/cli.py terms

# 聚合试算：SU7 Max 29.99 万、首付 30%、24 期
python skills/mi-car-trial/scripts/cli.py aggregate "SU7 Max" 299900 0.3 24
```

---

## 目录结构

```
mi-car-trial/                              # repo 根
├── SKILL.md                               # （已移到 skills/mi-car-trial/ 下）
├── README.md                              # 本文件
├── LICENSE                                # MIT
├── .gitignore
├── CHANGELOG.md                           # 版本记录
└── skills/
    └── mi-car-trial/
        ├── SKILL.md                       # Skill 元信息 + 使用说明（Agent 首读文件）
        └── scripts/
            ├── cli.py                     # 统一 CLI 入口
            └── core/
                ├── http.py                # 与 afs.airstarfinance.net 的 HTTP 客户端
                ├── aggregate.py           # 聚合试算接口封装
                ├── car_models.py          # 车型清单 + 模糊匹配
                ├── terms.py               # 期数定义
                ├── money.py               # 首付金额/比例换算、金额格式化
                └── evaluate.py            # 方案打分与摘要
```

---

## 故障排查

### `HTTPError 403` / 接口被拒

接口可能已更新风控策略。优先从 SU7 App 官方端复现问题并确认公开接口是否变更。

### `ConnectionError` / 请求超时

确认本机可以 ping / 访问 `afs.airstarfinance.net`。企业代理 / VPN 可能拦截该域名。

### 返回方案为空

- 检查车型是否在 `python skills/mi-car-trial/scripts/cli.py car-models` 清单中
- 检查期数是否在 `python skills/mi-car-trial/scripts/cli.py terms` 支持范围
- 确认首付比例是否在金融产品合规区间（通常 20%–50%）

### Skill 没被 Agent 触发

- 检查 `SKILL.md` 的 `description` 是否包含触发词
- 重启 agent host（Claude Code / OpenCode 等）让其重新索引 skills 目录
- 确认 Skill 已安装到对应 agent 的扫描路径（`~/.config/opencode/skills/` 或 `~/.claude/skills/` 等）

---

## 贡献

欢迎 issue / PR。新增车型或适配新产品时：

1. 在 `skills/mi-car-trial/scripts/core/car_models.py` 追加条目
2. 在 `skills/mi-car-trial/scripts/core/terms.py` 确认期数
3. 运行 `python skills/mi-car-trial/scripts/cli.py aggregate ...` 验证返回
4. 更新 `CHANGELOG.md`

---

## License

[MIT](./LICENSE) © 2026 天星数科科技有限公司 (Xiaomi Finance / Airstar Finance)
