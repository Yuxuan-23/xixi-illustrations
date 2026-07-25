# 西西 × 小光手绘讲解图

> 把中文内容里的判断、流程、关系和方法，变成西西与小光共同参与的温柔水彩讲解图。
>
> 成熟西西 / 可选 Q 版西西 | 4:5 知识卡片或 16:9 正文配图 | 暖米白水彩 | 雾蓝 × 金黄 | Codex Skill

## 这是什么

这是一个 Codex Skill，用于为中文文章、帖子、博客、知识卡片和方法论内容设计、规划和生成手绘讲解图。

它的重点不是做人物肖像，也不是把文字塞进 PPT。每张图先找到一个要解释的认知锚点，再让西西和小光共同参与一个更大的讲解对象：西西观察、书写、整理或操作；小光通过光轨照亮关系、串联节点或引导方向。

西西的面貌与头发以 [相貌参考图](xixi-xiaoguang-illustrations/assets/xixi-face-reference.png) 为准。技能不再使用“一张主参考图套所有内容”的方式，而是从已有成熟样图中按主题选一种构图模式：

- 分析讲解卡：西西 + 分析板，适合拆问题。
- 系统流程页：信息分区 + 小光路径，适合多步方法。
- 旅程隐喻图：大物件/两端场景 + 路线，适合变化过程。
- 判断关系卡：证据/观察卡 + 关系链路，适合认知判断。

详细映射见 [画面模式说明](xixi-xiaoguang-illustrations/references/modes.md)，角色不可漂移元素见 [角色锚点](xixi-xiaoguang-illustrations/references/character.md)。

## 产出

- 一篇内容的 4-8 张 shot list。
- 每张图的主题、核心意思、画面模式、西西与小光的动作和短标注建议。
- 单张或多张 PNG 手绘讲解图，默认保存至 `assets/<article-slug>-illustrations/`。

默认不输出 PPTX、SVG、HTML/Canvas 可编辑图或长段文字信息图。

## 视觉规则

- 暖米白水彩纸感，细铅笔/墨线与柔和水彩结合。
- 西西保留大波浪黑长卷发、珍珠发夹、珍珠耳饰和雾蓝职业服装；默认成熟西西版，用户指定时可转为 Q 版。
- 小光是鲜明的金黄色光之伙伴，光尾承担路径、连接或重点提示作用。
- 人物比例、文字密度和讲解对象由所选画面模式决定，不使用固定的“人物必须很小 + 巨型物件”模板。
- 社交媒体/知识卡片默认 4:5 竖版；文章正文默认 16:9 横版。
- 文字只在必要时使用 2-5 个短词，避免错误长文本。

## 安装

克隆仓库：

```bash
git clone https://github.com/Yuxuan-23/xixi-illustrations.git
cd xixi-illustrations
```

复制需要安装的技能目录：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./xixi-xiaoguang-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

## 使用方式

### 先做配图规划

```text
Use $xixi-xiaoguang-illustrations 先不要生图。
请分析下面这篇内容哪里值得配图，输出 5 张左右的 shot list。
每张图写清楚：放在哪段后、核心意思、画面模式、西西和小光分别在做什么、建议短标注词。

<粘贴内容>
```

### 直接生成正文配图

```text
Use $xixi-xiaoguang-illustrations 把下面这篇文章生成 4 张西西与小光共同参与的手绘讲解图。
文章正文用 16:9 横版。每张先从系统流程页、旅程隐喻图、分析讲解卡或判断关系卡中选择一种，不要套用同一构图。

<粘贴内容>
```

### 为单个观点生成知识卡片

```text
Use $xixi-xiaoguang-illustrations 为“证据不等于结论，先看见关系，才能形成判断”生成一张 4:5 竖版知识卡片。
让西西观察证据卡，小光用光轨把信息引向关系装置；人物合计不要超过画面的三分之一。
```

更多可复制的请求见 [examples/prompts.md](examples/prompts.md)。

## 工作流程

1. 阅读内容，选择值得视觉化的认知锚点。
2. 先输出 shot list；一张图只选一个判断或结构，再选择一种画面模式。
3. 只读取西西相貌参考和该模式的对应样图。
4. 单张生成并检查人物稳定性、互动关系、信息表达和文字。
6. 保存最终 PNG 并说明用途与路径。

## 目录结构

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── examples/
│   └── prompts.md
└── xixi-xiaoguang-illustrations/
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── assets/master-reference.png
    ├── assets/xixi-face-reference.png
    ├── assets/upstream-archive/
    └── references/
        ├── modes.md
        ├── character.md
        └── qa.md
```

## 致谢与许可

本仓库改造自 Ian 的 `ian-xiaohei-illustrations`，保留其 MIT 许可证与衍生作品署名说明；西西、小光和主参考图为本项目的视觉资产。详见 [NOTICE.md](NOTICE.md) 与 [LICENSE](LICENSE)。
