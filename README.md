# Shakespeare Writing Studio

Agent-ready English writing workflow for Medium, Substack, research essays, founder notes, analytical articles, memos, op-eds, and publish-ready long-form work.

<img src="assets/shakespeare-logo.png" alt="Shakespeare Writing Studio logo" width="280">

This repository is built for Claude Code, Claude CLI, Codex CLI, and other local agents that can read files, research carefully, edit prose, build charts, and produce Markdown or HTML deliverables.

It started from article publishing workflows, but it is not limited to one platform. The standard is broader: strong thinking, human voice, credible evidence, tasteful layout, and a final package that can actually go live.

## What It Produces

Core package:

- `final.md`: publish-ready essay, article, memo, speech, or research note.
- `medium-ready.html`: clean web preview for Medium/Substack/blog-style reading.
- `publishing-note.md`: title set, subtitle, social copy, voice notes, fact cautions, and AI-feel cleanup notes.
- `charts/*.svg`: optional source-backed charts, timelines, maps, word clouds, or data cards.

Example now included:

- [The AI Boom Is Becoming A Power Grid Story](examples/ai-data-centers/final.md)
- [Medium-style HTML preview](examples/ai-data-centers/medium-ready.html)
- [Research charts](examples/ai-data-centers/charts)

## Core Standard

Top writing is a full editorial system:

- one real point of view
- a concrete opening
- structure that carries the reader forward
- human sentence rhythm
- evidence where evidence matters
- layout that respects reading flow
- charts only when they clarify the argument
- an ending that lands instead of summarizing

If a paragraph could appear in any article on the internet, it probably should not survive the edit.

## Human Voice / Lower AI Feel

This workflow is designed to reduce AI-like writing patterns by default.

It avoids:

- generic thesis openings
- “not only X, but also Y” scaffolding
- symmetrical three-part paragraphs everywhere
- hollow transitions like “in today’s fast-paced world”
- overuse of “delve,” “leverage,” “unlock,” “transform,” “foster,” “robust,” and “seamless”
- conclusions that summarize instead of landing
- fake certainty, fake intimacy, and motivational poster language

It encourages:

- specific scenes
- uneven but intentional sentence rhythm
- original analogies
- lived constraints
- small admissions of uncertainty
- concrete verbs
- named stakes
- one central claim per piece

## Research And Data

Use research only when it makes the piece sharper.

The workflow can:

- search for relevant public statistics
- prioritize official, primary, or reputable sources
- extract numbers into a source table
- decide whether a chart is actually useful
- choose a chart type: line, bar, slope, scatter, heatmap, small multiples, timeline, map, word cloud, or quote/data card
- produce charts only when they improve the reader’s understanding

Important constraint: not every strong article needs charts. Unless the piece is explicitly data-led, visuals should support the argument rather than take over the essay.

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

See [references/source-quality.md](references/source-quality.md).

## How To Use

Start here:

- [SKILL.md](SKILL.md)

Recommended agent flow:

1. Read [references/platform-formats.md](references/platform-formats.md) to choose the article type.
2. Read [references/human-voice.md](references/human-voice.md) before rewriting.
3. Read [references/source-quality.md](references/source-quality.md) before any background search.
4. Read [references/research-data.md](references/research-data.md) when evidence is required.
5. Read [references/data-visuals.md](references/data-visuals.md) before creating charts.
6. Read [references/editorial-qa.md](references/editorial-qa.md) before delivery.

Compatible with:

- Claude Code
- Claude CLI
- Codex CLI
- local CLI agents that can read files, browse/search when needed, rewrite drafts, run scripts, and produce Markdown/HTML outputs

Search keywords:

- Medium writing workflow
- Substack essay workflow
- Claude Code writing skill
- Claude CLI writing workflow
- Codex CLI writing skill
- AI human voice editing
- reduce AI writing style
- data storytelling workflow
- research essay workflow

## Repository Structure

- [SKILL.md](SKILL.md): core execution protocol.
- [references/platform-formats.md](references/platform-formats.md): writing and layout rules across Medium, Substack, memos, op-eds, speeches, and web articles.
- [references/source-quality.md](references/source-quality.md): top-tier source rules for background research.
- [references/medium-writing-patterns.md](references/medium-writing-patterns.md): structures for Medium/Substack-style English essays.
- [references/human-voice.md](references/human-voice.md): anti-AI style rules and human voice editing.
- [references/research-data.md](references/research-data.md): evidence search and source discipline.
- [references/data-visuals.md](references/data-visuals.md): chart selection and data storytelling rules.
- [references/editorial-qa.md](references/editorial-qa.md): final quality gate before publishing.
- [assets/shakespeare-logo.png](assets/shakespeare-logo.png): transparent mascot logo.
- [examples/ai-data-centers](examples/ai-data-centers): complete research article with charts and HTML preview.
- [examples/sample-essays.md](examples/sample-essays.md): fictional samples for inspecting structure and voice.

## Quality Gate

Before release, the piece must pass:

- no unsupported factual claims
- no weak source chain for data
- no generic AI filler
- no decorative charts
- no confusing section order
- no ending that merely recaps
- no broken image paths in HTML preview

## Platform Notes

Medium and Substack readers can tolerate long pieces. They do not tolerate padded pieces.

Executives can tolerate dense memos. They do not tolerate vague ones.

Public essays can be personal. They cannot be lazy.
