# Shakespeare Writing Studio

Agent-ready writing studio for Chinese and English publish-ready work: WeChat articles, Medium/Substack essays, research notes, founder memos, op-eds, speeches, data storytelling, statistical graphics, and polished web articles.

<img src="assets/shakespeare-logo.png" alt="Shakespeare Writing Studio logo" width="280">

One unified editorial workflow handles every output type:

- Chinese finance / technology WeChat articles
- English Medium / Substack essays
- research-backed articles
- executive memos and founder notes
- source-bound statistics and charts
- creative statistical graphics and visual explainers
- HTML previews and publish-ready packages

## What It Produces

Core package:

- `final.md`: publish-ready article, essay, memo, speech, or research note.
- platform preview: `wechat-ready.html`, `medium-ready.html`, or clean web HTML.
- `charts/*.svg` or `assets/*.svg`: source-backed charts, covers, timelines, mechanism diagrams, maps, word clouds, or hero statistical graphics.
- `publishing-note.md`: title set, subtitle/deck, social copy, source cautions, visual notes, and AI-feel cleanup notes.

Examples:

- [Chinese WeChat article: Fable 5 被封禁，智谱冲万亿。中国模型登顶日即将来临？](examples/fable-zhipu/final.md)
- [WeChat HTML preview](examples/fable-zhipu/wechat-ready.html)
- [English research article: The AI Boom Is Becoming A Power Grid Story](examples/ai-data-centers/final.md)
- [Medium-style HTML preview](examples/ai-data-centers/medium-ready.html)
- [Research charts and atlas](examples/ai-data-centers/charts)

## Core Standard

Top writing is a full editorial system:

- one arguable point of view
- concrete opening
- structure that carries the reader forward
- human sentence rhythm
- credible evidence where evidence matters
- platform-aware layout
- visuals matched to the article, not a default style
- charts only when they clarify the argument
- an ending that lands

If a paragraph or graphic could appear in any article on the internet, it probably should not survive the edit.

## Unified Workflow

Start here:

- [SKILL.md](SKILL.md)

The workflow chooses modules by task:

- Chinese WeChat: [references/wechat/chinese-finance-tech-writing.md](references/wechat/chinese-finance-tech-writing.md), [references/wechat/wechat-layout-patterns.md](references/wechat/wechat-layout-patterns.md), [references/wechat/layout-wechat.md](references/wechat/layout-wechat.md)
- English long-form: [references/medium-writing-patterns.md](references/medium-writing-patterns.md), [references/platform-formats.md](references/platform-formats.md), [references/human-voice.md](references/human-voice.md)
- Research and sources: [references/source-quality.md](references/source-quality.md), [references/research-data.md](references/research-data.md)
- Data and visuals: [references/data-visuals.md](references/data-visuals.md), [references/visual-production.md](references/visual-production.md)
- Final QA: [references/editorial-qa.md](references/editorial-qa.md), [references/release-gate.md](references/release-gate.md)

## Visual Principle

The visual style must come from the article.

No default dark mode. No default purple. No generic tech cards. No chart because “a chart looks serious.”

Before creating a visual, choose a direction:

- Clean Analyst: finance, strategy, market analysis, public data
- Energy / Infrastructure Report: power, climate, industrial systems, logistics
- Product Interface: SaaS, AI workflow, enterprise tools
- WeChat Editorial Cover: mobile-first Chinese article packaging
- Data Evidence: statistics, comparisons, source-backed claims
- Conceptual Mechanism: abstract thesis, causal route, supply chain, map

Dark visuals are allowed only when the article’s tone and metaphor call for them. A dark background chosen merely because it looks premium fails QA.

## Human Voice / Lower AI Feel

The workflow removes:

- generic thesis openings
- “not only X, but also Y” scaffolding
- symmetrical three-part paragraphs everywhere
- hollow transitions
- inflated business jargon
- endings that merely summarize
- fake certainty and motivational-poster language

It encourages:

- specific scenes
- uneven but intentional rhythm
- original analogies
- lived constraints
- concrete verbs
- named stakes
- one central claim per piece

## Source Standard

Background research must use top-tier sources only.

Preferred sources:

- official company announcements and documentation
- regulators, agencies, standards bodies, and court records
- primary datasets and research institutions
- audited public filings
- reputable business, technology, and financial publications with named reporting

Rejected sources:

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

## Repository Structure

- [SKILL.md](SKILL.md): unified execution protocol.
- [references/wechat](references/wechat): Chinese WeChat writing and layout rules.
- [references/medium-writing-patterns.md](references/medium-writing-patterns.md): Medium/Substack-style English essays.
- [references/human-voice.md](references/human-voice.md): anti-AI style and human voice editing.
- [references/source-quality.md](references/source-quality.md): top-tier source rules.
- [references/research-data.md](references/research-data.md): evidence search and source discipline.
- [references/data-visuals.md](references/data-visuals.md): chart selection and statistical graphics.
- [references/visual-production.md](references/visual-production.md): visual direction and production rules.
- [examples/fable-zhipu](examples/fable-zhipu): complete Chinese WeChat article.
- [examples/ai-data-centers](examples/ai-data-centers): complete English research article with charts.

## Quality Gate

Before release:

- central stance is visible
- no unsupported factual claims
- no weak source chain
- no generic AI filler
- no decorative charts
- no default visual style
- no broken image paths in HTML preview
- platform layout is readable on mobile
