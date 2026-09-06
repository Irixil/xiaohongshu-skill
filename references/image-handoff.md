# Image-generation handoff

Use this handoff when the current Codex task cannot access native image generation but the user can generate images in a ChatGPT web/Chat conversation.

## Handoff rules

- Carry over the approved topic and script; do not reselect the topic.
- Generate each finished card with all approved Chinese copy already integrated into the image. Do not generate a blank template for later typesetting.
- Generate exact 3:4 portrait images, preferably 1242 × 1656 px.
- Generate the cover first. Present a complete cover proof with the intended title and hierarchy for visual approval; do not call a bare background the cover unless the user requested only that layer.
- Use the default tactile owl editorial-collage profile from `visual-system.md` unless the project names another approved profile.
- Keep each card's focal visual distinct while preserving the warm coarse-fiber paper, torn collage, wine-red handwritten title, blue-pen annotations, muted paper palette, natural shadows, recurring owl, grid logic, and corner furniture.
- Generate one card per request. If any required text is wrong, regenerate that card with the correct string and preserve the accepted composition and style; do not repair it by adding a text layer.
- Return files in reading order with zero-padded names, e.g. `01-cover.png` through `07-takeaway.png`.

## Copy-paste handoff template

```text
请完整阅读我上传的交接文件和视觉参考图。不要重新选题，不要改动已确认的逐页脚本。一次只生成一张成品图。先制作第1张封面的完整视觉样稿，精确3:4竖版（推荐1242×1656；1086×1448也可），让用户能够同时判断构图、标题层级、角色、纸张质感和整体风格。未经确认不要继续其余图片。

目标受众：对AI感兴趣但缺少基础知识的小白。
视觉：若本期没有另行指定，严格使用默认的温暖手工编辑拼贴：粗纤维米白旧纸、撕边纸片、真实办公物件和自然投影、深酒红粗粝手写标题、深蓝钢笔批注与箭头、橄榄绿/浅蓝/沙褐纸卡；使用拟人棕色猫头鹰作为统一角色，穿军绿色工作外套、系红围巾。真实摄影拼贴与手绘标注融合，克制、有触感、有编辑感。
硬性约束：每张卡的全部指定中文必须在生图时直接成为画面的一部分，文字、纸片、角色、插图与阴影一次生成。不得先生成空白模板再后期压字，不得用覆盖文字修补错字。不要添加提示词之外的可读标签、Logo或水印。避免扁平矢量、赛博朋克、霓虹、发光机器人、复杂UI、光滑塑料3D和图库广告感。

把每张卡的全部文字逐条、逐字写进提示词，并要求原样生成。生成后立即逐字核对标题、正文、角标、数字、顺序和标点；有一处错误就只重生这一张，保持已经通过的画面不变。
```

## Return package

Ask the user to bring back:

1. The generated PNG/JPG files.
2. The final prompt or prompt revision that produced them.
3. Any visual feedback, rejected variants, or approved cover reference.
4. The approved text and the complete finished card images.

After return, compare each image against the approved card role and exact copy. Preserve accepted files. Return card-specific regeneration prompts for failures instead of applying typography overlays.
