# 生图提示词模板

每张图单独生成。生成前读取 `assets/master-reference.png` 与 `assets/xixi-face-reference.png`；前者只校准画风、服装、小光和互动比例，后者只校准西西面貌与头发。不要复刻其中任何一张的构图。

```text
Use case: illustration-story
Asset type: Chinese hand-drawn explainer illustration for {渠道/文章正文/知识卡片}

Input images:
- Image 1: assets/xixi-face-reference.png. Authoritative reference for Xixi's face shape, hairline, large loose wavy black hair, gentle mature eyes and expression, pearl hair clip, and pearl earring. Use it for Xixi's likeness only; do not copy its cream clothing, badge, pose, or layout.
- Image 2: assets/master-reference.png. Authoritative reference for Xiaoguang, warm ivory watercolor paper, mist-blue professional clothing, bright-gold light trails, and the rule that characters interact with a larger teaching object. Do not copy its evidence-to-conclusion cards or layout.

Primary request:
Create one standalone {4:5 vertical / 16:9 horizontal / user-specified} illustration that explains: {核心观点}.

Structure type:
{证据与结论 / 逐步流程 / 前后对比 / 关系地图 / 检查与选择 / 小场景隐喻}

Main teaching object:
{一个比角色大 1.5-3 倍的具体对象，例如大笔记本、关系网、地图、筛选器、桥、台阶、卡片容器}

Characters and interaction:
{成熟西西 / Q版西西} occupies only {约 15%-25%} of the image. Keep her black long wavy hair, silver pearl hair clip, visible pearl earring, and refined mist-blue tailored dress. She is {书写/观察/整理/指向/操作} the main teaching object.
Xiaoguang is a vivid warm golden-yellow round light companion with a small top glow bud, dot eyes, rosy cheeks, and a luminous tail. Xiaoguang {串联节点/递送卡片/点亮路径/照亮重点}. Both characters must physically interact with the same teaching object.

Scene and style:
Warm ivory watercolor paper, gentle blue washes, delicate pencil-and-ink outlines, mist blue information lines, vivid gold light trail, quiet negative space, polished Chinese hand-painted explainer illustration. Keep Xixi's full dress silhouette, lower hem, and any visible legs clearly separated from watercolor washes and the ground; do not let blue washes overlap or visually dissolve her clothing. The teaching object carries more visual weight than the people.

Text:
{no text / 2-5 exact short Chinese labels: “{词1}” “{词2}”}

Constraints:
One idea only. Keep the two characters together below 35% of the canvas. Preserve Xixi's recognizable face, large loose wavy hair, pearl hair clip, pearl earring, and blue professional outfit. Keep Xiaoguang bright gold and actively guiding information. No mandatory Haisen badge unless requested by the user.

Avoid:
Large central portrait, generic anime poster, childlike schoolgirl, sticker mascot, hard sci-fi UI, dense PPT infographic, long text, pseudo-text, dark background, neon, 3D render, watermark, copying the master reference layout, skirt or lower body blended into a blue watercolor puddle/background.
```

## 图像编辑提示

### 缩小人物、放大讲解物

```text
Edit the provided illustration. Keep Xixi and Xiaoguang's identity, watercolor style, and all existing information unchanged. Reduce the characters together to about 25% of the composition and enlarge the central teaching object and its interaction path. Xixi must still touch, write on, observe, or operate that object; Xiaoguang must still guide the path with its golden light tail. Do not add new text or a title.
```

### 从成熟西西转为 Q 版西西

```text
Edit the provided illustration into a refined Q-version of Xixi while preserving the same scene, message, and Xiaoguang. Change only Xixi to a 3-4-head-tall professional chibi proportion. Keep the large loose black wavy hair, pearl hair clip, visible pearl earring, gentle mature expression, and mist-blue tailored dress. Keep her smaller than the teaching object. Do not add a Haisen badge unless it already exists and is requested to remain.
```
