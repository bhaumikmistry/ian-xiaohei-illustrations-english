---
name: ian-xiaohei-illustrations
description: Generate Ian-style inline article illustrations. Used when users ask to generate "absurd," "Xiaohei," "hand-drawn," "inline illustrations," "article illustrations," "illustration suggestions," "shot list," "remove title/edit image" for articles, blog posts, Notion documents, workflow docs, methodology, processes, structures, states, metaphors, or viewpoints. Defaults to Xiaohei IP, pure white hand-drawn style, sparse red/orange/blue annotations, clean yet imaginative visual style.
---

# Ian Xiaohei Absurd Inline Illustrations

## Core Positioning

Design and generate 16:9 landscape inline illustrations for articles. The goal is not commercial illustration, PPT infographics, or cute cartoons — it's to turn the article's key judgments, processes, structures, states, or metaphors into a clean, absurd, creative, readable (but not manual-like) hand-drawn explanatory illustration.

The default visual IP is "Xiaohei": solid black, white dot eyes, thin legs, blank expression — seriously doing something absurd but valid. Xiaohei must participate in the image's core action, not just stand on the side as decoration.

## Read These References First

Load as needed per task — don't stuff all into context at once:

- `references/style-dna.md`: Style DNA, colors, text, prohibitions.
- `references/xiaohei-ip.md`: Xiaohei IP's appearance, personality, action library, and prohibitions.
- `references/composition-patterns.md`: Structure types, original metaphor methods, and anti-copying rules.
- `references/prompt-template.md`: Single image generation prompt template.
- `references/qa-checklist.md`: Post-generation checking and iteration rules.
- `assets/examples/`: Only for low-frequency visual calibration — do not enter the default generation path. Do not copy these examples' compositions, objects, or annotations.

## Workflow

### 1. Digest the Article

First read the user's article, link, Notion page, Markdown file, or screenshot content. Extract:

- What is the core viewpoint
- Which paragraphs carry cognitive turning points
- Which content is suitable for visual explanation
- Which parts are better as text only — no image needed

Don't distribute illustrations evenly. Prioritize "cognitive anchors," for example: core judgments, two breakpoints, input-output loops, branching, before/after comparisons, one-fish-many-uses, handoff paths, common pitfalls, role state changes.

### 2. Output Illustration Strategy First

If the user only says "analyze where to add illustrations / think about which parts need illustrations," give a shot list first. Specify for each image:

- Placement (after which paragraph)
- Image theme
- Core meaning
- Structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested English annotation labels

Default 4-8 images. For short articles, 1-3; for long articles, don't easily exceed 9. Enough is enough — avoid turning the article into a picture book.

### 3. Single Image Generation

If the user explicitly asks to "generate / output / make images / help me generate," don't stop and wait for confirmation; use the built-in `image_gen` to generate each image separately. Don't combine multiple images into one.

Each image covers only one core structure. The prompt must include:

- 16:9 landscape inline article illustration
- Pure white background
- Black hand-drawn line art
- Sparse red/orange/blue handwritten English annotations
- Generous whitespace
- Xiaohei as the core action subject
- Prohibit PPT, commercial illustration, childish/cute, complex architecture, type-label titles in top-left corner

Do not copy past examples. Examples only provide style density and how Xiaohei participates — you cannot directly reuse compositions like "conveyor belt breakpoints / Xiaohei pulling lines / material fish / stamp toolbox / common pitfalls path," unless the user explicitly asks to replicate a specific image. Every time, reinvent a strange but valid metaphor from the current article.

### 4. Check and Iterate

After generation, check `references/qa-checklist.md`. If these problems appear, prioritize regeneration or partial editing:

- Xiaohei is only decorative
- Image is too crowded
- Too similar to a flowchart/PPT
- Too much text or severe typos
- Top-left corner shows titles like "Common Pitfalls/Flowchart/System Architecture"
- Style is too cute, childish, or rigid
- Background isn't clean white

### 5. Save and Deliver

If the user is working within a workspace, copy final images to:

```text
assets/<article-slug>-illustrations/
```

Name sequentially:

```text
01-topic-name.png
02-topic-name.png
```

Keep original generated files — don't overwrite existing assets unless the user explicitly asks for replacement.

## Output Guidelines

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- Each image's purpose
- File paths
- Which images are strongest, which are optional

Don't write long explanations about style theory; let the images speak for themselves.
