# 生图和编辑模板

每张独立调用 imagegen 内置工具，具体见 [生成入口](generation-model.md)。先观察原稿；必须传图片引用，不能把本地路径文字当作已附图。以下字段按任务填写，删除不适用字段。生成后必须执行 QA 视觉审核。

```text
Generate ONE standalone 16:9 horizontal Chinese article illustration.
Input image role: Cappy identity reference only. Invent a new scene; do not reproduce the reference sheet or its multi-view layout.

Visual DNA:
Pure #FFFFFF background, minimalist slightly wobbly black pen line art, generous empty white space. Sparse red/orange/blue handwritten Chinese annotations. No gradients, shadows, paper texture, UI, commercial vector polish, PPT layout, children's illustration or mascot poster.
Use ONE coherent contour style for Cappy, props and the scene: rounded black outlines matching the supplied original, with slight natural hand pressure variation and gentle drawing irregularity. Do not split a thick character from an ultra-fine scratchy environment. Text is different: light, natural Chinese handwritten annotations with varied glyph proportions and baselines, not heavy printed headings or bubble lettering. Keep visible limb and contact contours clear; stop hidden contours at the occluding form.

Recurring character:
Cappy is the white keycap character in the reference. The keycap shell IS its entire body: a rounded trapezoid narrower on top and wider at the base. A black-outlined white oval face panel on the front contains two thick black vertical eyes and a small w-shaped mouth; simple expression variations are allowed. Short white mitten hands grow from the sides, two short flat oval feet below. Three-quarter views show the top plane and one side plane. Preserve its compact proportions and original rounded hand-drawn contour language, shared with the props and scene. No separate head, long legs, solid-black body, white dot eyes, black face screen, cat ears or costume. Keep its natural friendliness without turning the composition into a cute poster. Cappy performs the core action.

Theme: {主题}
Structure: {8 种结构之一，不写进图里}
Core idea: {一句话}
Scene: {Cappy 的具体动作、主物件、输入输出或状态变化}
Physical action and anatomy: {逐个角色写操作手的壳体侧面连接、掌面朝向与接触点，另一手的放松或辅助姿态，两脚支撑与具体遮挡者。Use the ORIGINAL compact rounded mitten shape: fingers grouped as one mass, a small thumb notch only where needed, no row of knuckles. Keep the prop within short-hand reach and sized for the palm; move the body or prop instead of stretching an arm or twisting a wrist. Both hands and feet are structurally accounted for, but need not all be fully visible. Use clear overlapping contours for grip and occlusion, never a prop line through the palm. The free hand may rest naturally.}
Exact Chinese labels: {逐字列出；通常 3–5 处，最多 5–8 处，每处 2–8 字}
Color: Black line art and main text, WHITE Cappy shell and face. Orange only for main flow/path/arrows; red only for warnings/emphasis/results; blue only for secondary notes/feedback/system state. Color is optional, sparse, and never fills Cappy.

Constraints:
One core idea. Main illustrated group about 40–60% of canvas; at least 35% blank white space. No title in the top-left, no structure-type heading, dense explanatory copy, formal diagram or excessive arrows. Fresh physical metaphor, not a copied example. Reference images supply character identity only.
```

## 去标题

传目标图并标记为编辑对象；如需额外原稿参考，说明其用途。

```text
Edit image 1, the target illustration. Remove only the handwritten title "{逐字标题}" and its underline in the top-left. Restore pure white background there. Preserve everything else: Cappy's white trapezoid body, oval face, eyes, hands and feet, all remaining labels, props, paths, pen style, colors, aspect ratio and composition. Add no text or objects. If image 2 is supplied, it is identity reference only, not another edit target.
```

## 改文字或角色

```text
Edit image 1. Change only {精确区域和变化}. Preserve {其余文字、角色、物件、结构、颜色和比例}. Render exact replacement text "{文字}". Keep a pure white background and hand-drawn lines. Image 2, if supplied, is Cappy identity reference only.
```

角色替换时写清楚“只将目标角色替换成参考中的白色 Cappy 键帽；接手同一个核心动作”，不要把目标图中的黑色身体/白点眼继续保留。

## 加强隐喻与减法

太普通时重新生成同一核心意思，换一个具体物理动作或主物件；让 Cappy 真正执行，保持身份参考和留白。太拥挤时删掉次要物件与标注，只保留一个动作和 3–5 个短词。不要以“更怪诞”为由扭曲键帽壳。
