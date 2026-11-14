\---  
name: music-build  
description: 音乐**制作全流程知识与参数级操作指南，覆盖编曲配器、混音、母带、MIDI 制作、**&#x7EAF;音乐（器乐）制&#x4F5C;**、**&#x60C5;感表达**与参考曲逆向分析。**&#x9ED8;认在 DAW 里作曲编&#x66F2;**（MIDI + 采样音源 + 合成器 + 自动化 + 混音），合成器是正常音色来源；**&#x5435;闹电子舞曲风&#x683C;**（EDM/House/Techno/Trap/drop）另见独立文档 `electronic-styles.md`。并含**编曲写作专&#x9898;**：**&#x60C5;绪驱动编曲配方（按情绪分类）**、**&#x573A;景与感受塑造配方（梦幻/宏大/悲壮/神秘等）**、情绪×场景组合矩阵、钢琴/小提琴/手风琴三件主体乐器写法、配器法、经典曲目拆解、乐理速查、可复用和弦库、真实乐器音源与采样库、编曲哲学、B 站学习地图、抽帧谱例与口述转写笔记。当用户要求做音乐、编曲、配器、混音、母带、导出成品，或问某段音乐"为什么听着浑浊/刺耳/单薄/没层次/没感觉"、要求"我要这种效果"并给出参考曲、需要 EQ/压缩/混响/响度等具体参数建议、要用合成器铺底/pad/bell 做氛围、要做纯音乐（没有歌词的曲子）或想表达某种情绪，或说"想写宏大的/悲伤的/梦幻的/悲壮的/神秘的…"这种情绪与场景需求、问和弦怎么走 / 有哪些万能和弦 / 音程调式 / 乐器音域 / 选哪套音源 / 钢琴小提琴手风琴怎么写 / 编曲为什么没层次 / 去哪系统学编曲时使用。  
agent_created: true  
\---**

# **Music Build**

**面向独立创作者的音乐制作知识与工作流。核心理念：  
所有建议都给可执行的数值和顺序，不给"要合理使用 EQ"这种废话。**

**环境假设为 Windows + DAW（含浏览器 DAW）+ MIDI 工具链 + 采样音源 + 合成器。**  
吵闹电子舞曲风格单独存 `references/electronic-styles.md`；合成器在主线里正常用。

## **何时使用**

- **用户描述的是情绪 / 画面 / "某种感" 而不是技术需求**（"想写那种宏大的悲伤""要梦幻一点""要悲壮"）→ **默认走情绪驱动工作流**（见下）
- **用户要做一段音乐、编曲、混音、母带、导出成品**
- **用户描述听感问题（浑浊/刺耳/单薄/糊/动态死/人声被埋）**
- **用户给出参考曲说"我要这种效果**"→ 走参考曲逆向分析流程
- 用户要具体的频率、压缩参数、响度目标、混响时间等数值建议
- 用户要做编曲编排、段落规划、配器决策
- **用户要做纯音乐/器乐曲/没有歌词的音乐**（谁当主唱、段落怎么标记、各曲风要点）
- **用户要表达某种情绪**（悲伤/史诗/宁静/紧张…）或问"怎么让音乐有感情/有感觉"
- **要塑造场景与感受质感**（梦幻感、宏大感、悲壮感、神秘感、空灵、苍凉、圣洁…）→ `scene-texture-recipes.md`
- **情绪 + 场景感叠加**（"悲伤又梦幻""宏大而悲壮"）→ `scene-emotion-matrix.md` 组合矩阵
- **按情绪查配方、查和弦、查配器** → `emotion-arrangement-recipes.md`、`emotion-chord-index.md`
- **写钢琴 / 小提琴 / 手风琴**（宏大叙事与悲伤的主体乐器）→ `core-instruments.md`
- **要用合成器 pad / 铺底 / bell / soft lead 做氛围，但不要吵闹电子风格** → `scene-texture-recipes.md`、`resources.md`（合成器是正常音色来源）
- **明确要做 EDM / House / Techno / Trap / drop 这类吵闹电子舞曲风格** → `electronic-styles.md`（独立存档）
- **要做经典 / 传统写作法**（古典、管弦、爵士、华语流行、摇滚、民谣、中国风、影视配乐等）→ `classic-arrangement.md`、`classic-breakdown.md`
- **查乐理 / 音程 / 调式 / 四部和声 / 终止式 / 转调 / MIDI 音高号** → `theory-cheatsheet.md`
- **要一条能直接抄的和弦进行，或想把平淡进行改高级** → `chord-library.md`
- **选钢琴 / 弦乐 / 管乐 / 民乐 / 鼓的音源与采样库，或判断一个音源好不好** → `instrument-libraries.md`
- **要安排循环 / 一个 loop 反复几遍就腻 / 动机发展** → `loop-and-rhythm.md`（含「循环不腻的八种手法」）
- **要设计节奏型、律动不对、鼓组怎么写、swing 调多少** → `loop-and-rhythm.md`
- **音色太假 / 想换掉廉价 GM / 问 LMMS 能用什么音色库 / VST3 与 SFZ 怎么落地** → `lmms-tone-libraries.md`（本机实测，含格式边界与硬数据）
- **"技术都对但不好听 / 没层次 / 一直很满"，或要编曲自检清单与训练法** → `arrangement-philosophy.md`
- **要找 B 站教程、看课程谱例、重新采集素材** → `bilibili-up-map.md`、`bilibili-study-map.md`、`frame-notes.md`

> **制作口径**：用户**全程在 DAW 里作曲编曲**——MIDI + 采样音源 + 合成器 + 自动化 + 混音。  
> 真实乐器、采样音源、合成器音色都是**合法音色来源**，不做「原声 vs 电子」的出身审查。  
> **范围分流**：不默认做**吵闹的电子舞曲风格**（EDM / House / Techno / Trap / Dubstep /  
> 鼓机 drop / riser / 泵感侧链 / supersaw lead），这类内容单独收在  
> `references/electronic-styles.md`，主线不混。  
> **主用途**：情绪驱动 + 场景感双轴 + **钢琴 / 小提琴 / 手风琴**三件套；  
> 合成器在这条主线里的角色是**色彩与空间**（pad / bell / soft lead / 铺底），不是舞曲骨架。  
> 专题内的视频观点与技能硬规则冲突时，以技能硬规则为准——**视频是素材，不是裁判**。
>
> **用户主做情绪驱动编曲**，常见目标是宏大叙事与悲伤，并强调  
> **场景与感受塑造**（梦幻 / 宏大 / 悲壮 / 神秘）。  
> 给编曲建议时默认按三件套与「情绪 + 场景感」双轴思考，  
> 不要先抛一套乐队四大件或吵闹电子舞曲模板。  
> **注意**：真实乐团各声部人数 / 谱台数这类行政数字在 DAW 制作里没有执行价值，不要当干货输出。

## 工作方式

### 情绪驱动工作流（默认路径）

用户说情绪、"某种感"或画面、不讲技术时，**按这个顺序给方案**，不要跳步：

```
1. 定情绪坐标   → 效价(正/负) × 唤醒(高/低) + 强度级别（含蓄 / 宣泄）
                   情绪卡见 emotional-expression.md §1
2. 查情绪配方   → emotion-arrangement-recipes.md：该情绪的 BPM / 调式 / 密度曲线 /
                   段落弧线 / 混响与动态 / 两个失败模式
3. 定场景感     → scene-texture-recipes.md：梦幻 / 宏大 / 悲壮 / 神秘 …
                   这一轴管音区、织体、和声色彩、空间、动态、时间形状
4. 查组合矩阵   → scene-emotion-matrix.md：情绪 × 场景感的强组合 / 冲突组合，
                   拿「悲伤 × 梦幻」「宏大 × 悲壮」这类现成配置
5. 按情绪查和弦 → emotion-chord-index.md 的主索引，回查 chord-library.md 拿完整变体
6. 落到三件套   → core-instruments.md：钢琴/小提琴/手风琴的音区、奏法、
                   voicing、力度曲线、MIDI 人性化数值
7. 自检         → arrangement-philosophy.md §15 自检清单 +
                   emotional-expression.md 的情绪弧线与高潮设计
```

**两条分类轴，各管各的事**：**情绪定调式与弧线，场景感定音区与空间**。  
两轴先各自锁死再叠加；冲突时以情绪为主、质感为辅（裁决规则见 `scene-emotion-matrix.md`）。

**情绪先于编制，编制先于音符。** 用户改口说"再悲伤一点 / 再梦幻一点"时，  
优先动的是调式、和声节奏、音区高度、留白比例、力度曲线与混响时间  
（见情绪配方的「情绪 → 可调参数」映射表、场景配方的「调强/调弱旋钮表」），  
**不是先加一层乐器**。

### 先定位问题在哪个环节

```
听感不对
 ├─ 段落没有起伏 / 一直很满        → 编曲问题 → arrangement.md
 ├─ 某个元素听不清 / 整体浑或刺     → 混音问题 → mixing.md
 ├─ 整体不够响 / 各平台音量不一致   → 母带问题 → mastering.md
 ├─ 音符机械 / 演奏感假            → MIDI 问题 → workflow.md §4
 ├─ 做的是没有歌词的曲子            → 纯音乐专题 → instrumental-production.md
 ├─ 说不清，就是想"像某首歌"        → 逆向分析 → reference-analysis.md
 ├─ "技术都对但没感觉/情绪不对"      → 情感表达 → emotional-expression.md
 ├─ 说得出情绪、不知从哪下手        → 情绪配方 → emotion-arrangement-recipes.md
 ├─ 要梦幻/宏大/悲壮/神秘这类"感"   → 场景质感 → scene-texture-recipes.md
 ├─ 情绪 + 场景感怎么叠 / 会不会打架 → 组合矩阵 → scene-emotion-matrix.md
 ├─ 情绪对了但和弦不对味           → 情绪和弦索引 → emotion-chord-index.md
 ├─ 和弦不会走 / 进行平淡           → 和弦库 → chord-library.md
 ├─ 三件套写得干 / 不像在叙事       → 主体乐器 → core-instruments.md
 ├─ 音程调式转调记不住 / 写 MIDI 查数 → 乐理速查 → theory-cheatsheet.md
 ├─ 不知给哪些乐器写 / 声部打架      → 配器法 → classic-arrangement.md
 ├─ 想抄某首经典作品的编法          → 拆解库 → classic-breakdown.md
 ├─ 音色假 / 不知选哪套音源         → 采样库 → instrument-libraries.md
 └─ "堆了一堆音色还是不好听"        → 编曲哲学 → arrangement-philosophy.md
```

**编曲阶段的问题不要用混音解决。** 浑浊的常见根因是两件乐器抢同一频段，  
而不是 EQ 没调好——先在编曲层面让位，再考虑 EQ。

**情绪问题不要用参数解决。** "没感觉"的根因通常是：没定情绪目标（效价/唤醒  
两个轴没有裁判）、弧线平（唤醒值全程不变）、高潮通胀或压根没设计结尾——  
先看 `emotional-expression.md` 的情绪卡与情绪弧线，再动笔。

**"堆音色"不是编曲。** 层次来自前景—中景—背景的分工与留白，  
见 `arrangement-philosophy.md` §2/§3；换更好的音源解决不了配器问题。

### 给建议时必须带数值

正面：`人声与吉他冲突通常在 200–400 Hz，把人声这边切 2–3 dB、Q=1.2`  
负面：`注意 EQ 的合理使用`

数值是**起点不是法则**，要说明"以耳朵为准"。

### 区分事实与惯例

- **有出处的事实**：平台 LUFS 标准、GM 音色表、音程与和弦构成、压缩器参数语义
- **业界惯例/经验**：具体参数区间、手法偏好、B 站 UP 主的编曲心得

标注清楚，用户才知道哪些可以放心改。经典编曲专题里的  
`【源】/【事实】/【验】/【经验】/【通用理论补充】` 沿用这套分界。

## 目录导航

### 通用制作流程（原有）

| 文件                                      | 内容                                                                                                          |
| --------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| `references/workflow.md`                | 采样率/位深、工程组织、导出格式、**MIDI 人性化与 GM 音色表**                                                                       |
| `references/arrangement.md`             | 歌曲结构、段落职能、动态密度控制、**频率分工表**、声部写作                                                                             |
| `references/mixing.md`                  | 增益架构、EQ/压缩/混响/声像、**常见病症诊断表**                                                                                |
| `references/mastering.md`               | 各平台 LUFS 标准、true peak、母带 EQ 顺序、验证清单                                                                         |
| `references/reference-analysis.md`      | **CAR 原则**：用数据反推参考曲的编配与混音                                                                                   |
| `references/melody-revision.md`         | **旋律去重复/变奏改写**：量化重复、5 类同节奏换音高手法、和弦吻合度校验、叠奏轨陷阱、A/B 验证                                                        |
| `references/stem-mix-pipeline.md`       | **无 DAW 分轨混音流水线**：分轨渲染、体检表、送混响的音色、IR 生成三大坑、tanh 饱和哑炮、分频动态陷阱、LUFS/真峰                                         |
| `references/sample-instrument-swap.md`  | **换采样音源**：Salamander+sfizz 离线渲染、`--use-eot` 必加、1/3 倍频程正确测频、换源后必做的低频重分工、严格 A/B                               |
| `references/instrumental-production.md` | **纯音乐（器乐）制作**：五根柱子接管歌词职能、动机展开十法、无歌词段落标记法、分曲风要点（独奏钢琴/ambient/后摇滚/cinematic/lo-fi/电子/jazz）、纯音乐混音母带专项、交付物与训练练习 |
| `references/emotional-expression.md`    | **情感表达**：效价–唤醒模型、BRECVEMA 八机制、期待管理工程化、特征→情绪映射表、10 种情绪配方、乐器音色情绪字典、情绪弧线与高潮设计、chills 触发点                       |
| `references/resources.md`               | 免费 DAW / 合成器 / 采样音源 / 效果器 / cheatsheet 清单 + 本技能专题索引                                                         |
| `references/electronic-styles.md`       | **电子舞曲 / 吵闹电子风格（独立存档）**：结构、drop、riser、侧链、分风格 BPM 速查、与主线接口；主线不混                                              |

### 情绪驱动编曲（用户主用途，按情绪分类）

| 文件                                          | 内容                                                                                                                               |
| ------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `references/emotion-arrangement-recipes.md` | **情绪配方库（默认入口）**：15 张配方卡（12 个指定情绪 + 童真/宿命感/神性 3 个附加），每卡给效价/唤醒、BPM、调式、和弦、密度曲线、三件套分工、段落弧线、混响与动态、失败模式；含 14 项「情绪 → 可调参数」映射表与 15 行一页速查 |
| `references/emotion-chord-index.md`         | **按情绪查和弦**：12 类情绪 × 3–5 条进行的主索引、同一进行换情绪的 10 组改写、情绪弧线上的和声调度、三件套 voicing 提示                                                        |
| `references/core-instruments.md`            | **钢琴 / 小提琴 / 手风琴**：音域与常用音区、奏法清单、情绪映射、织体模板、MIDI 人性化数值、宏大叙事 vs 悲伤两套配置、三者让位与音源落地                                                    |

### 场景与感受塑造（第二分类轴）

| 文件                                    | 内容                                                                                                                                       |
| ------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `references/scene-texture-recipes.md` | **按「感」分类**：梦幻 / 宏大 / 悲壮 / 神秘 / 空灵 / 苍凉 / 圣洁 / 压抑 / 童真 / 破败 / 黎明 / 宿命等 12+ 种，每种给六大杠杆（音区、织体、和声色彩、空间、动态、时间形状）的具体数值、三件套配置、调强/调弱旋钮、8 小节微型织体方案 |
| `references/scene-emotion-matrix.md`  | **情绪 × 场景感 组合矩阵**：12×12 强组合/可用/慎用/冲突标注、12 组高频组合配方卡（含参考作品）、5 步决策顺序、三件套角色切换表、冲突诊断                                                          |

### 编曲写作专题（B 站素材扩充）

| 文件                                     | 内容                                                                                                                                   |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `references/classic-arrangement.md`    | **配器法**：乐器音域总表（中央 C=C4 口径）、管弦编制、木管铜管、弦乐组、乐队四大件、织体四型、四部和声连接、中国风民乐、Big Band、配器错误清单、编写 SOP                                              |
| `references/classic-breakdown.md`      | **经典曲目拆解**：把"这首歌为什么好听"翻译成可执行手法，按华语流行 / 中国风 / City Pop / 爵士标准曲 / 摇滚 / 影视动画 / 古典小品分类，含前奏间奏尾奏写法                                         |
| `references/theory-cheatsheet.md`      | **乐理速查卡**：音程、音阶调式、五度圈调号、和弦构成（含 MIDI 音高号）、功能组、四部和声禁忌、终止式、转调、拍号、首调/固定调/Nashville 对照、写 MIDI 执行顺序                                        |
| `references/chord-library.md`          | **可复用和弦库**：4536251、1645、卡农、ii–V–I、布鲁斯、副属链、模态互换、五声/中国风、影视持续音等，每条给级数 + 具体和弦名 + bass + 情绪 + 段落 + 变体，附 12 种"变高级"改写手法                     |
| `references/instrument-libraries.md`   | **真实乐器音源与采样库**：采样播放器对照、判断音源好坏的硬指标、钢琴/弦乐/管乐/吉他/鼓/民乐分类目录、免费起步三级配置、加载优化与商用授权                                                            |
| `references/arrangement-philosophy.md` | **编曲哲学**：三层听觉注意力、留白减法、对比重复比例、动机发展、信息量管理、编曲与混音职责边界、参考曲四遍法、常见误区、20 条自检清单、卡住时的 10 个决策顺序                                                 |
| `references/bilibili-up-map.md`        | **B 站 UP 主 / 合集导航**：58 个视频经接口核实（aid/cid/分P 大纲/简介/高赞评论干货），按系统课、乐理、和声、爵士、配器、扒带、影视中国风、音源分类；含单条拆解与结构化核实来源两份附录                            |
| `references/bilibili-study-map.md`     | **B 站学习地图**：973 条真实视频去重筛选后的分主题清单（BV 号 / UP 主 / 播放量），含采集口径与已知偏差                                                                       |
| `references/frame-notes.md`            | **抽帧谱例笔记**：8 个课程视频下载抽帧后 38 张拼图的画面实录，带 `t=MM:SS` 时间戳，只记能辨认的谱例与数值                                                                      |
| `references/audio-transcript-notes.md` | **口述干货**：8 个课程视频本地语音转写（56 分钟）提炼，补抽帧看不到的讲解正文——声部分组与 DAW 工程轨道顺序、弦乐三步 SOP 与 CC11→CC1→CC7、DAW 落地检查清单、和弦进行的情绪语义、常用进行↔例曲、中国风五声 4566、和声学习路线 |
| `references/loop-and-rhythm.md` | **循环与节奏**：循环的四个层级、ostinato 四种位置、**循环不腻的八种手法**、loop 长度选择（含奇数长度）、情绪/场景下的循环配方、三件套在循环里的分工、接缝处理；节奏三层结构、**四步设计节奏型**、常用节奏型格点表、律动量化的三个数值、段落间节奏对比 |
| `references/lmms-tone-libraries.md` | **LMMS 音色库**（本机实测）：LMMS 格式边界（SF2/GIG/VST2 可用；**VST3/SFZ 不可用、无音频输入**）、**GM 为什么廉价的硬数据**（100% 循环采样、采样 0.30 s、强弱只改音量）、五条突破路线、可用音源清单、三件套落地配置 |

> 专题来源为 B 站公开教程 / 专栏 / 测评（采集于 2026-11-10）。  
> 逐条出处见各文件末尾的「来源索引」；**BV 号与链接均经接口或页面核实，未编造**。

## 任务路由

| 要做的事                                 | 去哪                                               |
| ------------------------------------ | ------------------------------------------------ |
| 规划歌曲结构与各段配器                          | `arrangement.md`                                 |
| 判断两件乐器是否打架                           | `arrangement.md` §3 频率分工表                        |
| 修听感问题                                | `mixing.md` §6 诊断表                               |
| 定压缩参数                                | `mixing.md` §3 参数表                               |
| 定响度目标                                | `mastering.md` §1                                |
| 做 MIDI 不想太机械                         | `workflow.md` §4                                 |
| 复刻参考曲的效果                             | `reference-analysis.md`                          |
| 做纯音乐/器乐曲（无歌词）                        | `instrumental-production.md`                     |
| 想表达某种情绪/曲子"没感觉"                      | `emotional-expression.md`                        |
| 找免费工具                                | `resources.md`                                   |
| 用户说了一个情绪，要整套方案                       | `emotion-arrangement-recipes.md`（默认入口）           |
| 要梦幻 / 宏大 / 悲壮 / 神秘等"感"               | `scene-texture-recipes.md`                       |
| 把某种感调强 / 调弱                          | `scene-texture-recipes.md` 旋钮表                   |
| 情绪 + 场景感叠加 / 会不会打架                   | `scene-emotion-matrix.md`                        |
| "悲伤又梦幻""宏大而悲壮"这类组合                   | `scene-emotion-matrix.md` 高频组合配方卡                |
| 把某段改得更悲伤 / 更宏大                       | `emotion-arrangement-recipes.md`「情绪 → 可调参数」      |
| 按情绪挑和弦进行                             | `emotion-chord-index.md`                         |
| 同一条进行想换个情绪                           | `emotion-chord-index.md` 改写手册                    |
| 钢琴 / 小提琴 / 手风琴怎么写                    | `core-instruments.md`                            |
| 宏大叙事 / 悲伤的三件套配置                      | `core-instruments.md` 两套配置对照表                    |
| 写管弦 / 弦乐 / 乐队四大件 / 民乐                | `classic-arrangement.md`                         |
| 查某乐器音域、查声部连接禁忌                       | `classic-arrangement.md` §2 / §8                 |
| 抄一首经典作品的编法                           | `classic-breakdown.md`                           |
| 查音程/调式/和弦构成/转调                       | `theory-cheatsheet.md`                           |
| 要一条能用的和弦进行                           | `chord-library.md` §1                            |
| 把平淡和弦进行改高级                           | `chord-library.md` §3                            |
| 选音源 / 判断音源好坏                         | `instrument-libraries.md`                        |
| 编曲堆满了但不好听 / 要自检                      | `arrangement-philosophy.md`                      |
| 找系统课 / UP 主 / 看分P 大纲                 | `bilibili-up-map.md`                             |
| 按主题找 B 站课程 / 看课程谱例                   | `bilibili-study-map.md` / `frame-notes.md`       |
| 看课程讲者口述的「为什么 / 怎么做」                  | `audio-transcript-notes.md`                      |
| 查声部分组 / 工程轨道顺序、弦乐写法的数值顺序             | `audio-transcript-notes.md` §1 / §2              |
| 用合成器铺底 / bell / soft lead，但不要舞曲骨架    | `scene-texture-recipes.md`、`resources.md`        |
| 做吵闹电子舞曲风格（EDM / House / Trap / drop） | `electronic-styles.md`                           |
| 问真实乐团人数 / 谱台数                        | `audio-transcript-notes.md` §1（**DAW 用不上**，只作背景） |
| 要安排循环 / 一个 loop 反复几遍就腻了 / 动机怎么发展      | `loop-and-rhythm.md` §1–§7                       |
| 要设计节奏型 / 律动不对 / 鼓组怎么写 / swing 多少       | `loop-and-rhythm.md` §8–§14                      |
| 选音源 / 音色太假太廉价 / LMMS 能用什么音色库 / VST3 怎么用 | `lmms-tone-libraries.md`                          |
| 要装某个免费音源但不知道 LMMS 认不认                | `lmms-tone-libraries.md` §1（格式边界表）+ §4           |
| 要把方案落成工程 / 渲染出音频                     | 转交 `cli-lmms`（`lmcli`，LMMS 1.3 无头）               |
| 多路乐器打架 / 浑浊刺耳 / 要声场规划                | 转交 `music-mixing-craft`（含 `mix_layout.py`）       |


## 十四条硬规则

1. **频率是稀缺地产**——每件乐器只拿自己的主战场，抢频段时必须有一件让路。
2. **HPF 先行**——除 kick 与 bass 外，几乎每个元素都要做 gentle HPF。
3. **压缩顺序固定**：先定 ratio，再调 threshold 到目标 gain reduction。
4. **混响/延迟走 send，不走 insert**——保证所有元素在同一空间。
5. **120 Hz 以下 mono**；mono 兼容性检查不应为负。
6. **调参考曲时用 LUFS 对齐，不要用 peak**；响度不匹配的 A/B 等于没做。
7. **先填情绪卡再动笔**——效价由调式管、唤醒由速度管，两个轴先锁死，  
   每个编曲决策才有裁判（`emotional-expression.md` §1）。
8. **纯音乐里音色就是报幕员**——段落转换必须有可听见的事件：新音色进入、  
   全停、鼓组进出或调性转移，至少来一样（`instrumental-production.md` §4）。
9. **先定音色轨与声部让位，再写音符**——工程轨道分组、音域表与让位关系先于音色堆砌；  
   任一时刻只有一个焦点声部，其余声部在**编曲阶段**让位，不留给 EQ 擦屁股  
   （`classic-arrangement.md` §1、`arrangement-philosophy.md` §7）。
10. **情绪与场景感是两条分类轴，不是形容词**——用户说情绪时先按情绪查配方与和弦索引，  
    说"梦幻/宏大/悲壮/神秘"时按场景感查质感配方，两者再叠；  
    "再悲伤一点 / 再梦幻一点"优先改调式、和声节奏、音区、留白与混响，不先加乐器  
    （`emotion-arrangement-recipes.md`、`scene-texture-recipes.md`）。
11. **情绪定调式与弧线，场景感定音区与空间**——两轴各自锁死再叠加，  
    冲突时以情绪为主、质感为辅（`scene-emotion-matrix.md`）。
12. **DAW 是默认制作环境，合成器是合法音色来源**——MIDI + 采样音源 + 合成器 +  
    自动化 + 混音，不做「原声 vs 电子」的出身审查；合成器在主线里是色彩与空间层。  
    **吵闹电子舞曲手法只在 `electronic-styles.md`**，与情绪 / 场景两轴冲突时一律让位。  
    真实乐团人数 / 谱台数对 DAW 无执行价值，不作为干货输出。
13. **推荐音源之前先确认格式能落地**——LMMS 只认 SF2 / GIG / 64 位 VST2，
    **不认 VST3 和 SFZ，也没有音频输入**。没验证过出声的音源不要推荐；
    判断音色好坏看**采样长度、有无循环点、力度层是否换采样**，不看宣传词
    （`lmms-tone-libraries.md`）。
14. **自建 SF2 入库前必须验「它到底循不循环」**——渲染一个 4 小节长音，看最后一个超过 −40 dB 的点落在哪（`_loop_probe.py`）。只跑 `sf2_audit` / `sf2_loopcheck` 会被骗：采样头里有 loop 点、接缝指标也漂亮，但 generator 写错时播放器根本不用它，长音一两秒就断。**「能出声」不等于「格式被接受」。**

## 与其他技能的配合

本技能只管**写什么、为什么**（情绪 / 场景感配方、和弦、配器、织体、参数起点）；  
**落成工程并出音频**交给 `cli-lmms`，**让多路乐器不打架**交给 `music-mixing-craft`。

| 环节          | 技能                   | 接口                                                                                                                                                                      |
| ----------- | -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 定方案         | `music-build`（本技能）   | 情绪配方 → 和弦索引 → 三件套织体 → 音区 / CC / 混响数值。产出**编曲方案**，不是工程文件                                                                                                                  |
| 落地成工程 / 出音频 | `cli-lmms`           | LMMS 1.3.0-alpha.2 无头 CLI `lmcli`：建 `.mmp`、加轨（22 种原生合成器 / TAL VST2 / 2 套 GM SoundFont / 421 采样）、写音符、琶音和弦器、效果器与总线、自动化、`render` WAV / 分轨；`doctor --render` + `wavInfo` 验收 |
| 声场与不打架      | `music-mixing-craft` | 频率掩蔽与避让、1–3 dB 动态让位 / 侧链、X/Y/Z 空间与混响深度、浑浊刺耳诊断；`scripts/mix_layout.py --tracks …` 直接出声场规划                                                                                |
| 回修方案        | `music-build`        | 混音诊断若指向「同时发声太多 / 音区重叠」，改的是配器与织体（硬规则 1 / 9），不靠 EQ 救                                                                                                                      |

### 典型链路（顺序别跳）

1. **本技能**：`emotion-arrangement-recipes.md` 定效价/唤醒 + BPM/调式 → `emotion-chord-index.md` 拿级数 → `core-instruments.md` 定三件套音区与 voicing → `scene-texture-recipes.md` / `scene-emotion-matrix.md` 定混响、空间与密度预算。
2. **`cli-lmms`**：按上面的 BPM / 调式 / 级数建工程；**三件套优先挂自建音色**（`--file D:/LMMS13/data/soundfonts/SalamanderV3-4L.sf2` / `ViolinVSCO.sf2` / `AccordionHN.sf2`，`--patch 0`；小提琴要逐音精确、不要拉伸时换 `ViolinIowa.sf2`），只有临时试听才退回 `FluidR3_GM`（钢琴 0 / 小提琴 40 / 手风琴 21）；选型与实测数据见 `lmms-tone-libraries.md` §5 / §8；合成器 pad 用 `tripleoscillator` 或 TAL-NoiseMaker 挂在色彩组；`addAutomation --param vol` 画情绪曲线；`render out.wav --normalize -1` → `wavInfo` 必须 `silent:false`、`peakDb ≤ 0`。
3. **`music-mixing-craft`**：拿实际音轨清单跑 `mix_layout.py`，按输出做纯推子平衡 → 200–500 Hz 去浑浊 → 1–3 dB 让位；混响返回轨 HPF 200–250 Hz、低通 8 kHz、加 pre-delay 并对主角侧链。
4. **回到本技能**：若诊断是编曲层问题（乐器太多、音区重叠、密度预算超了），用 `arrangement-philosophy.md` 做减法后重回第 2 步。

### 三个接口坑

- **中央 C 口径（实测纠正）**：本技能统一 `C4 = MIDI 60 = 261.63 Hz`。`addNotes` 里写 `key=C4` 时，LMMS 送进 SF2 的是 **MIDI 72**（实测三口不同 SF2 渲染基频都是 523.8 Hz）——LMMS 内部沿用 `C5 = 60`。后果：**自己写 SF2 的音域要按这个 +12 偏移核对**，否则会出现「音域 60–72 的采样，弹 A4 完全没声」。做 A/B 只要两边用同一组键名就不影响结论。
- **`CC11 / CC1 / CC7` 不是通用 MIDI 自动化**：`audio-transcript-notes.md` §2.7 那套是 Kontakt 类采样弦乐音源的控制器；LMMS 自动化只支持 `vol` / `pan` / `fcut` / `fres` / `fwet` / 乐器属性。在 LMMS 里用 `--param vol` 曲线近似 CC11 的情绪起伏，别硬找 CC11。
- **LMMS 边界**：只吃 64 位 VST2（VST3 挂不上）；`--wet` 范围 −1..1；LADSPA 混响默认 `blend=0` 是干声，要显式写 `blend=1`；`--normalize -1` 是常态，三振荡器满增益否则削顶。

> **边界**：本技能不生成工程文件、不渲染音频、不做逐轨混音诊断。这三类请求直接转交上面两个技能，  
> 不要在本技能里拿参数表硬凑。`music-mixing-craft` 给的是**深入诊断与声场规划**，  
> 本技能 `mixing.md` 只给通用参数起点，两者冲突时以「听感验收 + 参考曲 A/B」为准。

