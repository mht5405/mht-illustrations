# 生图提示词模板

先读取 `character-ip.md` 并查看角色基准图；支持参考输入时将 `assets/character/green-youth-reference.png` 作为角色参考实际传入。每张图单独生成。将以下角色段与变量展开为完整 prompt，不要仅向模型传文件路径。

```text
Generate one standalone 16:9 horizontal Chinese article illustration.

Visual DNA:
Pure white background, sparse slightly wobbly black hand-drawn pen contours, large white negative space, restrained flat character colors, a few short Chinese handwritten annotations. Simple lively editorial drawing with an inventive physical metaphor. Not a polished anime portrait, fashion poster, corporate mascot, PPT infographic or formal diagram. No gradients, paper texture, realistic UI or complex backdrop.

Recurring personal IP:
Use the provided green-youth reference image for character identity and palette only, not its pose or composition. A young ADULT man with slightly tousled black short hair and one small bent upward tuft, simple small black eyes, a short nose stroke and a small expressive mouth. Slightly enlarged head but adult proportions, approachable, curious and ready to act. Muted jade-green open overshirt with rolled sleeves, completely plain white T-shirt, charcoal-black above-knee casual shorts, white athletic socks and off-white sporty shoes with tiny pale warm-yellow accents. Use economical slightly wobbly lines for BOTH character and objects. Render hair as a few silhouette masses, folds as a few essential strokes and shoes as plain sporty contours without individual laces; no portrait-like facial shading. No clothing emblem, water-ripple symbol, logos, glasses or headphones by default. Keep him human; do not transform his body into machinery or a black creature. Vary expression, angle and pose to support the idea. A warm terracotta coffee cup with white lid is optional; omit it whenever the action needs free hands.

Theme: {正文配图主题}
Structure type for planning only: {流程 / 系统局部 / 前后对比 / 角色状态 / 概念隐喻 / 方法分层 / 地图路线 / 小漫画}
Core idea: {这张图表达的一个核心意思}
Composition: {青年角色在哪里、具体做什么、主要物件、信息或物件如何流动；不要固定为持杯插兜}
Suggested elements: {选择少量物件}
Chinese handwritten labels: {最多5至8处短标注}

Color use:
Keep the character's reference palette. Mostly black linework for scene objects, sparse orange for main paths, red for key problems/results and optional blue for feedback. Clothing and optional coffee colors are identity/prop colors, not diagram semantics.

Constraints:
The character performs the core conceptual action, not merely watches from a corner. For mechanism illustrations the mechanism/action/result is the primary visual focus, with the identifiable character scaled to serve it. In wide multi-person scenes start with figures about 25–40% of canvas height and adjust for readability; enlarge when character state is the subject. Keep hands contacting the operated object and feet visibly supported. Gaze follows the task; restrained facial emotion, no irrelevant upward smile or theatrical grimace. One image explains one core idea. Main subjects occupy about 40–60% of the canvas; preserve at least 35% white space. No top-left title and no structure-type label. Invent a fresh metaphor for this article; do not copy historical examples. Keep personality youthful and quietly humorous without babyish cuteness or rigid deadpan expression.
```

无参考图输入能力时，将“Use the provided ...”一句改为明确的文字角色描述，保留其他身份约束；不要声称模型已收到图像。

## 编辑提示

去标题：只移除指定文字与下划线，填回纯白；保留人物身份、服装配色、其他标注、构图及比例。

增强参与感：保持当前角色身份与核心意思，重新设计一个由青年亲手推动的物理动作；需要时移走咖啡杯，避免人物只站在图旁。保持留白和简练线条。

修正漂移：以角色基准图恢复黑色短发与弯曲翘发、玉绿衬衫、纯白 T、黑短裤和运动鞋；简化过细的五官与服装，不改动其他已正确的场景部分。

## 首轮样片后的修正

需要更简练时补充：场景道具用白色未填充区域和黑色轮廓，不画金属灰渐变；皮肤与衣服使用平涂，五官、衣褶和鞋带继续概括。多格画面补充：同一物件在各格保持轮子数量、轮廓和零件一致；镜头变化不能擅自改造物件。必要时按格局部编辑，不用连续多次整图重试来掩盖问题。
