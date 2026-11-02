# MHT Illustrations · 个人 IP 手绘正文配图

MHT Illustrations 是 mht5405 的个人 IP 配图 Skill，基于 Ian Xiaohei Illustrations 修改。将中文文章里的关键判断、流程、状态和隐喻变成白底、简练手绘的 16:9 正文配图，默认人物已替换为用户自己的绿衬衫青年男性 IP。

## 当前角色

![绿衬衫青年基准图](ian-xiaohei-illustrations/assets/character/green-youth-reference.png)

选择新版简化造型作为默认基准：相比上一版修长的时装插画，五官更概括、轮廓更容易缩小识别，也更适合不同动作的正文场景。绿衬衫、纯白 T、黑短裤和运动鞋是固定服装；黑短发及弯曲翘发是识别点。没有水纹标志，默认不戴耳机。咖啡杯为可选道具，动作需要双手时省略。姿态、表情和视角随文章变化，不固定为持杯站立。

保持原项目的纯白背景、大量留白、黑色手绘线条和原创物理隐喻，允许角色使用绿白黑平涂色。角色是自然、有朝气的成年人，不沿用小黑的全黑身体、白点眼及变形设定。

## 个人 IP 场景样片

另补充一张与小黑对比后优化的机制型样片：人物缩小、线条概括，强化握绳与踩板，让裂缝和货物先进入视线。绿色穿搭与发型识别点保留。这类主次调节用于机制图，不强制用于人物状态图。

![机制型配图优化样片](ian-xiaohei-illustrations/assets/scene-examples/07-mutual-cost-refined.png)

下方为此前六张首轮样片，保留用于观察动作与已知问题。

已实际生成六张首轮样片，覆盖八类构图，检验跪姿、站姿、坐姿、侧背视角、行走及连续分镜。人物基准图约束身份，场景样片校准动作与画面密度，不作为固定构图模板。优先参考“按用途筛选”和“把方法搭起来”的简洁程度；管道与连续小车仍有细节可压简，不能将此组视为所有场景均稳定的保证。

**修补信息断点**（系统局部、概念隐喻）

![修补信息断点](ian-xiaohei-illustrations/assets/scene-examples/01-repair-handoff.png)

**按用途筛选**（流程）

![按用途筛选](ian-xiaohei-illustrations/assets/scene-examples/02-sort-by-purpose.png)

**从忙乱到理顺**（前后对比、角色状态）

![从忙乱到理顺](ian-xiaohei-illustrations/assets/scene-examples/03-before-after.png)

**把方法搭起来**（方法分层）

![把方法搭起来](ian-xiaohei-illustrations/assets/scene-examples/04-build-method.png)

**边走边调整**（地图路线、概念隐喻）

![边走边调整](ian-xiaohei-illustrations/assets/scene-examples/05-explore-route.png)

**试一下再修改**（小漫画分镜、角色状态）

![试一下再修改](ian-xiaohei-illustrations/assets/scene-examples/06-test-and-adjust.png)

完整[场景索引与检查说明](ian-xiaohei-illustrations/references/scene-examples.md)、[生成提示词](examples/personal-ip-generation.json)和[检查记录](examples/personal-ip-review.json)均已保存。

## 安装与使用

```bash
git clone https://github.com/mht5405/mht-illustrations.git
cd mht-illustrations
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

GitHub 仓库名称为 `mht-illustrations`；仓库内的 Skill 子目录与调用名仍保留 `ian-xiaohei-illustrations`，兼容现有安装。显示名称为“个人 IP 手绘配图”，默认角色为 MHT 的绿衬衫青年。

```text
Use $ian-xiaohei-illustrations 为这篇文章设计并生成 4 张正文配图。
使用我的绿衬衫青年 IP，每张图让角色参与核心动作，保持白底、简练手绘和留白。
```

仅需规划时加“先不要生图，输出 shot list”。更多调用示例见 [examples/prompts.md](examples/prompts.md)。最终图保存到 workspace 的 `assets/<article-slug>-illustrations/`，每张独立生成，保留原始文件。

## 维护位置

- `ian-xiaohei-illustrations/SKILL.md`：执行入口和工作流。
- `references/character-ip.md`：角色定义的唯一正文来源（位于 Skill 内）。
- `assets/character/green-youth-reference.png`：默认角色视觉基准（位于 Skill 内）。
- `references/style-dna.md`：画风、色彩与留白。
- `references/prompt-template.md`：生图及编辑模板。
- `references/composition-patterns.md`：构图、动作和原创隐喻。
- `references/qa-checklist.md`：角色一致性与画面检查。
- `agents/openai.yaml`：展示名称及默认提示。

原来的 `references/xiaohei-ip.md` 保留为兼容说明，不再定义角色。根目录 `examples/images/` 与 Skill 的 `assets/examples/` 保留原作者历史小黑示例；默认不读取、不传给图像模型，仅在明确研究原画风时参考线条和留白，不能作为当前角色参考。当前形象仅以本页基准图为准。

## 来源

原始 Skill 由 [Ian](https://github.com/helloianneo) 创建，源项目为 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)。本分支替换个人 IP 和相关生成规则，保留原项目归属说明与历史素材。见 [NOTICE.md](NOTICE.md) 与 [LICENSE](LICENSE)。
