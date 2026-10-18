# Rāna

最近主要在做 AI 编程工具相关的开发，也在折腾笔记可视化。

AI 写代码时到底在忙什么，我挺想弄明白的。比如一条命令为什么反复跑，测试跑到什么时候才够。cmdaudit 和测试策略项目就在试着回答这些问题。

## 自己在做的项目

- [cmdaudit](https://github.com/cat0825/cmdaudit)：翻 AI 编程工具的会话记录，看每条命令花了多久、哪里失败了、哪些地方一直在重试。
- [AI Coding Agent Test Strategy](https://github.com/cat0825/ai-coding-agent-test-strategy)：研究 AI 写完代码后该怎么跑测试。想减少反复跑全量测试的浪费，又不漏掉真正的问题，目前还在做实验。
- [Cognitive Terrain](https://github.com/cat0825/cognitive-terrain)：把本地笔记画成一张能逛的三维地图。相关的笔记放在附近，可以点开看它们为什么出现在这里。计算在浏览器里完成，笔记不上传。[在线试试](https://cognitive-terrain.eriri-blog.workers.dev)。
- [Research Hub](https://github.com/cat0825/research-hub)：一个整理和分享研究资料的网站，可以发布资源、评论、收藏。用 Next.js 和 Supabase 写的。

## 给开源项目做过的改动

有些是修 bug，也有些是补功能。挑几条放在这里，细节和验证过程都在 PR 里。

- [LiteLLM #34696](https://github.com/BerriAI/litellm/pull/34696)：解封用户的请求返回成功，用户却仍被封禁。`false` 在写入数据库前被过滤掉了，修了这个问题。
- [new-api #5963](https://github.com/QuantumNous/new-api/pull/5963)：浏览器翻译改动了 React 管理的页面节点，创建密钥时会崩到 500 错误页。给前端入口加了禁止浏览器翻译的标记。
- [Headroom #8](https://github.com/llm-learner/headroom/pull/8)：原本只读 Codex 的记录，补上了 Claude Code 等其他工具，让它们共用一份每日预算。
- [CodeIsland #197](https://github.com/wxtsky/CodeIsland/pull/197)：接入 pi 和 Oh My Pi，补上扩展的安装、状态检查、修复和卸载。
- [Supermemory #1032](https://github.com/supermemoryai/supermemory/pull/1032)：记忆图只加载了一部分，却没告诉用户。补了已加载数量和继续加载的按钮。
- [MapLibre GL JS #7918](https://github.com/maplibre/maplibre-gl-js/pull/7918)：不会交互的地图标记被读屏软件当成按钮。调整了标记的无障碍角色。
- [MarkItDown #2045](https://github.com/microsoft/markitdown/pull/2045)：补上下载响应里 `filename*=` 格式的文件名解析，避免转换时丢掉文件名和扩展名。
- [open-multi-agent #286](https://github.com/open-multi-agent/open-multi-agent/pull/286)：给多智能体协作加了统一的模型路由规则，可以按任务和执行阶段选择模型。

[其他已合并的 PR](https://github.com/pulls?q=is%3Apr+author%3Acat0825+is%3Amerged+-user%3Acat0825)

我也用 AI 编程工具写代码。复现过程和验证结果会写在对应的 PR 里。

## GitHub 记录

<img width="100%" alt="cat0825 的 GitHub 活动、常用语言和贡献记录" src="https://raw.githubusercontent.com/cat0825/cat0825/metrics/github-metrics.svg">
