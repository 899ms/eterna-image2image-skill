# ETERNA Color Specification / ETERNA 色彩规格

This is a practical image-generation specification inspired by Fujifilm ETERNA/CINEMA. It is not a claim to reproduce Fujifilm's proprietary color science exactly.

这是一份面向图像生成的实用 ETERNA/CINEMA 启发色彩规格。它不是对 Fujifilm 专有色彩科学的精确复刻声明。

## Target Output / 目标输出

- Color space: Rec.709 / sRGB display rendering.
- White balance: neutral to subtly warm highlights; avoid extreme teal-orange split toning.
- Contrast: low-to-medium for standard ETERNA; higher only for Bleach Bypass.
- Saturation: restrained, usually 65-80 percent of a normal digital photo.
- Texture: gentle filmic grain and natural optical softness; no fake damage by default.

- 色彩空间：Rec.709 / sRGB 显示输出。
- 白平衡：高光中性到轻微偏暖；避免极端橙青分离调色。
- 反差：标准 ETERNA 为低到中等；只有 Bleach Bypass 才提高反差。
- 饱和度：克制，通常约为普通数码照片的 65-80%。
- 质感：轻微电影颗粒和自然光学柔和；默认不要假划痕、灰尘或胶片损坏。

## Hue Tendencies / 色相倾向

- Shadows: charcoal, cool gray-green, or soft blue-gray.
- Highlights: neutral cream, pale straw, or gentle warm skin highlights.
- Greens: olive, sage, lichen, military fabric green; avoid neon grass or emerald.
- Blues: steel blue, smoke blue, gray cyan; avoid electric cyan.
- Reds: muted brick, dried blood red, dark oxide; avoid lipstick red unless source requires it.
- Yellows: straw, aged brass, muted sodium vapor; avoid lemon yellow.

- 暗部：炭黑、冷灰绿、柔和蓝灰。
- 高光：中性奶油色、浅稻草色、轻微偏暖肤色高光。
- 绿色：橄榄、鼠尾草、地衣、军布绿；避免霓虹草绿或祖母绿。
- 蓝色：钢蓝、烟蓝、灰青；避免电光青。
- 红色：低饱和砖红、干血红、暗氧化红；除非源图需要，否则避免口红红。
- 黄色：稻草色、旧黄铜、低饱和钠灯黄；避免柠檬黄。

## Working Palette / 工作色盘

Use these as prompt anchors, UI swatches, or QA references. They are approximate working colors, not official Fujifilm values.

这些颜色可作为提示词锚点、UI 色块或质量检查参考。它们是近似工作色，不是 Fujifilm 官方数值。

| Role / 角色 | Hex |
| --- | --- |
| Deep green-black / 深绿黑 | `#151817` |
| Cinema charcoal / 电影炭灰 | `#252827` |
| Cool gray shadow / 冷灰暗部 | `#3F4948` |
| Steel blue-gray / 钢蓝灰 | `#5F7478` |
| Sage green / 鼠尾草绿 | `#7B887A` |
| Olive green / 橄榄绿 | `#646B4F` |
| Muted dark khaki / 低饱和深卡其 | `#8A7D58` |
| Dark straw gold / 深稻草金 | `#B59A67` |
| Warm skin midtone / 暖肤色中间调 | `#C89572` |
| Pale skin highlight / 浅肤色高光 | `#D7B49A` |
| Muted brick red / 低饱和砖红 | `#9B5E4E` |
| Cream highlight / 奶油高光 | `#D8D0BB` |
| Fog white / 雾白 | `#E2E0D4` |

## Negative Constraints / 负向约束

Avoid:

- HDR microcontrast and hyperreal clarity.
- Neon signs or saturated primaries unless explicitly part of the scene.
- Crushed black silhouettes with no recoverable detail.
- Clipped white skies, lamps, or explosions.
- Heavy orange-teal blockbuster grading.
- Brown-only sepia, Instagram vintage, fake scratches, dust overlays, or projector damage unless requested.
- Plastic skin, excessive beauty smoothing, extra-sharp eyelashes, or synthetic cloth texture.

避免：

- HDR 微反差和过度真实锐化。
- 除非场景明确需要，否则避免霓虹灯和高饱和原色。
- 没有细节的死黑剪影。
- 过曝死白的天空、灯光或爆炸。
- 过重的商业大片橙青调色。
- 单一棕褐复古、Instagram 复古、假划痕、灰尘叠层或放映机损坏感，除非用户明确要求。
- 塑料皮肤、过度美颜、过锐睫毛或合成感布料。

## Scene Defaults / 场景默认值

### War / Drama

- Prefer overcast daylight, smoke-diffused sun, dawn, dusk, or practical firelight.
- Keep uniforms, helmets, mud, canvas, and metal muted and tactile.
- Show tension through composition and light, not gore.
- Use wide cinematic aspect ratios such as 2.39:1 or 16:9 when possible.

### Romance / Interior Drama

- Keep skin natural and softly dimensional, not glossy.
- Use warm practical lamps, window spill, curtain diffusion, or dim hotel/apartment light.
- Keep reds and pinks muted; favor cream, straw, brick, wine, sage, and soft shadow blue.
- Let intimacy come from blocking, gaze, hand placement, distance, and negative space rather than explicitness.

### Night Exterior

- Use one or two motivated light sources: street lamp, shop spill, taxi light, moonlight, or sodium vapor.
- Preserve deep shadows with readable contour detail.
- Allow blue-gray shadows and muted sodium highlights, but avoid neon cyberpunk unless requested.
- Wet pavement, glass, and metal should reflect softly, not like HDR mirrors.

### Editorial / Character Reference Adaptation

- Preserve core identity markers: face shape, hair, clothing language, posture, accessories.
- Convert reference-card poses into believable film blocking.
- Avoid clean studio white backgrounds unless the user asks for reference-sheet output.

