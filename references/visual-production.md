# Visual Production / 顶级配图生产规范

This workflow must produce visuals that are worth publishing, not placeholders. The article can use multimodal AI when available, but it must still produce strong deterministic graphics when the agent only has code, HTML, SVG, Canvas, or Python.

## 一、两条生产路线

Important: samples under `examples/` are only QA fixtures. Production visuals must pass `release-gate.md`; they cannot stop at a simple style demo.

### A. Multimodal / Image Model Route

Use this route when the agent has access to image generation or image editing.

Best for:
- cover images
- founder / team atmosphere
- product scene mood
- editorial illustration
- textured opener images

Rules:
- Generate a visual direction before prompting: subject, setting, color temperature, composition, crop safety, typography needs.
- Do not ask the model to render small Chinese text inside the image. Add text later in HTML/SVG or Word.
- Keep the center 60% safe for WeChat square-card cropping.
- Use the generated image as material, then add article title, labels, masks, grain, and visual hierarchy with deterministic layout.
- Avoid generic glowing circuit boards, floating robots, office silhouettes, fake dashboards, and stock-photo handshakes.

Prompt frame:
```
Editorial cover image for a Chinese WeChat finance/technology article.
Subject: [specific scene].
Mood: [calm / tense / investigative / industrial].
Composition: 2.35:1 horizontal cover, main subject in center safe area, negative space for title, no text in image.
Style: premium business magazine, documentary detail, restrained contrast, no cartoon, no generic AI symbols.
Lighting: [natural / cold factory light / soft office light].
Output should look like a commissioned editorial image, not stock art.
```

### B. Deterministic Code Route

Use this route when no multimodal image tool is available. The output still needs to look polished.

Best for:
- mechanism diagrams
- process maps
- comparison charts
- evidence cards
- product/workflow diagrams
- cover plates with abstract but structured visuals

Tools:
- HTML/CSS rendered by Playwright
- SVG diagrams
- Canvas
- Python/Pillow only for final composition or resizing

Rules:
- Use layout, hierarchy, spacing, and contrast to create quality. Do not rely on a dark rectangle and a title.
- Every visual needs at least three layers: background texture, structural diagram, editorial labels.
- Use SVG for arrows, routes, nodes, grids, and product diagrams.
- Use real visual metaphors from the article: factory line, search chain, customer page, data trail, decision table.
- Keep all small labels readable after the image is scaled to 390px mobile width.
- Add article-specific substance: mechanism names, real actors, product steps, evidence categories, constraints, or tradeoffs from the draft.

## 二、视觉质量标准

A visual is publishable only if it passes these checks:

- It has one job: cover, explain, prove, transition, or summarize.
- It can be understood in 3 seconds on a phone.
- It has visible hierarchy: title, structure, labels, note.
- It is not just a decorative gradient, stock-like mood image, or generic tech wallpaper.
- It contains no sensitive competitor data or unsupported numbers.
- It still looks intentional when cropped to 2.35:1 and when shown as a square share card.
- It matches the article's tone and the other figures in the same package.
- It is not locked into one dark tech style. Choose a visual direction from the article's industry, tone, and reader expectation.
- It passes `release-gate.md`: generic node diagrams are rejected for final delivery.

## 三、Visual Direction Matrix / 视觉方向矩阵

Pick one direction before generating any visual. The same article should use one direction consistently, with small variations between cover and figures.

| Direction | Best for | Look | Avoid |
|---|---|---|---|
| Industrial Report | manufacturing, robotics, hardware, supply chain | dark graphite, blueprint lines, machine-map geometry, documentary restraint | sci-fi glow, fake robots, over-polished dashboards |
| Clean Analyst | finance, market analysis, strategy, macro trends | warm white background, sharp black type, thin rules, editorial charts, restrained accent color | dark tech wallpaper, heavy gradients, decorative icons |
| Product Interface | SaaS, AI workflow, enterprise software | light UI panels, real workflow cards, cursor/action trails, subtle shadows | fake app screenshots with tiny unreadable text |
| Human Profile | founders, teams, interviews | photographic or illustrated portrait space, quiet grain, one strong quote, editorial crop | corporate headshot collage, motivational poster style |
| Data Evidence | public metrics, reports, comparisons | one hero number, source line, compact chips, high contrast | unsupported precision, chartjunk, tiny legends |
| Conceptual Cover | abstract industry thesis | symbolic structure, map, chain, split surface, clean title zone | generic brain/circuit/robot imagery |

If using the deterministic code route, implement these directions through color, typography, layout density, line style, and metaphor. Do not default to the dark graphite theme.

## 四、Image Types

### 1. Editorial Cover

Purpose: win the first glance in WeChat feed and set the article's world.

Structure:
- 2.35:1 canvas.
- Subject or diagram occupies the center and right.
- Title zone stays clean.
- Bottom plate can hold series label, issue label, or article type.

Deterministic options:
- industrial map for manufacturing stories
- query-to-action network for AI search stories
- customer workspace diagram for SaaS/product stories
- capital flow / supply chain map for finance stories

### 2. Mechanism Diagram

Purpose: explain how something works.

Structure:
- 3–5 nodes.
- One highlighted feedback or decision path.
- Minimal labels.
- One sentence note at the bottom.

### 3. Evidence Card

Purpose: carry public data or non-sensitive facts.

Structure:
- one hero number or claim
- 2–4 support chips
- source note
- no unsupported precision

### 4. Workflow Map

Purpose: show how work moves from one actor/system to another.

Structure:
- left-to-right or top-to-bottom sequence
- status chips
- bottleneck marker
- final action

### 5. Comparison Figure

Purpose: contrast two routes or two operating models.

Structure:
- two columns, same fields
- one highlighted difference
- no fake symmetry if the story is not symmetric

## 五、No-Multimodal Visual Recipe

When only code is available, build images in this order:

1. Write the visual job in one sentence.
2. Pick the visual direction from the matrix and explain why it fits the article. Defaulting to dark graphite without article-specific reason fails QA.
3. Pick a type: cover, mechanism, evidence, workflow, comparison.
4. Sketch 3–5 nodes or cards.
5. Create HTML/SVG at 1200×511 for cover or 1200×620 for figures.
6. Render at 2x with Playwright.
7. Insert into article and check at 390px mobile width.
8. If text is too small, simplify the diagram instead of shrinking text.

## 六、Common Failures

- Dark card with title only: looks like placeholder.
- Too many labels: unreadable on phone.
- AI-generated text inside image: likely broken.
- Generic "AI brain / circuit / robot" imagery: low trust.
- Decorative image with no function: breaks reading rhythm.
- Diagram repeats the paragraph: wastes reader attention.
- Every project uses the same dark background: reads as template, not editorial direction.
- Dark background chosen only because it looks "premium": reject and choose a direction from article content.
- Simple style demo used as final work: fails the go-live gate.

## 七、Required Output Note

In `发布说明.txt`, list the route used for each visual:

```
cover.png / cover / multimodal generated + deterministic typography / no external license
fig01.png / mechanism diagram / deterministic HTML-SVG / no external license
photo01.jpg / scene image / Unsplash / license URL
```
