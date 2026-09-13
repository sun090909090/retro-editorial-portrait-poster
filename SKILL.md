---
name: retro-editorial-portrait-poster
description: >
  将人物照片重新设计为具有强烈视觉冲击力的复古 Editorial 杂志拼贴人物海报。
  视觉参考 70s–90s 欧美杂志、电影宣传册、独立出版物、旧报刊印刷与现代 Editorial Design。
  适用于人物海报、作品集封面、杂志封面、人物专题、明星感编辑设计、复古拼贴肖像。
version: 1.0
---

# Retro Editorial Portrait Poster Skill

## 1. 核心目标

将用户提供的人物照片重新设计成一张具有强烈视觉冲击力的「复古 Editorial 杂志拼贴人物海报」。

整体视觉融合：

- 70s–90s 欧美杂志
- 电影宣传册
- 独立出版物
- 旧报刊印刷
- 复古电影明星 Editorial
- 现代 Editorial Design
- Halftone / Offset Print / Xerox / Cutout Collage

最终画面必须同时具备：

- 强人物主体
- 明确杂志信息层级
- 半调网点（Halftone）
- 拼贴剪纸感
- 复古印刷颗粒
- 超大标题排版
- 少量电影 / 明星文化元素
- 高级独立杂志感
- 黑、米白、暗红为基础核心色板
- 真实印刷感，而非廉价做旧滤镜

最终目标：

> 像一本真实存在的独立人物杂志封面，而不是 AI 把很多复古元素堆在一起。

视觉优先级始终为：

**人物 > 主标题 > 构图 > 信息 > 装饰 > 纹理**

---

# 2. 触发条件

当用户请求包含以下任一意图时触发本 Skill：

- 复古人物海报
- Editorial 人物海报
- 杂志封面人物海报
- 复古杂志风人物
- Halftone 人像
- 半调人物海报
- 拼贴人物海报
- 电影明星杂志海报
- 独立杂志封面
- Vintage magazine poster
- Retro editorial poster
- Editorial portrait
- Halftone portrait
- Cutout collage poster
- Analog print portrait
- 复古电影宣传册风格
- 用户上传人物照片并要求改成参考图类似的杂志拼贴风格

若只是普通摄影棚写真、商业证件照、美颜写真，则不要自动触发。

---

# 3. 输入检查

## 3.1 人物照片

优先检查用户是否提供人物照片。

### 已提供人物照片

进入人物编辑流程。

必须优先保留：

1. 人物身份特征
2. 五官
3. 发型
4. 人物姿势
5. 服装主体
6. 大致镜头角度
7. 身体比例

允许修改：

- 色彩
- 背景
- 光影
- 人物抠图边缘
- 拼贴轮廓
- Halftone
- 胶片颗粒
- 印刷纹理
- 排版
- 周边装饰
- 局部对比度

禁止：

- 随意改变长相
- 改变人物性别
- 明显改变年龄
- 换成完全不同发型
- 将人物变成插画人物
- 过度磨皮
- AI 塑料脸

### 未提供人物照片

若用户明确想制作自己的海报：

调用 `ask_human`：

> 请上传一张人物照片。最好使用正面或轻微侧脸、人物清晰、光线较明确的照片，我会尽量保留五官、发型、姿势和服装主体。

若用户只是想预览风格：

允许生成占位人物概念示例，但必须说明：

> 这是风格演示稿，人物为虚构占位人物。

---

# 4. 文案规则

优先读取用户提供的信息：

- 主标题
- 人物姓名
- 副标题
- 年份
- 主题词
- 期刊编号
- 作品名称
- 自定义短句

如果用户没有提供文案，不要反复追问。

默认可使用少量中性 Editorial 占位文案：

- PORTRAIT
- DESIGNER
- VOL.01
- INTERVIEW
- CREATIVE
- EDITORIAL
- ISSUE 01
- ARCHIVE
- 2026

如果需要人物姓名，而用户未提供：

不要虚构真实身份。

可使用：

- PORTRAIT
- SUBJECT 01
- UNTITLED
- EDITORIAL STUDY

禁止自动虚构：

- 公司
- 奖项
- 学校
- 经历
- 品牌代言
- 电影作品
- 真实人物背景
- 获奖记录
- 名人身份

禁止生成大量无意义随机英文。

---

# 5. 构图选择

每次生成从以下 4 类布局中选择。

默认优先：

**Layout A 或 Layout C**

除非用户指定其他布局。

---

## Layout A — Magazine Cover

适合：

- 杂志封面
- 作品集封面
- 人物专题
- 点击率较高的封面视觉

结构：

- 顶部：超大人物姓名 / 主标题
- 中部：人物居中或略偏一侧
- 人物占画面约 50%–70%
- 左右：2–4 组小型 Editorial 信息
- 局部文字与人物产生前后遮挡
- 角落：编号 / 条码 / 小标签
- 底部：少量电影工业元素

特点：

- 第一眼非常强
- 信息层级明显
- 接近真实独立杂志封面

---

## Layout B — Film Poster

适合：

- 电影感人物
- 明星 Editorial
- 叙事感人物海报

结构：

- 人物偏左或偏右
- 另一侧加入 1–3 张竖排小照片
- 小照片可使用胶片框 / contact sheet
- 底部出现少量场记板 / 电影票 / film code
- 超大标题纵向或横向压画面

特点：

- 更电影宣传册
- 更有故事感
- 不要变成传统电影海报

---

## Layout C — Editorial Collage

适合：

- 最强设计感
- 设计师作品集
- 独立出版物
- 拼贴感

结构：

- 人物位于视觉中心
- 背后出现大面积 Halftone 或低对比人物影像
- 主标题部分压在人物后方
- 局部字被人物遮挡
- 周围加入少量纸片、编号、照片碎片
- 不规则剪纸轮廓围绕人物

特点：

- 拼贴感最强
- 更先锋
- 仍需保持高级与克制

---

## Layout D — Minimal Retro

适合：

- 极简
- 高级作品集
- 用户不喜欢元素太多

结构：

- 超大标题
- 单一人物
- 2 个以内小标签
- 少量 Halftone
- 少量条码 / 编号
- 留白明显

特点：

- 更高级
- 更时尚
- 更接近现代 Editorial

---

# 6. 人物处理规范

人物必须是画面的第一视觉中心。

默认人物：

- 半身
- 胸像
- 正面
- 轻微侧脸
- 人物占画面约 45%–70%
- 可局部超出画面
- 保持人物清晰轮廓

推荐人物处理：

- 黑白
- 低饱和
- 高反差
- Slight crushed blacks
- Fine grain
- 轻微胶片感
- 真实皮肤纹理
- 保留毛孔和自然面部细节
- 加强轮廓阴影
- 背景与人物分离明确

人物周围可加入：

- 米白不规则剪纸轮廓
- Halftone dots
- 局部 Xerox texture
- Slight misregistration
- RGB/ink offset 极轻微错位
- 不规则纸张切边
- 局部套色偏移

人物不能变成：

- 普通影楼写真
- 纯商业摄影
- 过度磨皮
- 3D 人偶
- CG 塑料皮肤
- 朋克人物
- Y2K 人像
- Cyberpunk

---

# 7. 色板系统

## 7.1 默认色板

背景：

- `#171717`
- `#1C1A19`

纸张 / 文字：

- `#E7DED2`
- `#F0E6DA`

强调红：

- `#B73B42`
- `#C94B51`

辅助：

- 灰黑
- 深褐色
- 暗米色
- Warm gray

默认比例：

- 60% 黑 / 深灰
- 25% 米白
- 15% 暗红

---

## 7.2 用户上传人物照片时

分析人物照片的：

- 衣服颜色
- 肤色暖冷
- 背景主色
- 环境氛围色
- 最明显的非肤色区域

提取 1–2 个主色。

处理方式：

1. 降低饱和度
2. 略微压暗
3. 转为复古印刷色
4. 作为辅助色或替代默认暗红
5. 黑与米白仍保持中性基础

例如：

原图是蓝色衣服：

不要直接使用亮蓝。

转为：

- Dusty blue
- Faded navy
- Desaturated steel blue

原图是绿色：

转为：

- Olive
- Faded forest green
- Muted moss

原图是黄色：

转为：

- Mustard
- Ochre
- Aged warm beige

原图是粉色：

转为：

- Dusty rose
- Muted burgundy
- Aged pink

---

## 7.3 用户指定颜色时

用户指定颜色优先。

但必须进行复古化处理：

- 降饱和
- 压暗
- 避免荧光
- 避免过亮
- 避免科技感

指定色只作为：

- 强调色
- 小面积辅助色
- 主标题色
- Halftone 色
- 标签色

黑与米白保持基底。

---

# 8. 主标题可读性

主标题属于 Level 1。

必须是画面中最高文字层级。

优先颜色：

- `#F0E6DA`
- `#C94B51`

必要时：

- 加 1–2px 轮廓
- 增加浅色叠印阴影
- 利用人物遮挡形成层次
- 主标题局部被人物遮挡，但不能影响核心阅读

禁止：

- 主标题与背景颜色接近
- 黑色标题压在黑背景
- 深灰标题压在黑衣服
- 标题被纹理完全破坏
- 复杂图形覆盖主标题
- 字体过细

---

# 9. Typography 系统

必须具有明显 Editorial Typography。

## 主标题

使用：

- Extra Bold Sans Serif
- Condensed Bold
- Wide Bold
- Grotesk
- Geometric Bold
- Heavy Display

特征：

- 超大字号
- 可全部大写
- 可超出画面
- 可局部压图
- 可与人物产生遮挡

---

## 副标题

使用：

- Retro Serif
- High Contrast Serif
- Editorial Serif

作用：

- 增加杂志感
- 与主标题形成字体对比

---

## 小字

使用：

- Neutral Sans
- Clean Serif
- Mono
- Magazine caption style

只用于：

- ISSUE
- VOL.
- DATE
- INTERVIEW
- ARCHIVE
- NO.
- FILM CODE
- 小型说明

---

## 排版规则

必须具有明显字号差：

Level 1：超大标题  
Level 2：人物  
Level 3：Editorial 副标题  
Level 4：编号 / 条码 / credits

禁止所有文字字号差不多。

---

# 10. 图形元素库

每张海报从以下元素中选择 **3–6 种**。

不要全部使用。

候选：

- Halftone 半调圆点
- Retro Sparkle
- 四角星
- 感叹号
- 圆形会员章
- 条形码
- 电影票
- 胶片边框
- Contact sheet
- 场记板
- Film code
- Issue number
- 小标签
- 复古印章
- 箭头
- 不规则纸张
- 撕纸边缘
- 下划线
- 方框
- Editorial divider
- 细线
- 页码
- 印刷裁切标记

装饰元素必须服务构图。

禁止抢过人物与主标题。

---

# 11. 小照片 / Inset Photo 规则

每张海报最多使用：

**1–3 张小照片**

可以：

- 人物局部特写
- 眼睛
- 手部
- 衣服细节
- 同一人物不同裁切
- 黑白电影帧感裁切

禁止：

- 自动生成无关陌生人物
- 放入随机电影剧照
- 使用无法解释的明星照片
- 小照片数量过多

如果只有一张人物原图：

优先通过原图裁切不同区域形成 inset photos。

---

# 12. 材质系统

整个画面加入真实印刷质感。

必须使用细腻版本。

可组合：

- Fine film grain
- Paper texture
- Offset printing texture
- Xerox texture
- Ink bleeding
- Slight misregistration
- Dust
- Subtle scratches
- Faded ink
- Paper fibers
- Slight ink spread
- Analog print noise

强度原则：

- 纹理可见但不过度
- 纹理不能破坏人物五官
- 纹理不能破坏标题可读性
- 纹理不能导致画面显脏

禁止：

- 严重破损
- 重度划痕
- 大面积污渍
- 末日风
- 朋克脏乱
- 烧焦纸张
- 大面积撕裂

---

# 13. 信息层级

画面必须至少有 4 个层级。

## Level 1

人物姓名 / 海报主标题

要求：

- 第一眼可读
- 高对比
- 超大字号

## Level 2

人物主体

要求：

- 最强视觉中心
- 45%–70% 画面占比

## Level 3

2–4 个 Editorial 副标题

例如：

- INTERVIEW
- CREATIVE ISSUE
- PORTRAIT STUDY
- ARCHIVE
- VOL.01

## Level 4

编号 / 条码 / Credits / 小标签

第一眼必须看到：

**人物 + 主标题**

---

# 14. 风格控制

最终画面应该：

- 高级
- 时尚
- 大胆
- 年轻
- 复古
- Editorial
- 独立出版物感
- 设计师作品集感
- 有真实印刷味
- 有电影文化暗示
- 信息丰富但主次清晰

---

# 15. 禁止风格

禁止生成：

- 普通商业海报
- 朋克海报
- 朋克拼贴
- Y2K
- Cyberpunk
- 科技感 UI 海报
- 街头涂鸦
- 大面积撕纸
- 满屏文字
- 廉价复古滤镜
- 过多装饰
- 完全对称排版
- AI 随机乱码
- 高饱和霓虹色
- 蓝紫科技渐变
- 荧光绿
- 荧光粉
- 赛博蓝
- 过度脏污
- 模板化 Canva 商业海报感

---

# 16. 生成流程

## Step 1 — 判断是否有人物照片

如果有：

使用人物编辑模式。

如果没有：

- 用户想制作自己的海报 → ask_human 上传照片
- 用户只想看示例 → 允许生成虚构人物风格稿

---

## Step 2 — 获取文案

读取用户已有文案。

若没有：

直接使用少量占位 Editorial 文案。

不要为普通演示稿反复追问。

---

## Step 3 — 选择 Layout

默认逻辑：

- 40% Layout A
- 35% Layout C
- 15% Layout D
- 10% Layout B

若用户说：

“简洁一点” → Layout D  
“更杂志封面” → Layout A  
“更拼贴” → Layout C  
“更电影” → Layout B

---

## Step 4 — 确定色板

若有照片：

提取照片 1–2 个主要色彩 → 降饱和 → 压暗 → 作为辅助色。

若无：

使用默认黑 / 米白 / 暗红。

---

## Step 5 — 组装 Prompt

提示词必须包含：

- 人物优先级
- 布局类型
- 主标题
- 色板
- Halftone
- Cutout collage
- Editorial typography
- Analog print
- Offset print
- Film grain
- Paper texture
- 真实面部保持
- 低饱和
- 高反差
- 高级独立杂志
- 克制装饰
- 防乱码约束
- 禁止朋克 / Y2K / cyberpunk

---

# 17. 图片编辑调用

若用户提供人物照片：

使用：

`edit_media_v3(task_type=edit_image)`

人物照片作为 reference image。

核心执行要求：

> 保留人物身份、五官、发型、姿势、服装主体和主要构图关系，只重新设计背景、排版、色彩、拼贴轮廓、Halftone 与印刷质感。

不要重新创造一张完全不同的人。

---

# 18. 无人物示例调用

若用户没有人物照片但明确要求风格示例：

使用：

`generate_media_v3(task_type=generate_image)`

人物必须为：

- 虚构
- 无真实身份
- Editorial 模特感

并在回复中说明：

> 这是用于展示风格方向的虚构人物演示稿。

---

# 19. 主提示词模板

生成时可基于以下模板动态替换。

```text
Create a premium retro editorial portrait poster based on the provided portrait photo.

Preserve the subject's identity, facial structure, hairstyle, pose, body proportions and main clothing. Do not redesign the person into a different individual.

STYLE:
1970s–1990s European and American independent magazine design, vintage cinema publicity booklet, analog editorial publishing, retro celebrity magazine layout, modern editorial graphic design.

COMPOSITION:
Use {LAYOUT_TYPE}.
The portrait must remain the strongest visual focus and occupy approximately 45–70% of the canvas.
Create a clear magazine hierarchy with one oversized main headline, 2–4 smaller editorial subheads, and minimal supporting labels.
Use asymmetrical composition.
Allow selected typography to overlap or sit partially behind the portrait.
Do not distribute all elements evenly.

PORTRAIT:
High-contrast monochrome or low-saturation portrait treatment.
Keep realistic facial detail and skin texture.
No excessive retouching.
Add subtle film grain.
Add a cream irregular cutout outline around selected parts of the subject.
Use selective black-and-white halftone treatment and subtle offset print misregistration.

TYPOGRAPHY:
Oversized editorial headline using heavy grotesk, condensed bold, wide bold or geometric display typography.
Headline text: "{MAIN_TITLE}"
Use cream #F0E6DA or muted dark red #C94B51 for maximum readability.
Secondary typography can use high-contrast editorial serif.
Small labels should be clean and restrained.
Strong scale contrast between headline, subheads and small captions.
No random gibberish.

COLOR:
Base palette:
black / charcoal #171717 or #1C1A19,
aged cream #E7DED2 / #F0E6DA,
muted dark red #B73B42 / #C94B51.

Optional accent:
{PHOTO_DERIVED_ACCENT}

Any accent color must be muted, slightly darkened and adapted to vintage offset printing.
Avoid neon, bright gradients or futuristic colors.

GRAPHIC ELEMENTS:
Select only 3–6 restrained elements from:
halftone dots, retro sparkle, barcode, film frame, ticket, contact sheet, film number, stamp, thin divider, arrow, small label, editorial box, registration mark.
Decorative graphics must never compete with the portrait or headline.

TEXTURE:
Fine film grain,
subtle aged paper texture,
offset print texture,
light Xerox texture,
minor ink bleed,
slight misregistration,
soft dust,
faded ink,
visible paper fibers.

Keep texture sophisticated and subtle.
Do not make the poster dirty, destroyed, grungy, punk or apocalyptic.

OVERALL FEEL:
premium,
fashion-forward,
bold,
young,
cinematic,
independent publication,
designer portfolio,
real printed magazine cover,
authentic analog graphic design.

The final result should feel like a real independent portrait magazine cover, not an AI collage filled with random retro elements.

Visual priority:
portrait > headline > composition > editorial information > decoration > texture.

AVOID:
commercial advertising poster,
punk collage,
Y2K,
cyberpunk,
street graffiti,
neon colors,
blue-purple tech gradients,
too much torn paper,
symmetrical template layout,
random fake English,
plastic skin,
generic studio photography.
```

---

# 20. Layout Prompt 追加词

## Layout A

```text
LAYOUT A — MAGAZINE COVER:
Place an oversized masthead / subject name across the upper area.
Position the portrait centrally or slightly off-center below it.
Add 2–4 compact editorial information blocks on the left and right.
Add a small barcode, issue number and one film-related label near the bottom.
Maintain strong hierarchy and generous negative space.
```

## Layout B

```text
LAYOUT B — FILM POSTER:
Place the portrait strongly to one side.
Arrange 1–3 vertical inset photo frames or contact-sheet crops on the opposite side.
Use restrained film-code, ticket or clapperboard references near the bottom.
Maintain editorial magazine design rather than conventional movie poster composition.
```

## Layout C

```text
LAYOUT C — EDITORIAL COLLAGE:
Place the portrait at the center.
Create a large halftone silhouette or cropped enlarged portrait layer behind it.
Allow the main headline to move behind the subject in selected areas.
Add a few irregular paper shapes, small photo crops and compact editorial labels.
Keep the collage controlled, premium and spacious.
```

## Layout D

```text
LAYOUT D — MINIMAL RETRO:
Reduce decoration dramatically.
Use one oversized headline, one strong portrait and no more than two small labels.
Add only subtle halftone, grain, barcode or issue number.
Use generous negative space and sophisticated modern editorial balance.
```

---

# 21. Negative Prompt

若生成工具支持 negative prompt，加入：

```text
cheap vintage filter,
punk poster,
punk collage,
grunge overload,
Y2K,
cyberpunk,
neon,
futuristic UI,
blue purple gradient,
graffiti,
extreme torn paper,
dirty texture,
heavy scratches,
destroyed paper,
symmetric template,
generic commercial poster,
random text,
gibberish typography,
extra people,
wrong face,
changed hairstyle,
changed identity,
plastic skin,
over-retouched face,
3D character,
illustration face,
AI facial distortion
```

---

# 22. 文本生成安全策略

图像模型在复杂文字排版上可能出现拼写问题。

因此：

- 主标题必须尽量短
- 副标题控制在 1–4 个单词
- 小字数量保持克制
- 不要让模型生成大段正文
- 不要要求生成真实长段文章
- 不要使用完整人物履历

如果用户要求精确文字：

优先确保：

1. 人物姓名
2. 主标题
3. ISSUE / VOL.
4. 1–2 个副标题

其余装饰文字允许减少。

宁可少字，也不要乱码。

---

# 23. 输出后的回复方式

生成完成后，不需要长篇解释。

简洁说明：

> 已按复古 Editorial 独立杂志方向处理，保留人物主体，并加入 Halftone、剪纸轮廓、黑/米白/暗红体系与杂志信息层级。

然后给用户可继续调整的方向：

- 构图：更满 / 更留白
- Layout：A / B / C / D
- 色调：更黑白 / 更暗红 / 跟随人物衣服颜色
- 标题：更大 / 更压人物
- 拼贴：更强 / 更克制
- 纹理：更复古 / 更干净

---

# 24. 参考图使用原则

参考图只用于提取：

- 视觉语言
- 信息层级
- 构图逻辑
- 色彩关系
- Halftone 方法
- 印刷质感
- 拼贴方式
- 字体层级
- Inset photo 结构

禁止复制：

- 具体人物
- 具体人物姓名
- 原海报标题
- 原始歌词
- 原有 credits
- 原徽章
- 原场记板文字
- 完全相同星形位置
- 完全相同照片裁切
- 完全相同版式

---

# 25. 参考方向

## Reference 01

紫调独立 Halftone 拼贴海报：

https://xla-persist.xingliu.art/agent_connector/pinterest/c581f183a39444a6/Taesan_Aesthetic_Graphic_Poster.jpg

借鉴：

- 人物 Halftone 肖像作为绝对主体
- 周围小照片碎片
- 展示字体混合
- Lo-fi 氛围
- 双色调
- 不规则照片裁切

不得复刻：

- 具体人物
- 歌词
- 星形具体位置

---

## Reference 02

复古电影明星杂志海报：

https://xla-persist.xingliu.art/agent_connector/pinterest/6531ab66d04d8775/William_LYKN_@gelluvshongshi.jpg

借鉴：

- 杂志封面信息层级
- 刊头
- 副标题
- 小型正文
- 电影工业元素
- 多张 inset photo
- 黑 / 米白 / 暗红
- 网点轮廓
- 场记板
- 条码 / 印章
- 粗衬线刊头

不得复刻：

- 原人物
- “WILLIAM”
- 场记板原文字
- “LYKN” 徽章

---

## Reference 03

蓝双色调 Vogue 风格封面：

https://xla-persist.xingliu.art/agent_connector/pinterest/d7e1055004b280db/Pin.jpg

借鉴：

- 双色调 Halftone 肖像
- 矩形细节裁切
- 角落 credits
- 条码
- 高级时尚编辑感
- 局部细微星芒

不得复刻：

- 原人物
- “Maita”
- “Vogue”
- 原 credits

---

# 26. 最终关键词

```text
retro editorial portrait poster,
vintage magazine cover,
halftone photography,
editorial typography,
cutout collage,
offset print,
film grain,
black red cream palette,
bold typography,
independent magazine,
analog print texture,
cinematic celebrity editorial,
paper texture,
high contrast portrait,
graphic design poster,
1970s magazine,
1980s editorial,
1990s independent publishing,
film contact sheet,
xerox texture,
premium vintage print design
```

---

# 27. 最终判断标准

生成结果必须通过以下检查：

- 人物是否第一视觉中心？
- 主标题是否第一眼可读？
- 主标题是否与背景形成足够反差？
- 人物身份是否被保留？
- 是否存在至少 4 个清晰信息层级？
- 是否具有 Halftone？
- 是否具有真实 Offset Print / Paper texture？
- 是否控制在 3–6 种装饰元素？
- 是否避免满屏文字？
- 是否避免 AI 随机乱码？
- 是否避免廉价复古滤镜？
- 是否避免朋克 / Y2K / Cyberpunk？
- 是否像真实独立人物杂志封面？
- 是否仍然具有现代、高级、时尚感？

如果答案不是明显的“是”，则继续简化元素、增强人物与标题层级。
