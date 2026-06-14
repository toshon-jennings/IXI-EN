# Ian Xiaohei Illustrations

> Transform the judgments, processes, states, and metaphors in Chinese articles into white-background, hand-drawn, quirky yet clean body illustrations.
>
> Landscape 16:9 | Xiaohei IP | Pure white hand-drawn | Minimal red/orange/blue Chinese annotations | Codex Skill

---

## What Is This Repository

IXI-EN is an English version of Ian Xiaohei Illustrations, "a Codex Skill that guides AI Agents to generate body illustrations for Chinese articles, posts, blogs, Notion documents, and methodology content." I have not only translated the text of the repo into English, but the output of the skill itself. Also, this skill is designed to be available to all agents.


Translated from [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations/tree/main):

It is not a general-purpose illustration prompt, nor a PPT infographic template. Its core goal is: first, to understand the cognitive anchors in an article; then, turn one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explanatory illustration.

The default visual IP is "Xiaohei" (Little Black): a small solid-black creature with white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, not a sticker, not a decorative figure standing in the corner — but an absurd worker genuinely participating in the system's operation.

In one sentence: **make AI do more than "add an image" — draw one key cognitive action from the article.**

---

## Who Is This For

Best suited for:

- People who write (English) articles and need body illustrations and article images
- Creators of knowledge content, methodology content, and AI workflow content
- People who want to turn abstract judgments into concrete metaphors
- People who want an illustration style that is lighter, quirkier, and more personally distinctive than PPT infographics
- People using AI agents for content production who want to reuse a consistent visual language

Not suited for:

- People who want commercial illustrations, brand KV, or polished flat illustrations
- People who want traditional PPT infographics, complex architecture diagrams, or flowcharts
- People who want children's cartoons, cute IP, or emoji-style art
- People who want to cram large blocks of text, long explanations, or full course pages into a single image
- People who need strictly editable vector source files

---

## What It Produces

Default output:

- Landscape 16:9 body illustrations
- A shot list of 4-8 images per article
- For each image: theme, core meaning, structure type, Xiaohei's action, and suggested (English) annotations
- Final PNG images saved to `assets/<article-slug>-illustrations/` in the workspace

Not produced by default:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover KV
- Large text-based infographics

---

## Visual Style

This skill defaults to Ian's "Xiaohei quirky body illustration" style:

- Pure white background — no paper texture, beige, shadows, or gradients
- Black hand-drawn line art, thin lines, slight wobble
- Generous white space — the main subject occupies roughly 40%-60% of the frame
- Small amounts of red, orange, and blue handwritten (English) annotations
- Each image expresses only one core action, structure, state, or metaphor
- Xiaohei must participate in the core action — never just decoration
- Quirky, creative, and clean — but not childish, not cute

---

## Example Output

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish, Many Uses

![One Fish, Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](images/examples/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style calibration samples, not composition templates. When using this skill, you should reinvent metaphors from the current article — do not copy the objects and compositions from old examples.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/toshon-jennings/IXI-EN.git
cd IXI-EN
```

Copy the skill to your Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installation, use in Codex:

```text
Use $ian-xiaohei-illustrations to design and generate 5 quirky Xiaohei body illustrations for this article.
```

---

## How to Use

### Illustration Planning Only

```text
Use $ian-xiaohei-illustrations — don't generate images yet.
Please analyze where this article would benefit from illustrations, and output a shot list of about 5 images.
For each image, specify: which paragraph it follows, the theme, core meaning, structure type, what Xiaohei is doing, and suggested ENglish annotation words.

<paste article>
```

### Generate Body Illustrations Directly

```text
Use $ian-xiaohei-illustrations to generate 4 quirky Xiaohei body illustrations from the article below.
Requirements: landscape 16:9, pure white background, black hand-drawn line art, small amounts of red/orange/blue handwritten English annotations.

<paste article>
```

### Generate One Image for a Single Concept

```text
Use $ian-xiaohei-illustrations to generate a body illustration for: "Trust isn't shouted into existence — it's paved with evidence, piece by piece."
The image should be quirky but clean. Xiaohei must perform the core action.
```

### Remove Titles or Incorrect Text from an Image

```text
Use $ian-xiaohei-illustrations to edit this image — remove the "Flowchart" title in the top-left corner, keep everything else unchanged.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

The skill's workflow:

1. Read the article, Markdown, Notion content, screenshots, or topic provided by the user
2. Extract core viewpoints, cognitive transitions, process structures, and visualization-worthy passages
3. Output a shot list first: each image addresses only one cognitive anchor
4. For each image, select a structure type: Workflow, system detail, before/after comparison, character state, concept metaphor, method layering, map route, or mini-comic panels
5. Reinvent a low-tech, quirky-but-coherent physical metaphor
6. Make Xiaohei perform the core action
7. Generate each image individually using the image model
8. Check against the QA checklist: white background, white space, Xiaohei action, English annotations, non-PPT feel, non-old-example-replica
9. Save final PNGs and report usage and file paths

---

## Directory Structure

```
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
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The subdirectory that needs to be installed into Codex is:

```
ian-xiaohei-illustrations/
```

The root-level README, LICENSE, NOTICE, and examples are GitHub sharing documentation.

---

## Notes

- The shorter the English text in the image, the more stable the generation.
- Each image should convey only one core structure — don't turn the article into an instruction manual.
- Xiaohei must perform the core action; if the image still makes complete sense with Xiaohei removed, Xiaohei is too decorative.
- Example images are for calibrating line density, white space, color restraint, and Xiaohei participation style only — do not copy their compositions.
- AI image models may produce wrong characters, hallucinated labels, style drift, or unnecessary titles — check after generation.
- If English character errors are severe, prioritize reducing annotation words and regenerating.

---

## Related Projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — Chinese hand-drawn PPT-style page illustration generation Skill
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — Curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — Guide to building a personal knowledge base with Obsidian + Claude AI

---

## [About Ian](https://github.com/helloianneo) — Product Designer / One-Person Company Practitioner / AI Builder


---

## License

MIT License. See [LICENSE](LICENSE).
