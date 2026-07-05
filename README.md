# Shackspare

## ZC's Writing Studio for essays, articles, memos, and publish-ready long-form work

<img src="assets/shackspare-logo.png" alt="Shackspare logo" width="280">

Shackspare is an agent-ready writing workflow for producing top-tier English writing across formats: Medium essays, Substack posts, founder notes, analytical articles, op-eds, research-backed pieces, product essays, speeches, memos, and polished web articles.

It started from article publishing workflows, but it is not limited to one platform. The standard is broader: strong thinking, human voice, clean structure, credible evidence, tasteful layout, and a final package that can actually go live.

## What It Produces

- `final.md`: publish-ready article or essay.
- `publishing-note.md`: title set, subtitle, social copy, voice notes, fact cautions, and AI-feel cleanup notes.
- Optional `article.html`: clean web preview for Medium/Substack/blog-style reading.
- Optional figures: data charts, quote cards, diagrams, or visual explainers when the article actually needs them.

## Core Standard

Top writing is not just "good prose." It is a full editorial system:

- A real point of view.
- A concrete opening.
- A structure that carries the reader forward.
- A human voice with texture and judgment.
- Evidence where evidence matters.
- Layout that respects reading rhythm.
- Charts and visuals only when they clarify the argument.

## Human Voice / Lower AI Feel

This workflow is designed to reduce AI-like writing patterns by default.

It avoids:

- generic thesis openings
- "not only X, but also Y" scaffolding
- symmetrical three-part paragraphs everywhere
- hollow transitions like "in today's fast-paced world"
- overuse of "delve," "leverage," "unlock," "transform," "foster," "robust," and "seamless"
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
- one real point of view per piece

## Research And Data

Shackspare can optionally run research and data modules when the article needs evidence.

It can:

- search for relevant public statistics
- prioritize official, primary, or reputable sources
- extract numbers into a source table
- decide whether a chart is actually useful
- choose a chart type: line, bar, slope, scatter, heatmap, small multiples, timeline, map, word cloud, or quote/data card
- produce charts only when they improve the article

Important constraint: not every strong article needs charts. Unless the piece is explicitly data-led, visuals should support the argument rather than take over the essay.

## Agent Compatibility

This repository is a file-based workflow. It can be used by Claude Code, Claude CLI, Codex CLI, or any local agent that can read files, browse/search when needed, rewrite drafts, run scripts, and produce Markdown/HTML outputs.

Recommended entry point:

- [SKILL.md](SKILL.md)

Search keywords:

- Medium writing workflow
- Substack essay workflow
- Claude Code writing skill
- Claude CLI writing workflow
- Codex CLI writing skill
- AI human voice editing
- reduce AI writing style
- data storytelling workflow
- AI writing research assistant

## Repository Structure

- [SKILL.md](SKILL.md): core execution protocol.
- [references/platform-formats.md](references/platform-formats.md): writing and layout rules across Medium, Substack, memos, op-eds, speeches, and web articles.
- [references/medium-writing-patterns.md](references/medium-writing-patterns.md): structures for Medium/Substack-style English essays.
- [references/human-voice.md](references/human-voice.md): anti-AI style rules and human voice editing.
- [references/research-data.md](references/research-data.md): evidence search and source discipline.
- [references/data-visuals.md](references/data-visuals.md): chart selection and data storytelling rules.
- [references/editorial-qa.md](references/editorial-qa.md): final quality gate before publishing.
- [assets/shackspare-logo.png](assets/shackspare-logo.png): transparent mascot logo.
- [examples/sample-essays.md](examples/sample-essays.md): fictional samples for inspection.

## Platform Notes

Medium and Substack readers can tolerate long pieces. They do not tolerate padded pieces.

Executives can tolerate dense memos. They do not tolerate vague ones.

Public essays can be personal. They cannot be lazy.

The final piece should feel clear, specific, and alive. If a paragraph could appear in any article on the internet, it probably should not survive the edit.
