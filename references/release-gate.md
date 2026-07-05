# Release Gate / 上线交付门槛

This file defines the final go-live gate. A package is not complete until it passes every item here.

## 一、原则

Examples in this repository are QA fixtures. They test layout, rhythm, visual direction, and rendering. They are not the complexity ceiling for final client work.

Formal delivery must be article-specific:

- The writing must use the user's facts, names, scenes, claims, and constraints.
- The images must encode the article's actual mechanism, evidence, workflow, people, product, market, or tension.
- The Word and HTML output must be ready for WeChat preview without rebuilding layout.
- The release note must let an editor publish confidently.

## 二、内容上线门槛

The article cannot ship if any item below fails:

- The first screen contains title, cover, and a concrete opening scene or conflict.
- Every section advances one layer of the information ladder.
- No section is only generic background, feature listing, or slogan.
- Every strong claim has support from the draft, source material, or explicit placeholder.
- No unverified numbers enter title, summary, cover, infographic, or caption.
- AI-like prose patterns have been removed from the final article text.
- The article has a clear closing judgment, not a vague "future imagination" ending.

## 三、视觉上线门槛

Formal visuals cannot be simple generic diagrams. A final visual must contain article-specific substance.

Each cover must include at least four of the following:

- article-specific subject or metaphor
- clear title-safe composition
- visual hierarchy across foreground, midground, and background
- project-specific color direction
- crop-safe 2.35:1 layout and square-card safe area
- real scene, workflow, map, product surface, or symbolic structure
- deterministic typography or labels added after generation

Each infographic must include at least five of the following:

- a named mechanism, workflow, model, comparison, or evidence set
- 3–6 meaningful nodes or cards from the article
- one highlighted path, bottleneck, tradeoff, or decision point
- labels that add information beyond the paragraph
- article-specific terms, not generic placeholders
- source or note line when data/facts are involved
- readable text at 390px mobile preview
- visual structure that differs when article type differs

Reject immediately:

- dark background + title + four generic nodes
- the same template reused across unrelated articles
- decorative image with no reading function
- AI-generated image with broken text inside
- infographic that merely repeats the adjacent paragraph
- chart with unsupported or invented numbers

## 四、排版上线门槛

- Body text uses one stable style.
- No pure text wall over six consecutive paragraphs.
- No sequence of more than five tiny one-line paragraphs.
- Every image has a setup paragraph and a follow-up sentence.
- Captions are short and do not repeat the paragraph.
- The 390px mobile preview has no crowded title, tiny infographic text, or abrupt visual interruption.
- Cover and body images remain readable after WeChat compression or manual replacement.

## 五、交付上线门槛

Required files:

- final `.docx`
- paste-ready `article.html`
- cover and all figure originals
- `发布说明.txt`
- zip package

The release note must include:

- primary title and alternates
- summary
- paste flow
- image list in article order
- visual production route for each image: multimodal / deterministic / licensed web image
- source and license for every web image
- unresolved placeholders
- sensitive wording cautions
- quote confirmation notes

## 六、Final QA Statement

Before delivery, write a short final QA statement in `发布说明.txt`:

```
上线检查:
- 手机 390px 预览:已检查 / 问题已修正
- AI 腔扫描:已清理
- 图片职责:每张已标注
- 图片可读性:已检查
- 数字与事实:已对照清单
- 授权与来源:已登记
```

If any item is not checked, the package is still a draft.
