# Xiaohongshu Concept Explainer

A Codex Skill for turning articles, notes, files, screenshots, images, and other source material into accurate, beginner-friendly Xiaohongshu knowledge infographics.

Designed primarily for Chinese-speaking readers who are curious about AI but may not have a technical background.

## What It Does

This Skill supports the complete production workflow for a Xiaohongshu knowledge post:

- Inspects mixed source material
- Selects a focused, publishable topic
- Verifies important claims using credible sources
- Builds a multi-card narrative
- Writes concise, beginner-friendly Chinese copy
- Designs a coherent 3:4 visual series
- Maintains character and art-direction consistency
- Checks typography, legibility, factual accuracy, and visual structure
- Learns reusable lessons from web-based debugging and revisions

It does not simply summarize everything in the source material. It identifies the smallest useful idea that can support one clear, valuable post.

## Supported Inputs

You can provide:

- Long-form articles
- Notes and fragments
- Keywords or topic ideas
- Word or PDF documents
- Screenshots
- Reference images
- Existing drafts
- Mixed combinations of the above

## Core Workflow

### 1. Topic Selection

The Skill inventories the supplied material and identifies up to three possible angles.

Each angle is evaluated for:

- Beginner value
- Editorial sharpness
- Factual support
- Story potential
- Visual potential
- Relevance

It recommends the strongest angle and defines what the post should and should not cover.

### 2. Research and Fact-Checking

Before drafting, the Skill verifies the concept with at least two credible or primary sources.

It separates:

- Verified facts
- Expert interpretations
- Analogies
- Inferences
- Uncertain or disputed claims

Definitions, boundaries, exceptions, dates, statistics, and causal claims are checked before publication.

### 3. Card Planning

The Skill plans the complete card series before generating images.

A typical narrative may include:

1. Cover
2. What it is
3. Why it matters
4. How it works
5. A concrete example
6. A memorable takeaway

The number of cards is determined by the topic. It is not locked to a fixed template.

### 4. Copywriting

Each card receives one primary editorial job.

The writing system prioritizes:

- Plain Chinese
- Short sentences
- Concrete verbs
- Early definitions
- Clear examples
- Essential limitations
- Fast mobile scanning

The final package includes:

- One recommended Xiaohongshu title
- Two alternative titles
- A post body of no more than 200 Chinese characters
- Optional hashtags when useful
- Card-by-card copy
- Sources for factual claims

### 5. Visual Production

Every card uses an exact 3:4 portrait ratio, preferably `1242 × 1656 px`.

The visual system emphasizes:

- Strong information hierarchy
- Clear reading paths
- Asymmetric editorial grids
- Directional composition
- Purposeful negative space
- Legible Chinese typography
- Consistent series-level art direction

Mechanical four-quadrant layouts, unnecessary symmetry, evenly filled pages, and repeated character placement are avoided.

Each card produces one formal version by default. When a problem is found, the current version is revised instead of generating more candidates. Alternative or A/B versions are created only when explicitly requested.

Important Chinese text should be typeset deterministically rather than entrusted to an image model.

### 6. Quality Assurance

Final cards are checked at both full size and thumbnail size.

QA covers:

- Factual accuracy
- Narrative continuity
- Exact Chinese wording
- Typography and contrast
- Safe margins
- Cropping and overflow
- Character consistency
- Clothing and anatomy logic
- Visual hierarchy
- Series consistency
- File order and naming
- Final image count

The Skill does not claim completion while text is garbled, clipped, inaccurate, difficult to read, or obstructed by illustrations.

## Series Consistency

Each new project starts by analyzing its own content and visual references.

Within a single series, the following should remain consistent:

- Character construction
- Linework
- Illustration material
- Color logic
- Typography hierarchy
- Layout language
- Rendering quality

A later card should not suddenly change art style.

However, the visual direction belongs to the current project. A previous project’s palette, composition, character, or illustration style should not be imposed on future projects.

## Optional Snowy Owl Mascot

The repository includes a dedicated snowy owl character reference.

It is loaded only when a project explicitly selects the snowy owl as its series character. The owl is not the default mascot for every Xiaohongshu project.

The reference defines:

- Core facial and feather characteristics
- Character-role variations
- Exactly two stick-figure arms for actions
- Clear separation between wings and hands
- Clothing and scarf construction
- Standing legs and grounded claws
- Prop selection
- Pose variation
- Series-level character consistency

See [`references/snowy-owl-mascot.md`](references/snowy-owl-mascot.md).

## Image-Generation Handoff

Image-generation capabilities can differ between ChatGPT and Codex surfaces.

When native image generation is unavailable, the Skill preserves the approved research, script, and visual plan, then prepares a structured handoff for another surface.

After the images are returned, the workflow continues with:

1. Character-structure QA
2. Deterministic Chinese typesetting
3. Full-size inspection
4. Thumbnail inspection
5. Final export

See [`references/image-handoff.md`](references/image-handoff.md).

## Example Prompt

```text
Use $xiaohongshu-concept-explainer to analyze the material I provide.

Recommend the strongest beginner-friendly topic, verify the important claims, plan the card series, write the Chinese copy, and create a consistent 3:4 Xiaohongshu knowledge-infographic post.
```

You can also provide more specific instructions:

```text
Use $xiaohongshu-concept-explainer to turn these notes and screenshots into a Xiaohongshu knowledge infographic for AI beginners.

First recommend the strongest topic angle. Do not generate images until I approve the card plan.
```

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── image-handoff.md
    ├── qa-checklist.md
    ├── snowy-owl-mascot.md
    ├── visual-system.md
    └── web-debug-feedback.md
```

## Design Principles

- Select before producing
- Verify before simplifying
- Plan before rendering
- Keep one primary message per card
- Maintain consistency within a series
- Let composition serve the narrative
- Revise the current version before adding alternatives
- Keep illustrations away from essential text
- Separate reusable rules from project-specific preferences
- Treat visual presets as replaceable, not permanent
