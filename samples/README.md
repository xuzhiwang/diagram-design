# 示例图（samples）

本目录放的是面向仓库所有者（xuzhiwang）主题的**原创示例图**，用来在浏览器里直接打开，查看 diagram-design 设计系统套在自己话题上的效果。

它们**不是** skill 自带的 `skills/diagram-design/assets/example-*.html` 官方样例；官方图库请看：

- 本地：[`skills/diagram-design/assets/index.html`](../skills/diagram-design/assets/index.html)
- 在线：https://cathrynlavery.github.io/diagram-design/

## 如何打开

任选其一即可（无需构建、无需服务器）：

```bash
open samples/grok-bot-architecture.html
# 或
open samples/pr-review-sequence.html
open samples/workreview-flowchart.html
open samples/priority-quadrant.html
```

也可以在文件管理器里**双击**对应的 `.html` 文件。图表是自包含静态 HTML（仅请求 Google Fonts）。

## 文件一览

| 文件 | 图类型 | 内容 |
|---|---|---|
| [`grok-bot-architecture.html`](grok-bot-architecture.html) | Architecture（架构） | 用户 ↔ Grok Bot ↔ 持久云电脑（browser / filesystem / terminal）↔ GitHub / Notion / 网站；焦点在云电脑 |
| [`pr-review-sequence.html`](pr-review-sequence.html) | Sequence（时序） | 用户请 Vigor → GitHub connector → 云端 coding agent → 打开 PR → 用户评审 |
| [`workreview-flowchart.html`](workreview-flowchart.html) | Flowchart（流程） | C++ 代码评审环：clone/open PR → compile → static checks → human review → merge 或 fix 回环 |
| [`priority-quadrant.html`](priority-quadrant.html) | Quadrant（四象限） | 助手工作按 Impact × Effort：GitHub PR babysitting、inbox、diagram generation、phone UI automation |

## 校验

对本目录新文件跑皮肤与自检（与贡献指南一致）：

```bash
python3 scripts/lint-skin.py samples/grok-bot-architecture.html samples/pr-review-sequence.html samples/workreview-flowchart.html samples/priority-quadrant.html
python3 skills/diagram-design/scripts/self_check.py samples/grok-bot-architecture.html
python3 skills/diagram-design/scripts/self_check.py samples/pr-review-sequence.html
python3 skills/diagram-design/scripts/self_check.py samples/workreview-flowchart.html
python3 skills/diagram-design/scripts/self_check.py samples/priority-quadrant.html
```
