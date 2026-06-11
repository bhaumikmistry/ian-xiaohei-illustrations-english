# Image Generation Prompt Template

Generate each image separately. Replace variables based on article content — don't combine multiple images into one.

```text
Generate one standalone 16:9 horizontal article illustration.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art that looks like quick pen sketches on paper — wobbly, imperfect, organic lines with natural line weight variation (thinner for details, thicker for main objects). Lots of empty white space. Sparse red/orange/blue handwritten English annotations scattered organically (not aligned or evenly spaced). The overall feeling should be someone explaining an idea by sketching on a whiteboard — casual, fast, inventive, not polished. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI, no clean geometric shapes.

Scene storytelling:
The illustration must tell a micro-story — not just show objects, but show objects INTERACTING. Something is happening: being poured, cut, carried, stuck, flowing, falling, being pushed through. The scene should have a narrative "punchline" — one slightly absurd thing that makes the viewer smile and then immediately understand the concept. Think: a fish being sliced on a cutting board to represent content repurposing, or items falling into pits in the ground to represent common mistakes, or experiences being poured into a fermentation jar.

Recurring IP character required:
{character description from the active character's IP file — include appearance, expression, and how it participates}

Theme:
{illustration theme}

Structure type:
{structure type: Workflow / System Partial / Before-After Comparison / Role State / Concept Metaphor / Method Layers / Map Route / Mini Comic Panels}

Core idea:
{the core meaning this image should express}

Composition:
{specific scene description — must include:
- A concrete physical metaphor (not abstract shapes or generic boxes)
- What the character is physically doing (body posture, hands, lean direction)
- How objects relate to each other spatially (on top of, flowing into, connected by)
- The direction of narrative flow (usually left-to-right or top-to-bottom)
- One slightly absurd or surprising element that makes the metaphor memorable}

Suggested elements:
{specific physical objects — NOT abstract concepts. Examples: cutting board, fermentation jar, conveyor belt, well, pit in ground, mailbox, lever, rope, ladder, funnel, pipe}

Handwritten labels:
{label 1} / {label 2} / {label 3} / {label 4} / {optional label 5}
(Place these organically near what they describe — tilted, casual, like margin notes, not centered or formal)

Color use:
Black for main line art and character. Orange for main flow/path/arrows/connections. Red only for key warnings/problems/results/emphasis. Blue only for secondary notes or system state (use sparingly — not every image needs blue).

Line style guidance:
- Main objects: slightly thicker, confident wobbly lines
- Details and small elements: thinner, sketchier lines
- Annotations: handwritten feel, slightly tilted, not straight
- Arrows: hand-drawn, not perfectly curved, organic
- Character body: adapts shape to the action (squished if carrying weight, leaning if pulling, stretched if reaching)

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten labels. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, or dense explainer. Do not use generic boxes/circles/arrows as the main visual — always ground the metaphor in a specific physical object or scene. Do not copy prior examples or reuse known case compositions unless explicitly requested; invent a fresh visual metaphor for this specific article. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## Character-Specific Prompt Blocks

When filling the "Recurring IP character required" section, use these per character:

### Xiaohei

```text
Xiaohei, a small solid-black absurd creature with white dot eyes, tiny thin legs, blank serious expression. Body shape is organic and adapts to the action — pear-shaped when standing, squished when carrying weight, leaning forward when cutting or working, stretched when reaching. Slightly uneven hand-drawn silhouette, never perfectly round or symmetrical. Xiaohei must physically interact with the scene's objects — cutting, carrying, pulling, stuck inside, operating a lever, feeding things into a machine. Not standing beside the action. Deadpan and serious about absurd tasks. Not cute.
```

### Haku

```text
Haku, a tall narrow floating spirit with a solid black robe-like body that fades/dissolves at the bottom (no legs, no feet — just wisps). White oval mask face with two simple dark oval eyes (no pupils), a small minimal mouth mark, and grey/purple tear-like marks running down from under each eye. Dark hands always visible, extending from the robe to interact with the scene. Haku's body can serve AS a structure — it can BE the doorway, the filter, the channel, the container. Things can flow into and out of Haku's body. Haku must embody or channel the core process, not just stand beside it. Silent, mysterious, deliberate — not scary, not cute, not frantic.
```

## Composition Guidance by Example

These describe the QUALITY of composition to aim for — not specific scenes to copy:

- **Narrative flow**: Objects should tell a story left-to-right or have a clear spatial relationship (pouring into, stacking on, flowing through). Never just float in isolation.
- **Specific objects over abstractions**: A fermentation jar with liquid inside > a generic circle labeled "process." A fish on a cutting board being sliced > an arrow pointing to three boxes.
- **Character integration**: The character's body TOUCHES or is INSIDE the scene objects. Xiaohei's hands hold the knife, Haku's body IS the doorframe.
- **Absurd punchline**: One element should be slightly surprising — too big, too small, in the wrong place, doing the wrong job. This is what makes it memorable.
- **Organic annotation placement**: Labels are scattered where they naturally fit — tilted, near margins, with casual dashed lines pointing to things. Never centered, never in a row.

## Image Editing Prompts

Remove top-left title:

```text
Edit the provided image. Remove only the handwritten title "{text to remove}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

Enhance character participation:

```text
Regenerate this illustration with the same core meaning and simple layout, but make the character more physically integrated into the scene. The character should be TOUCHING, HOLDING, or INSIDE the main objects — not floating beside them. Keep the hand-drawn wobbly line quality, keep it sparse, keep it absurd but clear.
```

Too generic / too abstract:

```text
Regenerate this illustration. The current version uses generic shapes (boxes, circles, arrows). Replace them with a specific physical metaphor — a real-world object that is slightly absurd in this context. Think: machines, jars, cutting boards, wells, conveyor belts, pits, pipes, ladders, mailboxes. The character should physically interact with this object. Keep the hand-drawn wobbly style and white background.
```
