---
name: ian-xiaohei-illustrations
description: Generate Ian-style inline article illustrations. Used when users ask to generate "absurd," "Xiaohei," "Haku," "hand-drawn," "inline illustrations," "article illustrations," "illustration suggestions," "shot list," "remove title/edit image," or "create a new character" for articles, blog posts, Notion documents, workflow docs, methodology, processes, structures, states, metaphors, or viewpoints. Supports multiple character IPs. Defaults to Xiaohei IP, pure white hand-drawn style, sparse red/orange/blue annotations, clean yet imaginative visual style.
---

# Ian Absurd Inline Illustrations

## Core Positioning

Design and generate 16:9 landscape inline illustrations for articles. The goal is not commercial illustration, PPT infographics, or cute cartoons — it's to turn the article's key judgments, processes, structures, states, or metaphors into a clean, absurd, creative, readable (but not manual-like) hand-drawn explanatory illustration.

## Characters

This skill supports multiple character IPs. Each character has its own definition file in `references/`:

| Character | File | Best For |
|-----------|------|----------|
| **Xiaohei** (default) | `references/xiaohei-ip.md` | Hands-on mechanical work: carrying, pulling, pressing, operating, sorting |
| **Haku** | `references/haku-ip.md` | Flow, transitions, hidden processes, thresholds, absorption, transformation |

### Character Selection

- If the user names a character ("use Haku", "with Xiaohei"), use that character.
- If the article theme matches a character's "Best Used For" section, suggest that character.
- If no preference is stated, default to Xiaohei.
- The user can also request "create a new character" — see the character creation workflow below.

The active character must participate in the image's core action, not just stand on the side as decoration.

## Read These References First

Load as needed per task — don't stuff all into context at once:

- `references/style-dna.md`: Style DNA, colors, text, prohibitions.
- `references/xiaohei-ip.md`: Xiaohei IP — appearance, personality, action library, prohibitions.
- `references/haku-ip.md`: Haku IP — appearance, personality, action library, prohibitions.
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
- Which character to use and what it's doing
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
- The active character as the core action subject (load its IP file for appearance and action details)
- Prohibit PPT, commercial illustration, childish/cute, complex architecture, type-label titles in top-left corner

Do not copy past examples. Examples only provide style density and how characters participate — you cannot directly reuse compositions unless the user explicitly asks to replicate a specific image. Every time, reinvent a strange but valid metaphor from the current article.

### 4. Check and Iterate

After generation, check `references/qa-checklist.md`. If these problems appear, prioritize regeneration or partial editing:

- Character is only decorative (not performing the core action)
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

---

## Character Creation Workflow

When the user says "create a new character," "I want a different character," "add a character," or similar — follow this process:

### Step 1: Interview

Ask the user these questions (adapt based on what they've already provided):

1. **Name** — What should we call this character?
2. **Visual reference** — Do you have an image, or can you describe the look? (shape, color, eyes, limbs)
3. **Vibe/personality** — What energy does it have? (serious, playful, mysterious, anxious, calm...)
4. **Role in illustrations** — What does this character DO? (builds things, observes, breaks things, flows through, guards...)
5. **Prohibitions** — What should it NEVER look like? (too cute, too scary, too detailed...)
6. **Best themes** — What article topics is this character best suited for?

If the user provides an image, extract the visual details from it. Skip questions they've already answered.

### Step 2: Generate the Character Definition

Create a markdown file following this exact structure:

```markdown
# {Name} IP

## Character Definition
{One paragraph: what this character is and its role in illustrations}

## Appearance
{Bullet list: body, color, eyes, limbs, expression, texture, scale}

## Personality
{Bullet list: 4-6 behavioral traits}

## Common Duties
{Bullet list: 8-12 typical actions this character performs in illustrations}

## Prohibitions
{Bullet list: 6-8 things this character must NEVER be}

## Best Used For
{Bullet list: themes/topics where this character works better than others}

## Quality Standard
{The "remove test" — how to know if the character is too decorative}
```

### Step 3: Save to Skill

Save the file to:

```text
references/{name}-ip.md
```

### Step 4: Update Skill References

Add the new character to the character table in this file (SKILL.md) under the "Characters" section, and add it to the "Read These References First" list.

### Step 5: Generate Test Images

Generate 3 test images to validate the character renders correctly:

1. **Basic form** — character alone on white background
2. **Core action** — character performing its signature action with a simple metaphor
3. **Comparison** — same theme rendered with both the new character and Xiaohei

Show results to the user. Iterate on the character definition if the rendering doesn't match intent.

### Step 6: Confirm

Once the user approves, the character is ready for use. Report:
- Character name and file path
- When to use this character vs. others
- Any adjustments made during testing
