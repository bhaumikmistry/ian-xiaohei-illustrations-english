# Ian Xiaohei Illustrations

> Turn the judgments, processes, states, and metaphors in articles into white-background, hand-drawn, absurd yet clean inline illustrations.
>
> 16:9 Landscape | Xiaohei IP | Pure White Hand-drawn | Sparse Red/Orange/Blue English Annotations | Codex Skill

---

## What Is This Repository

Ian Xiaohei Illustrations is a Codex Skill that guides AI Agents to generate inline illustrations for articles, blog posts, Notion documents, and methodology content.

It is not a generic illustration prompt, nor a PPT infographic template. Its core goal is: first understand the cognitive anchors in an article, then turn one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explanatory illustration.

The default visual IP is "Xiaohei": a solid-black, white-dot-eyed, thin-legged, blank-expression small character. Xiaohei is not a mascot, not a sticker, not a decoration standing in the corner — it is an absurd worker seriously participating in the system's operation.

In one sentence: **Make AI not just "add an illustration," but draw out a key cognitive action from the article.**

---

## Who Is This For

Especially suitable for:

- People writing articles who need inline illustrations
- People creating knowledge content, methodology content, or AI workflow content
- People who want to turn abstract judgments into concrete metaphors
- People who want an illustration style that is lighter, stranger, and more personally recognizable than PPT infographics
- People using Codex for content production who want to consistently reuse a visual language

Not suitable for:

- People who want commercial illustrations, brand KVs, or polished flat illustrations
- People who want traditional PPT infographics, complex architecture diagrams, or flowcharts
- People who want children's cartoons, cute IPs, or emoji-style art
- People who want to cram lots of body text, long explanations, or entire course pages into one image
- People who need strictly editable vector source files

---

## What It Produces

Default output:

- 16:9 landscape inline illustrations
- A 4-8 image shot list for an article
- Each image's theme, core meaning, structure type, Xiaohei's action, and annotation suggestions
- Final PNG images, saved to `assets/<article-slug>-illustrations/` in the workspace

Does not output by default:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover KVs
- Text-heavy infographics

---

## Characters

This skill supports multiple character IPs. Each character has a distinct role:

| Character | Style | Best For |
|-----------|-------|----------|
| **Xiaohei** (default) | Small solid-black blob, white dot eyes, thin legs, deadpan | Hands-on work: carrying, pulling, pressing, operating, sorting |
| **Haku** | Tall floating spirit, black fading robe, white mask, tear marks, visible hands | Flow, transitions, hidden processes, thresholds, absorption, transformation |

You can specify which character to use ("use Haku"), or let the skill pick based on the article's theme.

### Adding a New Character

You can ask the skill to create a new character:

```text
Use $ian-xiaohei-illustrations — I want to create a new character for my illustrations.
```

The skill will interview you about the character's appearance, personality, actions, and prohibitions, then generate a definition file and test images. Once approved, the character is available for all future illustrations.

See `ian-xiaohei-illustrations/references/xiaohei-ip.md` and `ian-xiaohei-illustrations/references/haku-ip.md` for examples of character definitions.

---

## Visual Style

This skill uses Ian's "Absurd Inline Illustration" style by default:

- Pure white background — no paper texture, cream, shadows, or gradients
- Black hand-drawn line art, thin lines, slightly wobbly
- Generous whitespace — subject takes up only about 40%-60% of the canvas
- Sparse red, orange, blue handwritten English annotations
- Each image expresses only one core action, structure, state, or metaphor
- The active character must participate in the core action — cannot be mere decoration
- Absurd, creative, clean — but not childish, not cutesy

---

## Example Results

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish Many Uses

![One Fish Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](examples/images/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style calibration examples, not composition templates. When using the skill, you should reinvent metaphors from the current article — do not copy the objects and compositions from old examples.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/bhaumikmistry/ian-xiaohei-illustrations-english.git
cd ian-xiaohei-illustrations-english
```

Copy the skill to the Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installation, use in Codex:

```text
Use $ian-xiaohei-illustrations to design and generate 5 Xiaohei absurd inline illustrations for this article.
```

---

## How to Use

### Illustration Planning Only

```text
Use $ian-xiaohei-illustrations — don't generate images yet.
Analyze this article for where illustrations would add value, and output a shot list of about 5 images.
For each image specify: placement (after which paragraph), theme, core meaning, structure type, what Xiaohei is doing, and suggested annotation labels.

<paste article>
```

### Generate Inline Illustrations Directly

```text
Use $ian-xiaohei-illustrations to generate 4 Xiaohei absurd inline illustrations for this article.
Requirements: 16:9 landscape, pure white background, black hand-drawn line art, sparse red/orange/blue handwritten English annotations.

<paste article>
```

### Generate One Image for a Single Concept

```text
Use $ian-xiaohei-illustrations to generate one inline illustration for: "Trust isn't something you shout — it's something you build one piece of evidence at a time."
The image should be absurd yet clean, and Xiaohei must perform the core action.
```

### Use a Specific Character

```text
Use $ian-xiaohei-illustrations with Haku to generate one inline illustration for: "Data flows through layers of processing before the user ever sees it."
```

### Create a New Character

```text
Use $ian-xiaohei-illustrations — I want to create a new character for my illustrations.
```

### Remove a Title or Incorrect Text from an Image

```text
Use $ian-xiaohei-illustrations — edit this image, remove the "Flowchart" title in the top-left corner, and keep everything else unchanged.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

This skill's workflow is:

1. Read the article, Markdown, Notion content, screenshot, or user-provided theme
2. Extract core viewpoints, cognitive turning points, process structures, and paragraphs suitable for visualization
3. First output a shot list: each image selects only one cognitive anchor
4. Choose a structure type for each image: Workflow, System Partial, Before/After Comparison, Role State, Concept Metaphor, Method Layers, Map Route, or Mini Comic Panels
5. Reinvent a low-tech, absurd but valid physical metaphor
6. Have Xiaohei perform the core action
7. Generate each image individually via the image model
8. Check against the QA checklist: white background, whitespace, Xiaohei's action, annotations, non-PPT feel, no old-example copying
9. Save final PNGs and report their purpose and file paths

---

## Directory Structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    ├── tests/
    │   └── character-test-prompts.md
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── haku-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The subdirectory that actually needs to be installed into Codex is:

```text
ian-xiaohei-illustrations/
```

The root-level README, LICENSE, NOTICE, and examples are GitHub-facing documentation.

---

## Important Notes

- Shorter text in illustrations produces more stable results.
- Each image should cover only one core structure — don't turn the article into a manual.
- Xiaohei must perform the core action; if the image still works perfectly without Xiaohei, then Xiaohei is too decorative.
- Example images are only for calibrating line density, whitespace, color restraint, and how Xiaohei participates — do not copy their compositions.
- AI image models may produce typos, hallucinated labels, style drift, or unwanted titles — check after generation.
- If text errors are severe, prioritize reducing annotation count and regenerating.

---

## Related Projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — Hand-drawn technical PPT-style page illustration generation Skill
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — Curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — Obsidian + Claude AI personal knowledge base setup guide

---

## Credits

**Created by Ian (Ian Xiaohei)** — Product Designer / Solo Company Practitioner / AI Builder

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)
- WeChat: `ianneoxyz`
- Email: hello.neoc@gmail.com

**Translated to English by Bhaumik Mistry**

- GitHub: [bhaumikmistry](https://github.com/bhaumikmistry)

---

## Keep Exploring

This Xiaohei illustration Skill is just one small tool in the personal production system I've built with AI.

If you're also using AI for content, knowledge bases, workflows, or productization, check out my website: [www.ianneo.xyz](https://www.ianneo.xyz).

If you just want to observe first, follow my [X/Twitter](https://x.com/ianneo_ai).

To learn about the Indie Builders Club, add me on WeChat: `ianneoxyz`, with note "OPC".

<p>
  <img src="assets/ian-wechat-qr.jpg" alt="Ian WeChat QR Code" width="120">
</p>

If you can't scan the code, search WeChat for: `ianneoxyz`.

---

## License

MIT License. See [LICENSE](LICENSE).
