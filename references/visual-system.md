# Visual system

## Intent

Use the approved tactile owl editorial collage as the skill's stable default identity. Preserve its physical paper character, recurring owl narrator, handwriting, annotation language, legibility, hierarchy, corner furniture, and series consistency. Do not copy one composition across every card: the scene and information structure should still follow each card's content.

## Current default profile

Use this profile for every new series unless the user explicitly requests another direction:

- warm off-white or light beige coarse-fiber paper, slightly aged but still clean enough for phone reading;
- tactile scrapbook/editorial collage made from torn paper, clipped documents, taped notes, printed fragments, and real office objects with soft natural shadows;
- deep wine-red rough handwritten display titles; dark charcoal or ink-black supporting copy; deep blue pen arrows, circles, underlines, check marks, and marginal notes;
- olive green, pale blue, sand, kraft brown, and muted cream paper cards, with a restrained red accent from the character's scarf or key emphasis;
- a recurring anthropomorphic owl as narrator or witness: white facial disks, brown-and-black speckled feathers, large yellow eyes, a dark beak, a textured red scarf, and an army-green work jacket; keep its recognizable face and clothing consistent while changing pose and task;
- realistic photographic collage fused with hand-drawn editorial marks: tactile, calm, intelligent, slightly imperfect, and never glossy;
- no flat vector infographic, neon technology aesthetic, cyberpunk, glowing robot, sterile corporate UI, glossy 3D render, plastic surface, stock-advertising polish, or gratuitous gradients.

When the user explicitly changes the style, replace this profile for that work and keep the rest of the system unchanged unless requested. Do not drift away from this default merely because a new topic suggests a generic technology aesthetic.

## Approved visual references

When image inspection is available, inspect these files before generating the first cover:

- `../assets/default-style/01-cover-reference.jpg`
- `../assets/default-style/04-list-reference.jpg`
- `../assets/default-style/07-checklist-reference.jpg`

Use them to lock the character, paper, palette, handwriting, object realism, shadow depth, and information density. Their topic-specific words and layouts are examples, not reusable copy or templates. If the assets are unavailable, follow the written profile in this file.

## Canvas and grid

- Use an exact 3:4 portrait canvas. Preferred working size: 1242 × 1656 px.
- Native generation at 1086 × 1448 px is also accepted because it is an exact 3:4 ratio.
- Keep a safe margin of 72–96 px on all sides.
- Use a consistent underlying grid across the series, but vary image crops and module placement to serve the story.
- Reserve clean text zones before placing illustrations. Never solve a crowded layout by shrinking explanatory text below legibility.
- Use fine rules, brackets, small folio marks, or asymmetric columns as editorial structure, not decoration for its own sake.

## Typography hierarchy

Use no more than three text levels plus corner furniture:

1. Display/concept: dominant, high contrast, normally 96–168 px depending on length.
2. Card headline/key phrase: bold or semibold, normally 48–72 px.
3. Explanation: regular or medium, normally 30–40 px with generous line spacing.
4. Corner furniture/caption: normally 22–28 px, still legible on a phone.

Use one Chinese display family and one highly legible Chinese text family at most. Allow an English serif or sans accent only when it adds editorial rhythm. Avoid fake bolding, condensed glyph distortion, excessive typefaces, and long vertical body copy.

For native image generation, describe typography by visible character rather than by an unavailable font name: rough wine-red hand-lettered title, neat dark-ink supporting copy, and blue-pen annotation. Every required Chinese string must be supplied verbatim in the prompt and generated as part of the same image. Do not add a text layer afterward.

## Cover

- Center the main title optically, not merely mathematically.
- Enlarge and embolden the concept term and key promise.
- Keep the title readable at feed-thumbnail size.
- Build one coherent desk, document, or project scene around the owl; collage elements must belong to that scene rather than becoming unrelated symbols.
- Limit secondary copy. The cover should create curiosity without hiding what concept is being explained.
- When the user asks to keep a source title, reproduce it verbatim even if it is longer than a typical Xiaohongshu headline; solve the hierarchy through line breaks and scale, not rewriting.

## Content cards

- Let copy determine composition.
- Assign one dominant reading path per card.
- Use the owl's action, real desk objects, archival-like cutouts, documents, diagrams, and paper modules to make the abstract concrete.
- Separate text from busy image regions using negative space, a quiet paper field, a solid block, or a clearly bounded module.
- Use labels, arrows, brackets, and comparisons only when they explain a relationship.
- Preserve the warm paper, wine-red, blue-ink, olive, pale-blue, and sand family across topics. Topic variation should come from the props, documents, scene, and information structure rather than abandoning the palette.
- Define the semantic relationship before selecting a visual metaphor. For transformation stories, write the intended input, transformation, and output first; every line, node, particle, or label must correspond to that relationship.
- Give directional flows a clear origin, destination, boundary, and convergence behavior. Avoid static text walls, random word clouds, fan-shaped radiation, or decorative particle fields when they do not encode meaning.
- Convert rejected structures into positive constraints. For example, replace “not a fan shape” with “one bounded channel whose upper and lower banks progressively narrow toward a single inlet.”

## Color and texture

- Start with warm, coarse-fiber paper and the approved wine-red, deep-blue, olive, pale-blue, sand, kraft, and cream palette.
- Use deep wine red primarily for display titles, deep blue for explanatory arrows and marks, dark ink for body copy, and the remaining muted colors for paper modules and props. Ensure accessible text contrast.
- Make torn edges, fibers, tape, clipped paper, slight misregistration, and natural object shadows visible enough to feel physical, but keep texture away from small text.
- Keep the owl's red scarf and army-green jacket stable as character anchors.
- Prefer the clean cream-paper background and real wooden workbench seen in the approved references. Do not revert to a full-bleed saturated blue paper field.
- Keep large subject glyphs standard, complete, and readable. Do not let grain, blur, particles, or flow lines erode their defining strokes.

## Fixed corner furniture

Place `2026`, `RiXi`, `AI`, and the topic-derived `{{关键词}}` in stable positions. Replace the placeholder with no more than four displayed characters. Suggested system:

- top-left: `2026`
- top-right: `{{关键词}}`
- bottom-left: `RiXi`
- bottom-right: `AI`

Use the same type size, inset, and alignment on every card. Move the whole system only when the chosen template establishes another consistent arrangement.
