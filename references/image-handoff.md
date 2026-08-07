# Image-generation handoff

Use this handoff when the current Codex task cannot access native image generation but the user can generate images in a ChatGPT web/Chat conversation.

## Handoff rules

- Carry over the approved topic and script; do not reselect the topic.
- Generate the visual layer separately from final long-form Chinese typesetting.
- Generate exact 3:4 portrait images, preferably 1242 × 1656 px.
- Generate the cover first. Present a complete cover proof with the intended title and hierarchy for visual approval; do not call a bare background the cover unless the user requested only that layer.
- If exact local typesetting is temporarily unavailable, clearly label model-rendered text as a composition prototype and return the background layer for later deterministic typesetting.
- Keep each card's focal visual distinct while preserving paper texture, grid logic, illustration treatment, and color family.
- Return files in reading order with zero-padded names, e.g. `01-cover.png` through `07-takeaway.png`.

## Copy-paste handoff template

```text
请完整阅读我上传的交接文件和视觉参考图。不要重新选题，不要改动已确认的逐页脚本。先制作第1张封面的完整视觉样稿，精确3:4竖版（推荐1242×1656），让用户能够同时判断构图、标题层级、留白和整体风格。未经确认不要继续其余图片。

目标受众：对AI感兴趣但缺少基础知识的小白。
视觉：严格使用交接文件中本期已确认的视觉预设；如果未指定，则使用干净白底、墨黑输入、深蓝结果、少量警示橙、克制留白与轻微印刷颗粒。该预设可由用户在后续项目中更换。
硬性约束：画面必须为文字排版预留干净安全区；不要把插画放在计划文字的位置；避免赛博朋克、霓虹、发光机器人、复杂UI、图库广告感。

不要让图像模型承担长中文段落的最终排版。若当前环境能进行确定性中文排版，请在视觉底图上加入确认后的原文再展示完整样稿；若不能，请同时返回构图样稿和无文字底图，并明确说明中文仍需后期逐字排版。
```

## Return package

Ask the user to bring back:

1. The generated PNG/JPG files.
2. The final prompt or prompt revision that produced them.
3. Any visual feedback, rejected variants, or approved cover reference.
4. The approved text and, when available, both the clean visual layer and the complete typeset proof.

After return, compare each image against the approved card role before typesetting. Preserve the image file; make compositing and typography edits as new versions.
