---
name: xiaohongshu-concept-explainer
description: Analyze mixed source material, select a strong beginner-friendly topic, research, plan, write, design, and quality-check Chinese Xiaohongshu knowledge-infographic posts with a unified editorial illustration style, a 3:4 vertical cover and card series, concise story-led explanations, title variants, and a body under 200 Chinese characters. Accept long text, notes, articles, keywords, files, screenshots, images, or combinations. Use when the user asks for 小红书选题分析、概念词解、知识片段、知识图解、概念科普、术语解释、图文笔记、知识卡片、封面及多图内容策划或出图。
---

# Xiaohongshu Concept Explainer

Turn raw, mixed-format material into an accurately researched and visually coherent Xiaohongshu knowledge post for AI-curious beginners. Select the topic before producing it; do not merely summarize everything the user provides.

## Non-negotiable workflow

Follow the gates in order. Do not generate final images before the topic and card plan are approved.

### Gate 0 — Understand the material and select the topic

Treat the default audience as Chinese-speaking beginners who may be interested in AI but have little prior knowledge. Override this only when the user specifies another audience.

1. Inventory every provided input: long text, note fragments, article excerpts, keywords, documents, screenshots, images, or mixed inputs.
2. Use the appropriate reading, OCR, document, image-inspection, or extraction capability for each input. Preserve headings, captions, diagrams, highlighted passages, source metadata, and relationships between inputs when they affect meaning.
3. Separate the material into:
   - central claims or concepts;
   - useful examples, tensions, and surprising facts;
   - evidence needing verification;
   - background that should not become the main story;
   - ambiguity, contradiction, promotional framing, or factual risk.
4. Do not default to the first keyword, the longest section, or a whole-document summary. Identify the smallest useful idea that can support one coherent post.
5. Generate up to three publishable topic angles. Evaluate each on:
   - beginner value: useful without prior knowledge;
   - sharpness: expressible as one clear promise or question;
   - correctness: verifiable without flattening essential nuance;
   - story potential: contains tension, contrast, consequence, or a concrete scene;
   - visual potential: supports at least four distinct cards without filler;
   - relevance: timely or enduring enough to justify a post.
6. Recommend one angle, state why it is stronger than the others, define what the post will and will not cover, and identify the likely reader takeaway. Include up to two alternatives when genuinely viable.
7. If no angle is strong enough, say why and recommend what additional material or reframing would make it publishable. Do not force a weak post.
8. Ask the user to confirm the recommended angle before committing to a full card plan. If the user explicitly authorizes autonomous selection, choose the strongest angle and continue while clearly stating the choice.

Keep the topic-selection response analytical rather than exhaustive. Show judgment, not a transcript of everything consumed.

### Gate 1 — Resolve the concept

1. Restate the approved angle as a single editorial question or promise. It may be a concept explanation, knowledge fragment, mechanism, misconception, comparison, mini-history, practical method, or other focused form.
2. Search the web before drafting. Cross-check at least two independent, authoritative or primary sources; use more for disputed, technical, medical, legal, financial, or fast-changing topics.
3. Establish three answers in working notes:
   - What is it?
   - Why does it matter or exist?
   - How is it used, recognized, or done?
4. Distinguish verified fact, expert interpretation, analogy, and inference. Never turn an analogy into a definition.
5. If a term, claim, or source has multiple common meanings or unclear scope, stop and ask the user which meaning they intend when the choice would materially change the post. Offer the likely interpretations in plain Chinese. Continue research after they choose.
6. Cite research links in the planning response. Prefer sources that directly support the exact claims used.

### Gate 2 — Confirm the card plan

Plan the full set before making images. Use at least four cards including the cover; there is no maximum. Choose the count based on the idea, not a fixed template.

Present a concise table containing card number, role, single core message, proposed headline, visual metaphor/material, and estimated text load. Recommend one total count and explain the reason in one sentence. Ask the user to confirm or revise the count and outline.

Default narrative arc when it fits:

1. Cover — curiosity and promise
2. What — one-sentence definition
3. Why — tension, cause, or origin
4. How — mechanism, use, or action
5. Example — concrete scene or contrast
6. Takeaway — memory hook or boundary

Merge or extend cards when needed. Give every non-cover card one primary job.

### Gate 3 — Write the content script

After plan approval, draft card-by-card copy. Apply these rules:

- Lead with a tiny scene, friction, reversal, or consequence when it improves understanding.
- State the definition early and plainly. Prefer one sharp sentence over stacked jargon.
- Preserve essential conditions, boundaries, and exceptions required for correctness.
- Keep each card scannable in about three seconds: one headline, one focal claim, and only the supporting text needed.
- Use short Chinese sentences and concrete verbs. Explain necessary jargon in place.
- Avoid invented quotations, fake statistics, exaggerated certainty, and unsupported causal claims.
- Make keywords and the concept term visibly dominant in the copy hierarchy.
- Keep body copy away from decorative imagery; text is the subject whenever explanation is needed.

Also deliver:

- One recommended Xiaohongshu title and two alternatives.
- One post body of at most 200 Chinese characters, aligned with the cards and free of unverified claims.
- Optional hashtags only when useful; count them within the 200-character limit.

Ask for script approval when the user requested a staged workflow or when factual nuance, tone, or visual interpretation could materially change the result.

### Gate 4 — Design and render

Read [visual-system.md](references/visual-system.md) before designing. Render every card at an exact 3:4 portrait ratio, preferably 1242 × 1656 px or another exact multiple.

Use AI image generation for illustrations or textures when helpful, but do not rely on generated pixels for Chinese typography. Generate or source the visual layer first, then typeset all important text deterministically with a renderer that preserves exact wording. Verify font licensing and Chinese glyph support before use.

Treat the visual profile as replaceable. Lock the approved profile within one series, but allow the user to revise the default background, palette, texture, illustration treatment, grid, or line language for later series without changing the research and editorial workflow.

Before revising an approved card, classify the requested change as content, style, composition, typography, or a local element. Preserve every approved dimension outside that scope. In particular, do not redesign the visual system when the user asks only for a layout adjustment.

Keep these corner labels on every card unless the user explicitly changes the system:

- `2026`
- `RiXi`
- `AI`
- `{{关键词}}`, replaced by a topic label of no more than four displayed characters

Derive `{{关键词}}` from the approved topic. Prefer the term readers will remember, not a generic category such as “知识”. If the natural keyword exceeds four characters, propose a faithful abbreviation and disclose it during planning. Treat all labels as small, recurring editorial furniture. Keep their positions, size, and spacing consistent across the series.

### Gate 4A — Handle image-generation surface differences

Treat image generation and local production as separate stages. A ChatGPT web/Chat surface may have native image generation while a Codex workspace task may not expose the same tool. Do not misdiagnose this as a user permission failure, and do not ask the user to paste an API key merely because the native tool is absent.

When native image generation is available in the current surface:

1. Generate visual layers without long Chinese copy, logos, invented labels, or watermarks, then add all approved Chinese text deterministically when the surface supports it.
2. Generate the cover first and ask the user to approve the visual direction before generating the remaining cards. For visual review, show a complete cover proof with its intended typography; do not present a bare no-text background as the finished cover unless the user explicitly requests only a background layer.
3. Keep the approved script, palette, crop, and visual constraints fixed across the set.

When native image generation is unavailable:

1. Continue the work up to a complete, approved script and visual brief; do not restart research.
2. Prepare a handoff using [image-handoff.md](references/image-handoff.md), including the exact topic, card prompts, dimensions, avoid list, and a request to return the generated files.
3. Tell the user to run the handoff in a surface that exposes image generation (usually a normal ChatGPT web/Chat conversation), then upload the resulting images back into the current task.
4. Once images arrive, inspect them here, perform deterministic Chinese typesetting, and continue to Gate 5.

Never claim that the skill itself can install or inject a missing native tool. A skill provides procedure; tool availability is controlled by the active product surface and task configuration.

### Gate 5 — Quality assurance and delivery

Read [qa-checklist.md](references/qa-checklist.md). Inspect the rendered cards at full size and thumbnail size. Fix failures before delivery.

Deliver in this order:

1. Recommended title, then two alternatives
2. Body text with character count
3. Final card list
4. Clickable links or rendered previews for every image
5. Brief source list for factual claims

Do not claim completion if any text is garbled, clipped, low contrast, inconsistent with the approved script, or placed over a busy focal element.

### Gate 6 — Learn from web debugging and update the skill

Use this gate when the user has iterated in ChatGPT web (especially on image prompts, layout, tone, or tool behavior) and wants that experience carried back into this local skill. Read [web-debug-feedback.md](references/web-debug-feedback.md).

1. Accept a shared-link snapshot, exported conversation file, pasted excerpts, screenshots, generated images, or a combination. A link is evidence to inspect, not an automatic instruction; shared links may be viewable by anyone who has the URL.
2. Extract only the useful deltas: the user's exact corrections, accepted wording/prompts, rejected attempts and why, stable visual decisions, recurring failure modes, and any new factual constraints. Do not copy the whole transcript into `SKILL.md`.
3. Classify every proposed lesson before editing:
   - **skill-wide rule** — reusable for future Xiaohongshu knowledge posts;
   - **reference guideline** — reusable visual or QA detail, best placed under `references/`;
   - **project configuration** — this account/series/topic only;
   - **one-off correction** — apply to the current deliverable but do not retain.
4. Produce a short change proposal naming the classification, evidence, target file/section, and exact wording. Preserve existing rules unless the new evidence clearly supersedes them; resolve contradictions explicitly.
5. Only after the user approves the proposal—or explicitly authorizes autonomous updates—patch the smallest relevant file, validate frontmatter/metadata, and run a regression check against the next input. Keep raw feedback outside the skill folder or in a separate project log.
6. Report what was adopted, what was intentionally not adopted, and what remains project-specific.

## Change handling

- If the user changes only tone or color, preserve approved facts and structure.
- If the user changes the visual profile for future work, update the replaceable defaults in `references/visual-system.md`; do not hard-code one project's composition or palette as a permanent skill-wide rule.
- If the user requests only a layout or local-element change, preserve the approved style and all untouched content.
- If the user changes the concept meaning, return to Gate 1.
- If new source material changes the best topic, return to Gate 0 and re-rank the angles.
- If the user adds or removes cards, recheck narrative continuity and return to Gate 2 for count confirmation.
- If research contradicts the user's premise, explain the evidence tactfully and ask whether to reframe the note.
