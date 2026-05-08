# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.2] - 2026-05-08

### Changed

- `SKILL.md` 中 `metadata.version` 从 `1.0.1` 升级到 `1.0.2`，与发布 tag 保持一致。
- `CHANGELOG.md` 补齐 `[1.0.2]` 版本条目。

### Notes

- `v1.0.1` tag 因受 GitHub tag protection ruleset 保护无法强制移动，故发布一个新的 `v1.0.2` 版本作为正式可用的 repo-rename 发布版。
- 本版本与 `[1.0.1]` 内容等价，仅版本号与 tag 对齐。

## [1.0.1] - 2026-05-08

### Changed

- 仓库名从 `caojia321/mi-car-trial` 改为 `caojia321/mifi-skills`。
- 同步更新 `README.md`、`CHANGELOG.md`、`SKILL.md` 中所有仓库引用（安装命令、compare/releases 链接、`metadata.homepage`、`metadata.repository`）。
- `SKILL.md` 中 `metadata.version` 升级到 `1.0.1`。

### Migration

- 旧安装命令 `gh skill install caojia321/mi-car-trial mi-car-trial` 仍可使用（GitHub 301 重定向）。
- 建议改用 `gh skill install caojia321/mifi-skills mi-car-trial --agent opencode --pin v1.0.2`。

## [1.0.0] - 2026-05-08

首次公开发布。

### Added

- 完整 `SKILL.md` frontmatter：`name` / `description` / `license` / `compatibility` / `metadata`（author、version、homepage、repository、tags、external_costs）
- 统一 CLI 入口 `scripts/cli.py`，提供 6 个子命令：`terms` / `car-models` / `match` / `calc-down` / `aggregate` / `evaluate`
- core 模块拆分：`http.py`（HTTP 客户端）、`aggregate.py`（聚合试算接口）、`car_models.py`（车型清单 + 模糊匹配）、`terms.py`（期数定义）、`money.py`（金额/比例换算）、`evaluate.py`（方案打分与摘要）
- `LICENSE`（MIT）、`README.md`（定位、免责、4 种安装方式、6 CLI 子命令说明、故障排查）、`.gitignore`（Python + IDE + macOS + Windows + Linux 通用模板）
- 覆盖 SU7 / SU7 Pro / SU7 Max / SU7 Ultra / YU7 系列的车型匹配清单
- 支持 4 大发布渠道：skills.sh / ClawHub / GitHub / gh skill

### Changed

- 仓库采用 multi-skill monorepo 布局：`SKILL.md` 与 `scripts/` 迁移至 `skills/mi-car-trial/` 子目录，以符合 `gh skill publish` 的目录名 = `name` 校验。

### Security / Compliance

- 本 Skill 为非官方社区工具，所有信息以小米汽车 App / 小米天星金融官方渠道为准。
- 调用的是小米天星金融对外公开的聚合试算接口，不携带任何凭证、token、Cookie。
- 仅使用 Python 标准库（urllib + json），无第三方 pip 依赖，减少供应链风险。

[Unreleased]: https://github.com/caojia321/mifi-skills/compare/v1.0.2...HEAD
[1.0.2]: https://github.com/caojia321/mifi-skills/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/caojia321/mifi-skills/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/caojia321/mifi-skills/releases/tag/v1.0.0
