---
title: "Toolbox"
description: "记录我在开发、研究与写作中实际使用的工具"
ShowReadingTime: false
ShowWordCount: false
hideAuthor: true
hideMeta: true
---

记录我在开发、研究与写作中实际使用的工具与插件，随工作环境的变化持续更新。常规必备的就不占篇幅了；自己写的会标（自研）。

## VS Code 插件

| 工具 | 用途 | 保留原因 |
| --- | --- | --- |
| [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) + [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) + [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) | 文档与代码规范、格式化 | 写 Markdown 和代码时保持一致的格式标准 |
| [Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv) | CSV 按列着色 | 看回测数据等表格文件时结构一目了然 |
| [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) | 容器化开发环境 | 需要复现项目环境时比手动配置更可靠 |
| [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) | Git 历史、blame、分支关系 | 查看代码演进时比命令行更直观 |
| [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) | Notebook 与数据分析 | 量化研究和数据实验时直接使用 |
| [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) + [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance) + [Python Environments](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-python-envs) | Python 语言服务、调试与多环境管理 | 量化与机器视觉脚本的主力环境 |
| [Extension Pack for Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) | Java 全家桶：语言支持、Maven / Gradle、调试、测试 | 课程和 Java 项目的标配 |
| [DeepSeek Harness for VS Code](https://marketplace.visualstudio.com/items?itemName=foorgange.dsh-vscode-pro) | 在编辑器里直接 @dsh 调 DSH 的 agent 能力 | 桌面端 DSH 的 VS Code 入口，自己 fork 魔改 |

## 笔记软件

### [Obsidian](https://obsidian.md/)

本地 Markdown 知识库，用 Git 做版本管理。笔记全部落在自己手里，不依赖某个云端服务的锁定。

| 插件 | 用途 | 保留原因 |
| --- | --- | --- |
| obsidian-git | 用 GitHub 仓库同步笔记与版本管理 | 笔记的每次改动都有迹可循 |
| obsidian-enhancing-export | 导出 PDF / HTML | 需要分享或归档时一键转出 |
| obsidian-custom-attachment-location | 自定义附件存放位置 | 保持笔记库结构整齐 |

## 效率工具

### [Everything](https://www.voidtools.com/zh-cn/)

Windows 文件名搜索。基本替代了资源管理器自带的搜索。

### [Snipaste](https://www.snipaste.com/)

截图 + 贴图。截图可以钉在屏幕上，写代码、对文档时对照着看。

### [Geek Uninstaller](https://geekuninstaller.com/)

卸载工具。绿色单文件，卸载时连同残留文件和注册表项一起清理。

## Agent 装备栏

主力是 Claude Code 与 DSH 双端，同一套 skill 尽量三端共享。下面只记还在服役、真的会天天打开的。

### [Claude Code](https://www.anthropic.com/claude-code)

啥都能干。AI 编程最高的山，最长的河。插件全来自[官方插件市场](https://github.com/anthropics/claude-plugins-official)，模型走第三方网关接 GLM / DeepSeek。

| 插件 | 用途 | 保留原因 |
| --- | --- | --- |
| superpowers | 14 个开发工作流技能：先规划、子代理开发、TDD、完成前验证 | 把「别急着动手、写完必验证」变成默认流程 |
| context7 | 拉取各类库的最新官方文档 | 少被模型的训练截止日期坑一次 |
| code-review + code-simplifier | 提交前评审与代码精简 | 多一双不带情绪的眼睛 |
| frontend-design | 前端视觉方向指导 | 让产出不像模板货 |
| github + skill-creator | GitHub 操作与 skill 制作 | 趁手的周边，随装随用 |

### cnb-npc-skill（自研）

让 CNB 的 CodeBuddy NPC 在云端替我干活：一句话派发任务，它在仓库里执行完、提交 PR（或只读评审出报告），我只管验收。不占主力 Agent 的上下文和模型并发，实测 240 秒内提交 PR。

[cnb-npc-skill](https://github.com/Zi-Yi-Ming/cnb-npc-skill) · [项目实践（CSDN）](https://blog.csdn.net/2402_87488142/article/details/164303415)

### DSH（DeepSeek 桌面端）

DeepSeek 的桌面 agent 客户端，cordis 插件体系，社区生态很活。装过 25 个，还在服役的高频选手：

| 插件 | 用途 | 保留原因 |
| --- | --- | --- |
| dsh-background-agents | 后台长任务智能体，带任务板、消息总线与审批交接，重启不丢 | 长活儿扔给后台接着跑，主会话不被占线 |
| @joekytc/dsh-swarm | 六角色编队（编排 / 规划 / 开发 / 双评审）流水线，需求进、带评审门禁的交付出 | 复杂需求一条龙，每个阶段有可查的交付证据 |
| dsh-cron-panel | 定时任务面板，管 agent 提醒与系统 crontab | 定时活儿不再靠手敲 cron |
| dsh-cost-meter | 会话 / 当日费用统计，内置 90+ 模型价格目录与 11 家订阅额度查询 | 每天烧了多少钱，心里有数 |
| dsh-computer-use-windows | 带安全门控的 Windows 桌面操控 | GUI 活儿直接让 agent 上手 |
| @lyd123qw2008/dsh-tool-control-chrome | 本地桥接的 Chrome 操控 | 浏览器自动化比截图点击稳 |
| @starpivot/dsh-session-import | 把 Cursor / Codex / Claude Code 的会话与技能导入 DSH | 几个 agent 的历史不用各管各的 |
| @linxin666/dsh-client-ui-skill-explorer | 技能中心面板：按来源浏览、启停、增删 skill | 技能多起来以后，管理全靠它 |
| dsh-genui | 在回复里内联渲染可交互的图表、表单、小应用，操作回传模型 | 数据展示从「贴图」变成「能点」 |
| dsh-ppt | Markdown 生成网页放映与可编辑 PPTX，长表格自动分页 | 汇报材料一条命令出来 |
| dsh-plugin-wallpaper-engine | 把 Wallpaper Engine 壁纸渲染成聊天背景，液态玻璃风格 | 纯好玩的，但好玩也是生产力 |

另有十来个基建类在服役，不一一列了：插件管理（plugin-manager / plugin-install / find-plugin）、断线自动续跑（auto-continue / dsh-continue）、上下文仪表盘（context）、模型能力与推理档位、MCP 市场与 Exa 搜索。

### 共享技能池

一套技能三端共用，省得各装一份：

- **firecrawl**：网页抓取全家桶，12 个子技能覆盖抓取、爬取、搜索、站点下载、变更监控，三端主力。
- **llm-wiki**：按 Karpathy 的 llm-wiki 方法论持续维护个人知识库，网页、推文、PDF 喂进去自动整理成结构化 wiki。

### [ZCode](https://zcode.ai/)

桌面端 AI 助手。目前在用，偶尔会有点 bug，但已经留在日常流程里。

### [AtomCode](https://atomcode.atomgit.com/)

终端里的 AI 编码助手。缓存命中率高，也更适配国内生态。

## 学习与资源

### [GitHub](https://github.com/)

日常开发、开源协作和项目托管。

### [Google Skills](https://skills.google/)

Google 的官方学习平台。用于补充云、AI 等方向的实践知识。
