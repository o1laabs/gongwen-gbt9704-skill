# Fork 说明（o1laabs）

本仓库是 [`mizzlelover/gongwen-gbt9704-skill`](https://github.com/mizzlelover/gongwen-gbt9704-skill) 的 fork，**未修改上游任何代码或文档**。仅用于存档、阅读与本地验证。

- 上游版本：SKILL.md `version: 2.0.0`，分支 `main`
- 上游许可：MIT（见 `LICENSE`），版权归原作者 mizzlelover
- 同步上游：`git remote add upstream https://github.com/mizzlelover/gongwen-gbt9704-skill && git fetch upstream`

## 本地实测记录（Linux / Node 22）

| 项 | 结果 |
| --- | --- |
| 生成 `--format ordinary` | ✅ 通过，`verify --profile ordinary` 13/13 PASS |
| 生成 `--format formal --letterhead digital` | ✅ 通过，`verify --profile formal` 23/23 PASS |
| 版心参数 | A4 210×297，上 37 / 下 35 / 左 28 / 右 26 mm，28 磅文档网格，与 GB/T 9704-2012 一致 |
| 字体 | ⚠️ 环境缺方正小标宋/仿宋时自动降级为 Songti SC / STFangsong 并明确告警；加 `--require-standard-fonts` 可直接失败 |
| 运行依赖 | 仅 Node.js + 系统 `zip` 命令，无 npm 依赖 |

## 使用提示

- 普通报告/方案一律 `--format ordinary`，不要因为单位名字像机关就上红头。
- `--format formal` 默认 `preprinted`（预印红头纸套打，首面留白不重绘红头）；要完整电子版才加 `--letterhead digital`。
- 红头纸套打的 `--letterhead-reserve-mm`（默认 72）必须按本单位实纸调（37–130 mm）。
- 印章、签名章、实体装订、横排表格单双页订口方向，生成器**不承诺**，须在目标 Word/WPS 与打印条件下人工核对。
