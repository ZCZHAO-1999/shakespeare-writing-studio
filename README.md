# Shakespeare Writing Studio

<p align="center">
  <img src="assets/shakespeare-logo.png" alt="Shakespeare Writing Studio logo" width="260">
</p>

Shakespeare Writing Studio is an agent-ready editorial system for producing publish-ready writing in Chinese and English.

It supports WeChat articles, Medium/Substack essays, research notes, op-eds, founder memos, speeches, data storytelling, statistical graphics, HTML previews, and complete publishing packages.

The goal is simple: turn a rough idea, draft, notes, transcript, or research question into work that has a point of view, reads like a human wrote it, cites serious sources, and looks ready to publish.

## What It Produces

- `final.md`: publish-ready article, essay, memo, speech, or research note.
- Platform preview: `wechat-ready.html`, `medium-ready.html`, or clean web HTML.
- Visual assets: covers, timelines, evidence cards, mechanism diagrams, data charts, statistical atlases, maps, word clouds, or source-backed explainers.
- `publishing-note.md`: title options, subtitle/deck, social copy, source cautions, visual notes, paste steps, and AI-feel cleanup notes.

## Core Standard

Strong writing needs more than fluent paragraphs.

This workflow checks for:

- a clear, arguable stance
- a title with tension and search value
- a concrete opening
- paragraph rhythm that works on mobile
- serious source discipline
- human sentence texture
- visuals that raise the article's perceived quality
- data graphics that clarify the argument
- platform-specific packaging
- a final QA gate before release

If a paragraph, chart, or cover could appear in any article on the internet, it usually needs to be rebuilt.

## Examples

- [Chinese WeChat article: Fable 5 被封禁，智谱冲万亿。中国模型登顶日即将来临？](examples/fable-zhipu/final.md)
- [WeChat HTML preview](examples/fable-zhipu/wechat-ready.html)
- [English research article: The AI Boom Is Becoming A Power Grid Story](examples/ai-data-centers/final.md)
- [Medium-style HTML preview](examples/ai-data-centers/medium-ready.html)
- [Research charts and atlas](examples/ai-data-centers/charts)

## Workflow Modules

Start with:

- [SKILL.md](SKILL.md)

## Install As A Plugin

This repository is packaged for both marketplace-style plugin installation and direct agent reading.

Codex / OpenAI-style marketplace:

```bash
codex plugin marketplace add https://github.com/ZCZHAO-1999/shakespeare-writing-studio
```

Claude-style marketplace:

```bash
claude plugin marketplace add https://github.com/ZCZHAO-1999/shakespeare-writing-studio
```

If your agent does not support plugin marketplaces yet, point it at:

```text
AGENTS.md
```

or copy this skill folder into your agent's skills directory:

```text
plugins/shakespeare-writing-studio/skills/shakespeare-writing-studio
```

For chat-only tools such as DeepSeek, Doubao, Kimi, Qwen, or a browser chatbot, use the copy-paste prompt pack:

- [DeepSeek / Doubao prompt pack](prompts/deepseek-doubao.md)

The chat-only path cannot install a plugin, but it can follow the same editorial workflow if you paste the prompt, then paste your topic, draft, notes, or source links.

Plugin manifests:

- [Codex manifest](plugins/shakespeare-writing-studio/.codex-plugin/plugin.json)
- [Claude manifest](plugins/shakespeare-writing-studio/.claude-plugin/plugin.json)
- [Codex marketplace](.agents/plugins/marketplace.json)
- [Claude marketplace](.claude-plugin/marketplace.json)

Core references:

- [references/editorial-lessons.md](references/editorial-lessons.md): hard-won rules for titles, stance, anti-AI prose, WeChat rhythm, and cover quality.
- [references/human-voice.md](references/human-voice.md): human voice editing and AI-feel reduction.
- [references/source-quality.md](references/source-quality.md): top-tier source rules.
- [references/research-data.md](references/research-data.md): research and evidence discipline.
- [references/data-visuals.md](references/data-visuals.md): chart selection and statistical graphics.
- [references/visual-production.md](references/visual-production.md): visual direction and production rules.
- [references/editorial-qa.md](references/editorial-qa.md): final editorial checks.
- [references/release-gate.md](references/release-gate.md): go-live quality gate.

Platform references:

- [references/wechat/chinese-finance-tech-writing.md](references/wechat/chinese-finance-tech-writing.md): Chinese finance and technology article patterns.
- [references/wechat/wechat-layout-patterns.md](references/wechat/wechat-layout-patterns.md): WeChat mobile reading rhythm and layout archetypes.
- [references/wechat/layout-wechat.md](references/wechat/layout-wechat.md): WeChat-ready layout guidance.
- [references/medium-writing-patterns.md](references/medium-writing-patterns.md): English Medium/Substack-style essays.
- [references/platform-formats.md](references/platform-formats.md): platform-specific format choices.

## Visual Principle

The visual style must come from the article.

No default dark mode. No default purple. No generic tech cards. No chart added just to look serious.

Before creating a visual, choose the job:

- cover
- proof
- explanation
- transition
- comparison
- statistical evidence
- share-card packaging

Then choose the direction from the story:

- Clean Analyst: finance, strategy, market analysis, public data
- Event Pricing Board: regulatory shock, market repricing, valuation narrative
- Energy / Infrastructure Report: power, climate, industrial systems, logistics
- Product Interface: SaaS, AI workflow, enterprise software
- Data Evidence: statistics, comparisons, source-backed claims
- Human Profile: founders, teams, interviews
- Conceptual Cover: abstract thesis when the metaphor is strong enough

Rejected cover patterns include literal mountain/flag/summit graphics, cheap up-arrows, generic node maps, unreadable tiny labels, decorative dark plates, and private metaphors the reader has to decode.

## Source Standard

Background research must use serious sources.

Preferred:

- official company announcements and documentation
- regulators, agencies, standards bodies, and court records
- primary datasets and research institutions
- audited public filings
- reputable business, technology, and financial publications with named reporting

Rejected:

- generic SEO explainers
- unsourced statistics pages
- AI-summary pages
- random blogs with no primary trail
- reposts and screenshot-only evidence

## Agent Compatibility

Works with:

- Claude Code
- Claude CLI
- Codex CLI
- local CLI agents that can read files, browse/search when needed, rewrite drafts, run scripts, and produce Markdown/HTML/SVG outputs

Search keywords:

- Shakespeare Writing Studio
- WeChat article workflow
- Medium writing workflow
- Claude Code writing skill
- Claude CLI writing workflow
- Codex CLI writing skill
- AI human voice editing
- data storytelling workflow
- research essay workflow
- statistical graphics workflow

## Quality Gate

Before release:

- the central stance is visible
- the title has tension and search value
- no unsupported factual claims remain
- no weak source chain remains
- no generic AI filler remains
- no invented strategy/product frame remains
- no decorative chart remains
- no default visual style remains
- the cover improves the article's perceived quality
- HTML image paths work
- mobile layout is readable

---

# Shakespeare Writing Studio 中文说明

<p align="center">
  <img src="assets/shakespeare-logo.png" alt="Shakespeare Writing Studio logo" width="260">
</p>

Shakespeare Writing Studio 是一套面向 AI agent 的写作与出版工作流，用来生产可发布的中文和英文内容。

它可以处理微信公众号文章、Medium/Substack 英文长文、研究笔记、观点文章、创始人备忘录、演讲稿、数据叙事、统计图、信息图、HTML 预览和完整发布包。

目标很明确：把一个粗糙主题、草稿、访谈、资料包或研究问题，推进成一篇有观点、有人味、有来源、有排版、有视觉质量的成稿。

## 能交付什么

- `final.md`：可发布正文、长文、备忘录、演讲稿或研究笔记。
- 平台预览：`wechat-ready.html`、`medium-ready.html` 或干净网页 HTML。
- 视觉资产：封面、时间轴、证据卡、机制图、数据图、统计图谱、地图、词云或有来源的信息图。
- `publishing-note.md`：标题组、副标题、社交文案、来源提示、视觉说明、复制发布步骤和 AI 腔清理说明。

## 核心标准

顶级文章不只是句子流畅。

这套流程会检查：

- 有没有明确、可争论的观点
- 标题有没有张力和搜索价值
- 开头是否具体
- 手机阅读节奏是否顺
- 来源是否严肃
- 句子是否像真人写作
- 视觉是否抬高文章质感
- 数据图是否真的推进论证
- 是否适配目标平台
- 发布前是否通过质量门槛

如果一段话、一张图或一个封面可以放进任何文章里，它通常就需要重做。

## 示例

- [中文公众号文章：Fable 5 被封禁，智谱冲万亿。中国模型登顶日即将来临？](examples/fable-zhipu/final.md)
- [微信公众号 HTML 预览](examples/fable-zhipu/wechat-ready.html)
- [英文研究文章：The AI Boom Is Becoming A Power Grid Story](examples/ai-data-centers/final.md)
- [Medium 风格 HTML 预览](examples/ai-data-centers/medium-ready.html)
- [研究图表和统计图谱](examples/ai-data-centers/charts)

## 工作流模块

从这里开始：

- [SKILL.md](SKILL.md)

## 作为 Plugin 安装

这个仓库已经同时支持 marketplace 风格安装和普通 agent 直接读取。

Codex / OpenAI 风格 marketplace：

```bash
codex plugin marketplace add https://github.com/ZCZHAO-1999/shakespeare-writing-studio
```

Claude 风格 marketplace：

```bash
claude plugin marketplace add https://github.com/ZCZHAO-1999/shakespeare-writing-studio
```

如果你的 agent 还不支持 plugin marketplace，直接让它读取：

```text
AGENTS.md
```

或者把这个 skill 文件夹复制到对应 agent 的 skills 目录：

```text
plugins/shakespeare-writing-studio/skills/shakespeare-writing-studio
```

如果对方只会用 DeepSeek、豆包、Kimi、通义千问或网页聊天机器人，直接使用复制粘贴版 Prompt Pack：

- [DeepSeek / 豆包 Prompt Pack](prompts/deepseek-doubao.md)

聊天工具无法真正安装 plugin，但只要先粘贴这段 prompt，再粘贴选题、草稿、资料或链接，就可以按同一套编辑流程工作。

插件文件：

- [Codex manifest](plugins/shakespeare-writing-studio/.codex-plugin/plugin.json)
- [Claude manifest](plugins/shakespeare-writing-studio/.claude-plugin/plugin.json)
- [Codex marketplace](.agents/plugins/marketplace.json)
- [Claude marketplace](.claude-plugin/marketplace.json)

核心参考：

- [references/editorial-lessons.md](references/editorial-lessons.md)：标题、观点、反 AI 腔、公众号节奏、封面质量的实战修正规则。
- [references/human-voice.md](references/human-voice.md)：真人口吻和 AI 腔清理。
- [references/source-quality.md](references/source-quality.md)：高质量来源规则。
- [references/research-data.md](references/research-data.md)：研究和证据规范。
- [references/data-visuals.md](references/data-visuals.md)：图表选择和统计图谱。
- [references/visual-production.md](references/visual-production.md)：视觉方向和生产规范。
- [references/editorial-qa.md](references/editorial-qa.md)：最终编辑检查。
- [references/release-gate.md](references/release-gate.md)：上线质量门槛。

平台参考：

- [references/wechat/chinese-finance-tech-writing.md](references/wechat/chinese-finance-tech-writing.md)：中文财经科技文章模式。
- [references/wechat/wechat-layout-patterns.md](references/wechat/wechat-layout-patterns.md)：公众号手机阅读节奏和排版范式。
- [references/wechat/layout-wechat.md](references/wechat/layout-wechat.md)：公众号发布排版规范。
- [references/medium-writing-patterns.md](references/medium-writing-patterns.md)：英文 Medium/Substack 风格长文。
- [references/platform-formats.md](references/platform-formats.md)：平台格式选择。

## 视觉原则

视觉风格必须从文章里长出来。

不要默认暗色。不要默认紫色。不要默认科技卡片。不要为了显得严肃硬塞图表。

做图前先判断这张图的职责：

- 封面
- 证明
- 解释
- 转场
- 对比
- 统计证据
- 分享卡片

再从文章内容里选择视觉方向：

- Clean Analyst：财经、策略、市场分析、公共数据
- Event Pricing Board：监管冲击、市场重估、估值叙事
- Energy / Infrastructure Report：电力、气候、工业系统、物流
- Product Interface：SaaS、AI 工作流、企业软件
- Data Evidence：统计、对比、有来源的证据
- Human Profile：创始人、团队、访谈
- Conceptual Cover：只有隐喻足够强时才使用抽象封面

明确拒绝：山峰、旗子、登顶、火箭、廉价上升箭头、泛泛节点图、看不清的小字、套模板的暗色图、需要读者猜的私人隐喻。

## 来源标准

背景搜索只能使用严肃来源。

优先：

- 公司官方公告和文档
- 监管机构、政府机构、标准组织、法院记录
- 一手数据集和研究机构
- 审计过的公开文件
- 有署名报道的主流财经、商业、科技媒体

拒绝：

- SEO 水文
- 无来源统计页
- AI 总结页
- 没有一手来源链路的随机博客
- 搬运和截图证据

## Agent 兼容

适用于：

- Claude Code
- Claude CLI
- Codex CLI
- 能读文件、搜索、改写、运行脚本并生成 Markdown/HTML/SVG 的本地 CLI agent

搜索关键词：

- Shakespeare Writing Studio
- WeChat article workflow
- Medium writing workflow
- Claude Code writing skill
- Claude CLI writing workflow
- Codex CLI writing skill
- AI human voice editing
- data storytelling workflow
- research essay workflow
- statistical graphics workflow

## 质量门槛

发布前必须确认：

- 核心观点清楚
- 标题有张力和搜索价值
- 没有无来源事实
- 没有低质量来源链
- 没有明显 AI 腔
- 没有乱造的战略或产品概念
- 没有装饰性图表
- 没有默认视觉风格
- 封面提高文章质感
- HTML 图片路径可用
- 手机端阅读顺畅
