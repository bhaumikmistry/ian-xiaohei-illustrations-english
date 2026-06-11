# Image Generation Prompt Template

Generate each image separately. Replace variables based on article content — don't combine multiple images into one.

```text
Generate one standalone 16:9 horizontal article illustration.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art. Slightly wobbly pen lines. Lots of empty white space. Sparse red/orange/blue handwritten English annotations. Clean absurd product-sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
{character description from the active character's IP file — include appearance, expression, and how it participates}

Theme:
{illustration theme}

Structure type:
{structure type: Workflow / System Partial / Before-After Comparison / Role State / Concept Metaphor / Method Layers / Map Route / Mini Comic Panels}

Core idea:
{the core meaning this image should express}

Composition:
{specific scene: where the character is, what it's doing, what the main objects are, how information flows}

Suggested elements:
{element 1} / {element 2} / {element 3} / {element 4}

Handwritten labels:
{label 1} / {label 2} / {label 3} / {label 4} / {optional label 5}

Color use:
Black for main line art and character. Orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue only for secondary notes or feedback/system state.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten English labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## Character-Specific Prompt Blocks

When filling the "Recurring IP character required" section, use these per character:

### Xiaohei

```text
Xiaohei, a small solid-black absurd creature with white dot eyes, tiny thin legs, blank serious expression, slightly uneven hand-drawn body shape. Xiaohei must perform the core conceptual action, not decorate the scene. Make Xiaohei serious, deadpan, and slightly bizarre, not cute.
```

### Haku

```text
Haku, a tall narrow floating spirit with a solid black robe-like body that fades away at the bottom (no legs, no feet). White oval mask face with two simple dark oval eyes (no pupils), a small minimal mouth mark, and grey/purple tear-like marks under each eye. Dark hands visible, extending from the robe. Haku must embody or channel the core process — it IS the filter, gate, or conduit, not just standing beside it. Make Haku silent, mysterious, and deliberate, not scary or cute.
```

## Image Editing Prompts

Remove top-left title:

```text
Edit the provided image. Remove only the handwritten title "{text to remove}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

Enhance character participation:

```text
Regenerate this illustration with the same core meaning and simple layout, but make the character more central to the conceptual action. The character should be doing the strange work that explains the idea, not standing beside the diagram. Keep it clean, sparse, hand-drawn, and not cute.
```
