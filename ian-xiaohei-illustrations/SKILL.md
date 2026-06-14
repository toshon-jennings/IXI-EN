---
name: ian-xiaohei-illustrations
description: Generate Ian-style Chinese article body illustrations. Use when the user asks to create "quirky", "Xiaohei", "hand-drawn", "body illustrations", "article images", "illustration suggestions", "shot list", "remove title / edit image" for Chinese articles, posts, blogs, Notion documents, workflow documents, methodologies, processes, structures, states, metaphors, or viewpoints. Defaults to the Xiaohei IP, pure white hand-drawn style, minimal red/orange/blue annotations, clean yet wildly creative visual language.
---

# Ian Xiaohei Quirky Body Illustrations

## Core Positioning

Design and generate landscape 16:9 body illustrations for Chinese articles. The goal is not commercial illustration, PPT infographics, or cute cartoons — but transforming key judgments, processes, structures, states, or metaphors from an article into a clean, quirky, creative, readable hand-drawn explanatory illustration that doesn't read like an instruction manual.

The default visual IP is "Xiaohei": solid black, white dot eyes, thin legs, blank expression, seriously doing something absurd but coherent. Xiaohei must participate in the core action of the image — never just standing aside as decoration.

## Read These References First

Read as needed for the task — don't load all of them into context at once:

- `references/style-dna.md`: Style DNA, colors, text, and prohibitions.
- `references/xiaohei-ip.md`: Xiaohei IP appearance, personality, action library, and prohibitions.
- `references/composition-patterns.md`: Structure types, original metaphor creation method, and anti-repetition rules.
- `references/prompt-template.md`: Single-image generation prompt template.
- `references/qa-checklist.md`: Post-generation checking and iteration rules.
- `assets/examples/`: For low-frequency visual calibration only — not part of the default generation path. Do not copy compositions, objects, or annotations from these examples.

## Workflow

### 1. Digest the Article

First read the user's article, link, Notion page, Markdown file, or screenshot content. Extract:

- What is the core viewpoint
- Which paragraphs carry cognitive transitions
- Which content is suitable for illustration
- Which parts are better left as text only

Don't distribute illustrations evenly. Prioritize "cognitive anchors" — e.g., core judgments, two breakpoints, input/output loops, splits, before/after comparisons, one-input-many-outputs, handoff paths, common pitfalls, character state changes.

### 2. Output Illustration Strategy First

If the user just asks to "analyze how to illustrate / think about where images are needed", provide a shot list first. For each image, specify:

- Which paragraph it follows
- The image theme
- Core meaning
- Structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested Chinese annotation words

Default 4-8 images. For short articles, 1-3 images; for long articles, don't exceed 9 without good reason. Enough is enough — don't turn the article into a picture book.

### 3. Single Image Generation

If the user explicitly asks to "generate / output / make / help me generate", don't wait for confirmation — generate each image individually using the built-in `image_gen`. Don't compose multiple images into one.

Each image conveys only one core structure. The prompt must include:

- Landscape 16:9 Chinese body illustration
- Pure white background
- Black hand-drawn line art
- Small amounts of red/orange/blue handwritten Chinese annotations
- Generous white space
- Xiaohei as the core action subject
- No PPT, commercial illustration, childish cute, complex architecture, top-left type titles

Don't replicate past examples. Examples only provide style density and Xiaohei participation patterns — don't directly reuse known compositions like "conveyor belt breakpoints / Xiaohei pulling judgment lever / Xiaohei sorting funnel / Xiaohei cutting material fish" unless the user explicitly requests a replica of a specific image. Each time, reinvent a strange-but-coherent metaphor from the current article.

### 4. Check and Iterate

Check against `references/qa-checklist.md` after generation. If any of the following issues appear, prioritize regeneration or local editing:

- Xiaohei is just decoration
- Image is too cluttered
- Too much like a flowchart/PPT
- Too many Chinese characters or severe wrong characters
- Top-left corner has titles like "Common Pitfalls / Workflow / System Architecture / Roadmap"
- Style is too cute, childish, or rigid
- Background is not clean white
- Severe Chinese annotation errors

### 5. Save and Deliver

If the user is working within a workspace, copy final images to:

```
assets/<article-slug>-illustrations/
```

Name them sequentially:

```
01-topic-name.png
02-topic-name.png
```

Preserve existing generated files — don't overwrite existing assets unless the user explicitly requests replacement.

## Output Format

Strategy output before generation should be concise and precise. Post-delivery output should include:

- How many images were generated
- The purpose of each image
- Save paths
- Which images are most reliable, which are optional

Don't write long explanations of style theory — let the images speak for themselves.
