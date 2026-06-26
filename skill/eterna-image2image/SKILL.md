---
name: eterna-image2image
description: Apply a professional Fujifilm ETERNA-inspired cinema color and composition treatment to generated or edited raster images. Use when the user asks for ETERNA, Fujifilm ETERNA, ETERNA/CINEMA, ETERNA Bleach Bypass, muted cinema stills, filmic image-to-image color grading, cinematic composition, anti-AI image polish, movie screenshots, war/drama/romance/editorial frames, or restrained film color. 适用于用户要求富士 ETERNA、电影感图生图、电影截图、降低 AI 味、低饱和电影调色、电影构图、战争/爱情/剧情/时装片质感等场景。
---

# ETERNA Image2Image / ETERNA 图生图电影化处理

## Core Behavior / 核心行为

Use this skill to turn a source image or new image prompt into a professional ETERNA-inspired cinema still. Treat ETERNA as a restrained motion-picture color and tone language, not a generic retro filter.

使用这个 skill 时，要把源图或新图提示词引导成 ETERNA 启发的专业电影截图。把 ETERNA 理解为克制的电影色彩、影调和质感系统，而不是普通复古滤镜。

If raster image generation or editing is needed, use the normal image generation workflow available in the current environment. For an existing image, preserve subject identity, composition intent, perspective, and scene lighting unless the user explicitly asks for creative changes. For no input image, generate a new cinema still with the same color discipline.

如果需要生成或编辑位图，使用当前环境中的图像生成工作流。处理已有图片时，默认保留主体身份、构图意图、透视关系和场景光线；除非用户明确要求重写画面。没有输入图时，也要用同样的色彩纪律生成新的电影截图。

This is an experimental, evolving skill. Prefer practical, testable prompt language over claims of exact Fujifilm color science. Do not claim official LUT accuracy unless the user provides a licensed official workflow and source color-space details.

这是一个持续迭代的实验性 skill。优先使用可测试、可复现的提示词和质量检查，而不要声称精确复刻 Fujifilm 官方色彩科学。除非用户提供授权的官方流程和源色彩空间信息，否则不要承诺官方 LUT 级匹配。

## Look Selection / 风格模式

Choose one mode:

- `standard-eterna`: default. Muted color, low-to-medium contrast, rich detailed shadows, soft highlight roll-off, natural skin.
- `clean-cinema-eterna`: slightly cleaner, less grain, production still or streaming-drama finish.
- `eterna-bleach-bypass`: only when requested or strongly implied. Lower saturation, higher contrast, colder metallic feel, deeper blacks.

选择一种模式：

- `standard-eterna`：默认模式。低饱和、低到中等反差、暗部丰富但可读、高光柔和、肤色自然。
- `clean-cinema-eterna`：更干净、颗粒更少，适合剧照、现代剧集或商业片质感。
- `eterna-bleach-bypass`：只在用户明确要求或强烈暗示时使用。更低饱和、更高反差、更冷的金属感、更深的黑位。

Do not mix ETERNA Bleach Bypass into the default look.

默认不要把 ETERNA Bleach Bypass 混入标准 ETERNA。

## Prompt Recipe / 提示词配方

Start from the user's subject and add this color-grading block:

```text
Apply a professional Fujifilm ETERNA-inspired cinema grade: muted color, low-to-medium contrast,
soft highlight roll-off, rich but detailed shadows, natural warm skin tones, restrained olive/sage greens,
subdued steel blues, neutral-warm highlights, gentle filmic grain, natural soft sharpness, Rec.709/sRGB finish.
Preserve realistic lighting and texture. Avoid HDR, neon saturation, crushed blacks, clipped highlights,
orange-teal blockbuster grading, plastic skin, heavy halation, fake scratches, watermarks, and text.
```

中文提示词块：

```text
应用专业的 Fujifilm ETERNA 启发电影调色：低饱和、低到中等反差、
柔和高光过渡、丰富但可读的暗部、自然偏暖肤色、克制的橄榄绿/鼠尾草绿、
低调钢蓝色、中性偏暖高光、轻微电影颗粒、自然柔和锐度、Rec.709/sRGB 输出。
保留真实光线和材质。避免 HDR、霓虹饱和、死黑、过曝高光、
商业大片式橙青调色、塑料皮肤、重度光晕、假划痕、水印和文字。
```

For `eterna-bleach-bypass`, replace the first sentence with:

```text
Apply an ETERNA Bleach Bypass-inspired cinema grade: very low saturation, higher contrast,
cool metallic shadows, restrained warm highlights, hard but controlled drama, deep blacks with recoverable detail.
```

中文：

```text
应用 ETERNA Bleach Bypass 启发的电影调色：极低饱和、更高反差、
冷金属暗部、克制暖高光、强硬但受控的戏剧感、深黑但保留可恢复细节。
```

## Composition Guidance / 构图指导

Use `references/composition-guide.md` when the task needs cinematic framing, scene blocking, lens language, lighting motivation, or anti-AI composition polish.

当任务需要电影构图、调度、镜头语言、动机光或降低 AI 味时，读取 `references/composition-guide.md`。

Default composition preferences:

- Favor story-driven framing over centered passport/photo-card composition.
- Use foreground, midground, and background separation when the scene allows it.
- Preserve identity references, but adapt pose and blocking into a believable film moment.
- Use motivated light sources such as windows, street lamps, practical lamps, firelight, or overcast sky.
- Leave controlled negative space when it adds tension, intimacy, loneliness, or scale.
- Avoid over-clean symmetry, generic poster composition, floating props, impossible reflections, and text artifacts.

默认构图偏好：

- 优先让画面像叙事中的一帧，而不是居中的证件照或人设卡。
- 场景允许时，使用前景、中景、背景层次。
- 保留参考人物/主体身份，但把姿态和调度转化为可信的电影瞬间。
- 使用有动机的光源，例如窗光、路灯、实景台灯、火光或阴天自然光。
- 在紧张、亲密、孤独或表现空间尺度时保留有控制的负空间。
- 避免过度干净的对称、泛化海报构图、悬浮道具、不可能反射和文字伪影。

## Color And Tone Rules / 色彩与影调规则

Use `references/eterna-color-spec.md` when the task needs exact palette guidance, negative constraints, scene defaults, or quality checks.

当任务需要具体色盘、负向约束、场景默认色彩或质量检查时，读取 `references/eterna-color-spec.md`。

Use `references/lut-workflow.md` only when the user asks for LUTs, exact Fujifilm matching, color-managed workflows, or how to compare output against official resources.

只有当用户询问 LUT、精确 Fujifilm 匹配、色彩管理流程或如何与官方资源比较时，才读取 `references/lut-workflow.md`。

## Quality Check / 质量检查

Before finishing, check:

- Skin stays natural, not orange, gray, waxy, or over-smoothed.
- Greens are olive/sage, not neon or emerald.
- Blues are steel/gray-blue, not electric cyan.
- Blacks are deep but readable; highlights are soft and not clipped.
- Grain is subtle and image texture stays photographic.
- The frame reads as a plausible cinema still, not a social-media preset or AI promo image.
- Composition supports story, mood, and spatial logic.

完成前检查：

- 肤色自然，不橙、不灰、不蜡、不磨皮过度。
- 绿色偏橄榄/鼠尾草，不霓虹、不祖母绿。
- 蓝色偏钢蓝/灰蓝，不电光青。
- 黑位深但可读；高光柔和且不过曝死白。
- 颗粒轻微，整体质感仍像摄影。
- 画面像可信的电影截图，而不是社交媒体滤镜或 AI 宣传图。
- 构图服务于故事、情绪和空间逻辑。

