# LUT Workflow Notes / LUT 工作流说明

Fujifilm publishes official 3D LUT packages for several camera/log workflows. Use them as external references only; do not bundle official LUT files inside this skill unless the user provides licensed files for their own workspace.

Fujifilm 为若干摄影机/log 工作流发布过官方 3D LUT。这里只能把它们作为外部参考；除非用户为自己的工作区提供了授权文件，否则不要在本 skill 中捆绑官方 LUT。

## Practical Guidance / 实用指南

- For exact matching, ask what source color space/log curve the input represents.
- Use official Fujifilm LUTs only when the user's footage/image is in the matching input transform, such as F-Log, F-Log2, or F-Log2C.
- Official LUT output is intended for a BT.709/Rec.709 style deliverable.
- For ordinary generated or web images, use prompt-based ETERNA guidance rather than applying a camera-log LUT blindly.

- 如果用户要求精确匹配，先确认输入素材的色彩空间和 log 曲线。
- 只有当用户图像/素材处于匹配输入变换时，才使用对应官方 Fujifilm LUT，例如 F-Log、F-Log2 或 F-Log2C。
- 官方 LUT 输出通常面向 BT.709/Rec.709 交付。
- 对普通生成图或网页图片，使用提示词层面的 ETERNA 指导，不要盲目套用摄影机 log LUT。

## Matching Levels / 匹配等级

- `inspired`: prompt-only look, suitable for image generation.
- `reference-grade`: compare output visually against ETERNA-like stills or official examples.
- `color-managed`: user supplies source image, input transform, and official LUT or grading target.

- `inspired`：仅提示词级的启发式风格，适合图像生成。
- `reference-grade`：与 ETERNA 类似剧照或官方示例做视觉对比。
- `color-managed`：用户提供源图、输入变换和官方 LUT 或调色目标。

