---
name: ian-xiaohei-illustrations
description: 为中文文章设计并生成白底手绘正文配图，默认使用用户的绿衬衫青年男性 IP。适用于文章插图、配图规划、shot list、观点隐喻及已有配图修改。
---

# 个人 IP 手绘正文配图

为中文文章的关键判断、流程、结构、状态或隐喻生成 16:9 横版手绘解释图。保留 Ian 原项目的白底、留白、简洁结构与原创隐喻方法，默认人物已替换为用户自己的绿衬衫青年，不再生成小黑。

保留技术调用名 `$ian-xiaohei-illustrations`，以兼容已有安装；该名称不代表当前角色仍为小黑。项目来源见仓库的 NOTICE.md。

## 参考与优先级

1. 读取 `references/character-ip.md`，并查看 `assets/character/green-youth-reference.png`；角色外形以该图和角色定义为准。支持图像参考时将基准图传给生图工具，不只在 prompt 里写文件路径。
2. 读取 `references/style-dna.md`，确定整体画风、配色和文字密度。
3. 按任务读取 `references/composition-patterns.md` 与 `references/prompt-template.md`，生成后读取 `references/qa-checklist.md`。
4. 需要动作或画面校准时，读取 `references/scene-examples.md`，从 `assets/scene-examples/` 按需选一张；不要一次载入整组，不复制样片隐喻或构图。

`assets/examples/` 全部为原项目小黑的历史素材，默认不打开、不作为角色参考或图像输入；仅在用户明确要求研究旧画风时使用，并忽略其中人物外形。`references/xiaohei-ip.md` 仅是旧路径兼容说明。

## 工作流

### 理解正文与规划

读取正文、链接、Markdown 或截图，提炼观点和认知转折；优先给关键判断、输入输出、前后对比、常见坑或状态变化配图，不平均分配。

用户只要求分析时输出 shot list：放置位置、主题、核心意思、结构类型、青年角色承担的动作、建议物件和短中文标注。通常 4–8 张，短文 1–3 张，长文也避免轻易超过 9 张。

### 单张生成

用户明确要求生成时使用可用的内置 `image_gen`，每张单独生成，不拼成一张。根据角色定义与正文重新发明具体动作和隐喻，不复刻历史案例。

每张 prompt 使用 `references/prompt-template.md`，包含 16:9、纯白背景、简练黑色手绘线条、大量留白、克制的彩色批注以及绿衬衫青年参与核心动作。外形完整定义集中在 `references/character-ip.md`；不另行编造人设或重复定义冲突的服装。

咖啡杯可省略，耳机默认不戴。根据动作改变姿态、手势和表情，不把参考图的持杯站姿当成固定构图。让青年操作怪装置，而不是让人体变成装置。

### 检查与迭代

按 `references/qa-checklist.md` 检查角色一致性、动作参与度、留白、中文可读性和原创性。出现旧小黑、人物像装饰、画面过密、PPT 感、精细日漫化、服装标识或错误中文时，针对问题局部编辑或重生成。没有实际生图时，不宣称已验证角色生成稳定性。

### 保存交付

在 workspace 中工作时，将最终图复制到 `assets/<article-slug>-illustrations/`，按 `01-topic-name.png` 顺序命名。保留原始生成文件，不覆盖已有资产，除非用户明确要求替换。交付说明张数、用途和路径；策略和解释保持简洁。
