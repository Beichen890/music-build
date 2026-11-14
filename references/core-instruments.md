# 钢琴 / 小提琴 / 手风琴：三件主体乐器的情绪写法

> **来源**：B 站公开教程 / 专栏 / 测评整理（采集 2026-11-11，973 条去重视频、8 个课程视频下载抽帧）。逐条来源见文末「来源索引」，学习清单见 `bilibili-study-map.md`。
> **制作口径**：默认在 DAW 里作曲编曲（MIDI + 采样音源 + 合成器 + 自动化 + 混音）；真实乐器、采样、合成器音色都是合法音色来源，不做「原声 vs 电子」的出身审查。
> **范围分流**：不默认做吵闹的电子舞曲风格（EDM / House / Techno / Trap / Dubstep / 鼓机 drop / riser / 泵感侧链 / supersaw lead），这类内容单独收在 `references/electronic-styles.md`，主线不混。
> **主用途**：情绪驱动 + 场景感双轴 + 钢琴 / 小提琴 / 手风琴三件套；合成器在这里是色彩与空间层（pad / bell / soft lead / 铺底），不是舞曲骨架。
> **用法**：数值是起点不是法则，以耳朵为准；与本技能既有硬规则冲突时，以技能规则为准。
> **情绪驱动**：按情绪查配方 `emotion-arrangement-recipes.md`、按情绪查和弦 `emotion-chord-index.md`、钢琴/小提琴/手风琴写法 `core-instruments.md`。
> **标注**：【源】/【事实】= 可核实；【验】= 交叉验证；【经验】/【通用理论补充】= 惯例或未单条核实，可放心改。

---


> 面向对象：情绪驱动型编曲者。用户明确把**钢琴、小提琴、手风琴**定为「写宏大叙事和悲伤歌的主体乐器」。
> 本文只给参数级写法与情绪映射，**不写乐器介绍散文**。所有数值是起点不是法则，**以耳朵为准**。
> **边界**：只收经典/传统真实乐器编制（古典、管弦、室内乐、爵士、流行、民谣、中国风、影视配乐）。
> 合成器是合法音色来源（pad / bell / soft lead / 铺底）；不默认采用吵闹电子舞曲织体，见 `electronic-styles.md`。

## §0 口径、标注与引用约定

| 项 | 约定 |
|---|---|
| 音高口径 | **本文统一中央 C = C4 = MIDI 60 = 261.63 Hz**，A4 = 440 Hz |
| DAW 偏移 | Cubase / Ableton / Logic 把 MIDI 60 记作 **C3**；FL Studio 与部分软音源记作 **C5**，整体差一个八度；GM 标准多数叫 C4。跨 DAW 交换 MIDI 前，**先试听音源最低音验证口径**，别抄数值（【事】workflow.md §4.2、classic-arrangement.md §开头） |
| 【事】 | 有出处的事实：引自技能 references 文件或官网核实（核实日 2026-11-10） |
| 【经】 | 业界经验：数值为起点，需按曲风/音源试听微调 |
| 【补】 | 通用理论补充：跨来源综合、或因型号而异、无法核实到单一出处 |
| 引用文件 | `classic-arrangement.md`（音域/配器）、`instrument-libraries.md`（音源库）、`workflow.md`（MIDI 人性化/GM/CC）、`arrangement.md`（频率分工/声部）、`emotional-expression.md`（情绪字典）、`instrumental-production.md`（纯音乐让位） |
| 表格内分隔 | 单元格内并列值用 `｜` 或 `/` 分隔，不用裸竖线 |

**全文标注规则（区分事实与经验）**：音域数值、奏法的情绪指向、音源库规格、结构纪律、C3/C4/C5 口径、频率分工 → 【事】；
**§3 / §4 / §6 表格内的具体 velocity、CC 值、毫秒、detune 音分、混响 RT60 秒数、力度区间 → 一律为【经】业界经验起点**，未逐格重复标注；
手风琴音域因型号而异、织体模板、8 小节起伏表、类型对照 → 【补】/【经】。所有数值以耳朵为准。

---

## §1 实音音域、常用音区与记谱差异

### 1.1 音域总表

| 乐器 | 实音音域 | 常用音区 | MIDI 号 | 记谱 / 实音 | 出处 |
|---|---|---|---|---|---|
| 钢琴（88 键） | **A0–C8**（27.5–4186 Hz） | **C2–C6** | 21–108（常用 36–84） | 大谱表（高音+低音谱表），**实音=记谱，非移调** | 【事】classic-arrangement.md §2 |
| 小提琴 | **G3–E7**（196–2637 Hz，常用到 D7） | **G3–D7**（乐队常用 G3–A6） | 55–100（常用 55–98） | 高音谱表；定弦 **G3–D4–A4–E5 = 55/62/69/76**；**实音=记谱，非移调** | 【事】classic-arrangement.md §2 |
| 手风琴（钢琴式 41 键常见型） | 右手 **F3–A6**（174.6–1760 Hz）；左手 Stradella 低音约 **C2–B3** | 右手 **G3–C6**；旋律多在 C4–C6 | 右手 53–93；左手 36–59 | 右手实音=记谱；左手单键发单音/八度、和弦键一键发三音和弦；**型号差异极大**（48/60/72/96/120 bass、按钮式 bayan 右手更宽） | 【补】因型号而异，见 §8.3 |

> 三件套**都不是移调乐器**，别把低音提琴（实音低八度）、bB 单簧管（低大二度）、F 圆号（低纯五度）的口径带进来（【事】classic-arrangement.md §2）。
> 手风琴音域必须**以所用音源实测为准**，上表是常见型而非标准（【补】）。

### 1.2 各音区音色与情绪（低 / 中 / 高各一行）

| 乐器·音区 | 音名 / MIDI | 音色 | 情绪 |
|---|---|---|---|
| 钢琴 低 | A0–C2 / 21–36 | 浑厚、轰鸣、琴箱共振、泛音堆叠 | 庄严 / 威胁 / 送葬 / 宿命（【事】emotional-expression.md §3 低音区） |
| 钢琴 中 | C2–C5 / 36–72 | 最「说话」的叙事区、温暖、颗粒清晰 | 亲切 / 含蓄悲伤 / 独白（旋律+和声主战场） |
| 钢琴 高 | C5–C8 / 72–108 | 清亮、冷、脆弱、金属泛音 | 星光 / 疏离 / 宏大收尾光泽；硬击 2–4 kHz 易刺（【事】arrangement.md §3） |
| 小提琴 低 | G3–D4 / 55–62（G 弦） | 暗、厚、粗糙、男性化 | 隐忍 / 乡愁 / 克制悲伤 |
| 小提琴 中 | D4–A5 / 62–81 | 歌唱、最接近人声、热情 | 抒情 / 浪漫 / 叙事（【事】emotional-expression.md §6.1） |
| 小提琴 高 | A5–E7 / 81–100 | 尖锐、紧绷、悬置、脆弱 | 崩溃 / 恐惧（《惊魂记》式）/ 史诗顶点 |
| 手风琴 低 | 左手 bass C2–B3（16' 注册） | 风箱底气、心跳、行进感 | 沉重 / 送葬圆舞曲 / 史诗地基 |
| 手风琴 中 | 右手 F3–C5 / 53–72（8' 注册） | 簧片鼻音、人声感、市井 | 怀旧 / 叙事 / 孤独（右手旋律主战场） |
| 手风琴 高 | 右手 C5–A6 / 72–93（4' / musette） | 明亮、颤、刺、泛音多 | 巴黎 / 探戈 / 狂欢；也可做诡异疏离 |

---

## §2 奏法 / articulation 清单（每件 ≥8 种）

列含义：**触发或写法** = MIDI / keyswitch / CC / 力度上的落地手段。KS = keyswitch。

### 2.1 钢琴（10 种）

| 奏法 | 听感 | 情绪 | 适用段落 | 触发或写法 |
|---|---|---|---|---|
| Legato 连奏 | 音头软化、音间无缝 | 温柔 / 悲伤 / 歌唱性（【事】emotional-expression.md §3） | 抒情主题、主歌 | 前后音重叠 **10–30 ms**；vel 45–75；CC64 辅助连句 |
| Staccato 断奏 | 短、颗粒、干 | 紧张 / 轻快 / 愤怒（断奏比连奏更"恐惧"，Juslin 1997） | pre-chorus、ostinato | note length = 网格 **30–60%**；vel 80–110 |
| 延音踏板 sustain | 和声叠合、厅堂混响感 | 朦胧 / 宏大 / 怀旧 | 整段铺底 | **CC64 = 127** 踩下；换和弦前 **20–40 ms** 抬到 0、落下后 10–30 ms 踩回 |
| 半踏板 half-pedal | 半糊半清、泛音悬浮 | 含蓄悲伤 / 印象派 / 回忆 | 慢速抒情、桥段 | **CC64 = 20–90**（起点 60）；速度越慢越要勤换 |
| 弱音踏板 una corda | 变暗变柔、击槌触弦少 | 私密 / 脆弱 / 孤独 | 独奏开头、solo 段 | CC67（或音源专用）；NI UNA CORDA 库切 Felt 声库（【事】§8.2） |
| 琶音 / 分解和弦 | 流动、水波、推进 | 渴望 / 思念 / 叙事推进 | 伴奏层 | 和弦内音起音错开 **15–40 ms**（低音先落）；【事】workflow.md strum 5–30 ms |
| 震音 / 同音反复 tremolo | 颤动、逼近 | 悬疑 / 史诗铺垫 | pre-chorus 渐强 | 32 分音符交替；vel 每 2 小节 **60→110** 阶梯 |
| 泛音 / 预备泛音 | 金属泛音、空灵、非人间 | 疏离 / 回忆 / chills | 桥段、尾声 | 按下不发声的键（silent depression）再弹他键触发共振；或用 prepared piano（UNA CORDA Felt/Cotton） |
| 抓键 / 击槌噪声 | 机械、人味、在场感 | 亲密 / 真实（【事】emotional-expression.md §6.5） | 独奏、留白段 | 保留 noise 层：Salamander 琴弦共振 **CC20**、击槌 **CC21**、踏板噪声、release 采样（【事】instrument-libraries.md §3.1） |
| 八度 / 和弦硬击 | 重量、宣告、砸落 | 凯旋 / 崩溃 / 愤怒（felt=脆弱，硬击=愤怒） | 高潮、乐句落点 | vel **110–127**；低八度+高八度同发；起音错开 ≤10 ms 才"整" |

### 2.2 小提琴（12 种）

| 奏法 | 听感 | 情绪 | 适用段落 | 触发或写法 |
|---|---|---|---|---|
| Legato 连奏（true legato） | 无缝、歌唱 | 抒情 / 悲伤 / 浪漫 | 主题陈述 | KS 切 legato；叠加式引擎需音符**重叠 +10–30 ms** 触发过渡采样；CC11 画句弧 |
| Détaché 分弓 | 每音一弓、清晰颗粒 | 叙事 / 行走 / 坚定 | 主歌伴奏、对位 | 短音 KS；note length **80–95%**；vel 70–85 |
| Spiccato 跳弓 | 轻巧、弹跳 | 轻快 / 紧张 / 俏皮 | ostinato、快速音型 | 短音 KS；vel 70–100；note length 40–60% |
| Pizzicato 拨奏 | 点状、干、衰减快 | 俏皮 / 悬疑 / 不安（【事】emotional-expression.md §3） | 点缀、拨弦伴奏 | KS 切 pizz；注意左手 pizz 与右手拨弦分层 |
| Tremolo 震弓 | 抖动、逼近 | 悬疑 / 恐惧 / 史诗铺垫（【事】§6.1） | pre-chorus 渐强 | KS + 32 分重复；CC11 由 40→115 |
| Sul ponticello 靠琴马 | 金属、玻璃、冷 | 诡异 / 紧张 / 超现实 | 桥段、悬疑 | KS；常与 con sordino / harmonics 叠用 |
| Sul tasto / flautando 靠指板 | 笛状、空、柔 | 梦幻 / 疏离 / 回忆 | 氛围层 | KS；vel 压低 40–60 |
| Con sordino 弱音器 | 压抑、遥远、蒙纱 | 内敛悲伤 / 回忆（【事】§3 闷音=压抑遥远） | 主歌、主题变奏 | KS；高频衰减后可补 2–4 kHz 2 dB 防消失 |
| Harmonics 泛音（自然/人工 flageolet） | 银亮、空、非人间 | chills / 梦境 / 顶点 | 结尾、高潮前 | KS；高把位轻触弦；vel 45–60 |
| Portamento / glissando 滑音 | 抽泣、叹息、黏连 | 撕心裂肺 / 探戈式悲 | 乐句高点、上行跳进 | **CC64 触发 long portamento**（Chris Hein Solo Violin 明确用 CC64，【事】Sound On Sound 2026-11-10）；滑音时长 80–200 ms |
| Vibrato 揉弦宽度/速度 | 慢宽=温暖；快窄=紧张（【事】emotional-expression.md §3） | 情绪微调、揪心 | 长音、句尾 | **CC1 控 depth / speed**（Chris Hein 用 modwheel 控 speed/depth/intensity）；慢宽 ≈ 4–5 Hz / ±15 cent，快窄 ≈ 6–8 Hz / ±8 cent【经】 |
| Col legno / ricochet 弓杆击 | 干、骨感、机械 | 不安 / 仪式 / 超现实（【事】§6.1） | 特殊色彩段 | KS；短促、vel 60–85 |

### 2.3 手风琴（12 种）

| 奏法 | 听感 | 情绪 | 适用段落 | 触发或写法 |
|---|---|---|---|---|
| 风箱推/拉 push / pull | 换气、乐句呼吸、自然渐强渐弱 | 所有段落的「呼吸」 | 全曲 | **CC1 / CC11 画弧线**；每 **2–4 小节**换一次方向，换向处留 **30–80 ms** 气口（【经】，Ilya Efimov 明确 CC1 控动态、velocity 不控动态，【事】官网手册） |
| Bellows shake 抖风箱 | 颤抖、爆裂、逼近 | 探戈 / 紧张 / 悲恸 | 句尾、高潮 | KS 或 CC 触发；短促连续换向；**Accordions 2 提供 3 种 bellow shake**（【事】§8.2） |
| 8' / 16' / 4' 簧片注册 | 8'=基准（单簧中音）、16'=低八度（厚/地基）、4'=高八度（亮/穿透） | 切换注册 = 换角色 | 段落转换 | KS 切注册：Ilya Efimov 右手 **15 注册**、Pigini 音乐会手风琴 **15 注册**（【事】§8.2） |
| Musette 颤音（双/三簧 detune） | 巴黎、眩晕、甜中带苦 | 怀旧 / 香颂 / 圆舞曲 | 桥段、民谣 | 双簧 detune **±8–25 cent**【经】；Ilya Efimov Detune 开关 + KS、Accordions 2 单/双簧 Musette（【事】） |
| 左手 Stradella bass + 和弦键 | 低音 + 大三/小三/属七/减和弦一键三音 | 伴奏引擎 / 律动 | 全曲 | Ilya Efimov 和弦识别 + **Chord/Bass 与 Picking Mode**；Accordions 2 左手 **14 种预制节奏**（【事】） |
| 右手单音 / 柱式和弦触键 | 单音=线条，和弦=敲击块 | 叙事 / 宣示 | 旋律层 / 节奏层 | 右手 KS 或力度分层；柱式和弦起音错开 10–25 ms【经】 |
| 空气键 / 按键噪声 | 机械、人味、在场 | 亲密 / 真实 | 独奏、留白 | Ilya Efimov **Key Noise / Bellow / Release 可调**；Accordions 2 收录 key & button noises（【事】） |
| Staccato / Détaché 短触键 | 轻巧舞步、颗粒 | 圆舞曲 / 波尔卡 / 轻快 | 舞曲段 | 短音 KS；note length **40–60%**；vel 65–85 |
| Crescendo / Sforzato 渐强突强 | 逼近、爆发 | 撕扯 / 宣告 | pre-chorus、高潮 | Ilya Efimov 预备奏法 **Sustain / Staccato / Crescendo**；Bandoneon 带 threshold 的 **Sforzato**（【事】§8.2） |
| 重复音 repetition key | 同音反复、执念 | 追问 / 悬疑 | 固定音型 | Ilya Efimov Repetition key（KS B0 / B-1，【事】官网手册） |
| Vibrato 键 / 音高摇曳 | 激动、探戈式摇曳 | 悲恸 / 热切 | 长音句尾 | Ilya Efimov Vibrato key（【事】官网手册） |
| 左手节奏型 accompaniment | oom-pah-pah / 附点 habanera | 乡愁 / 行进 / 舞曲 | 全曲伴奏层 | 3/4 用 **Bass–Chord–Chord**；4/4 用 **Bass–Chord** 交替；换风箱方向对齐乐句 |

---

## §3 情绪映射表：音区 × 奏法 × 力度 → 情绪（21 行）

覆盖「悲伤（含蓄→崩溃）」与「宏大叙事/史诗」两端 + 中间态。vel = velocity；弦乐/手风琴动态同时看 CC1/CC11 弧线。

| # | 乐器 | 音区（音名/MIDI） | 奏法 | vel / 动态 | 情绪 | 段落 |
|---|---|---|---|---|---|---|
| 1 | 钢琴 | 中低 C3–C4 / 48–60 | Legato + una corda + 半踏板 | 40–55，CC64≈45 | **克制的悲伤 / 私语**（不是嚎啕） | intro、verse |
| 2 | 钢琴 | 中 C4–C5 / 60–72 | 分解琶音 + 半踏板 | 45–60，起音错开 20 ms | 思念 / 欲言又止 | verse |
| 3 | 钢琴 | 低 C2–C3 / 36–48 | 八度长音 + 全踏板 | 35–50 | 送葬 / 空洞 / 宿命 | intro |
| 4 | 小提琴 | 低 G3–D4 / 55–62 | con sordino + legato + 慢宽揉 | CC1 低，vel 45–60 | 隐忍 / 乡愁 | verse |
| 5 | 小提琴 | 中 D4–A4 / 62–69 | legato + 慢揉 + 下行句 | 50–70 | **含蓄悲伤 / 叹息**（乐句尾下行，【事】emotional-expression.md §7） | 主题 |
| 6 | 手风琴 | 中 F3–C5 / 53–72 | 8' 单簧 + 慢风箱 | CC11 40–60 | 怀旧 / 市井孤独 | verse |
| 7 | 手风琴 | 低 bass / 36–59 | 16' + oom-pah-pah 极轻 | 40–55 | 旧时光 / 葬礼圆舞曲 | intro |
| 8 | 钢琴 | 中 C4–C5 / 60–72 | Staccato 断奏 | 75–90 | 叙事 / 行走 / 清醒 | verse |
| 9 | 钢琴 | 中高 C5–C6 / 72–84 | 琶音 + 踏板渐深 | 65–85 | 渴望 / 涌动 | pre-chorus |
| 10 | 小提琴 | 中 A4–E5 / 69–76 | Détaché 分弓 | 70–85 | 温暖叙事 / 坚定 | verse |
| 11 | 小提琴 | 中 D4–A5 / 62–81 | legato + 揉弦渐快渐宽 + cresc | 60→100 | 揪心 / 期待（延迟解决） | pre-chorus |
| 12 | 手风琴 | 中高 C5–A6 / 72–93 | musette detune + 圆舞曲 | 60–80 | 苦涩的甜 / 巴黎回忆 | bridge |
| 13 | 手风琴 | 中 F3–C5 / 53–72 | 8'+4' 柱式和弦 + 轻 bellows shake | 70→90 | 不安 / 暗涌 | pre-chorus |
| 14 | 钢琴 | 全音区 A0–C8 | 八度 + 柱式和弦 + 全踏板 | 110–127 | **宣告 / 凯旋 / Triumph** | chorus / climax |
| 15 | 钢琴 | 低 C2 + 高 C6 | 八度长音 + 高音 tremolo | 90→120 渐强 | **史诗铺底 / 逼近** | pre-chorus |
| 16 | 小提琴 | 高 D5–E7 / 74–100 | tremolo / sul ponticello + 齐奏 | 100–120 | **恐惧 / 史诗顶点** | climax |
| 17 | 小提琴 | 高 A5–E7 / 81–100 | legato 上跳八度 + 宽揉 | 100–120 | **Triumph / chills**（音区突跳，【事】emotional-expression.md §2.4） | final chorus |
| 18 | 钢琴 | 低+中高全音区 | 不协和硬击 + 踏板全踩 | 120–127 | **崩溃 / 失控** | climax-break |
| 19 | 小提琴 | 高 A5–E7 / 81–100 | sul ponticello + 快窄揉 + ff | 105–127 | 歇斯底里 / 惊悚 | climax |
| 20 | 手风琴 | 全音域 | 16'+8'+4' 全注册 + shake + sforzato | 95–120 | **悲恸 / 撕扯** | climax |
| 21 | 手风琴 | 高 C5–A6 / 72–93 | 4' piccolo 单音 + 键噪 | 30–45 | 虚空 / 事后余烬 | outro |

---

## §4 可直接抄的织体模板

「撑几小节」= 在不加新元素、只做微调的前提下不腻的时长（【经】，依据 arrangement.md「每 8 小节必须变一件事」）。

### 4.1 钢琴（5 个）

| 编号 | 拍号 / BPM | 每小节音符 | 和弦 / 音型 | 左右手分工 | velocity 曲线 | 踏板 | 情绪·段落 | 撑几小节 |
|---|---|---|---|---|---|---|---|---|
| P1 独白 | 4/4 · 60–70 | 4–6 | i–♭VI–♭III–♭VII 分解（如 C–Eb–G–Bb） | 左手根音八度 C2/C3 + 右手 4 音分解 | 起 48 → 句尾 40，重拍 +10 | CC64 每和弦换踩（抬 20 ms 再踩），una corda 常开 | 含蓄悲伤·intro/verse | **8**（第 5 小节换一次转位） |
| P2 赞美诗柱式 | 4/4 · 72–84 | 4 和弦 | I–V–vi–IV 四声部柱式 | 左手五度/八度 + 右手三和弦转位 | 60→72→68→80 | CC64 每小节换，半踏板 60 | 温暖叙事·verse | **8** |
| P3 阿尔贝提变体 | 3/4 或 6/8 · 76–90 | 6 | 分解 low–mid–high–mid | 左手单音 + 右手 3 音 | 55/62/68/62 循环，句尾 +8 | 轻踏板 CC64 30–50 | 渴望·pre-chorus | **4–8** |
| P4 八度宣叙 | 4/4 · 90–110 | 8–16 | 旋律八度叠 + 左手震音 | 左右手八度齐奏 | 90→120，每 2 小节 +8 | CC64 127 全踩 | 史诗·chorus/climax | **4**（必须带渐强） |
| P5 悬置留白 | rubato | 1–2 | 单音 + 预备泛音 | 右手单音 + silent-key 共振 | 30–45 | 半踏板 45 + 保留 release 尾音 | 孤独/余韵·outro | **8–16**（靠稀疏事件） |

### 4.2 小提琴（5 个）

| 编号 | 拍号 / BPM | 每小节音符 | 和弦 / 音型 | 声部分工 | velocity 曲线 | legato / 弓法 | 情绪·段落 | 撑几小节 |
|---|---|---|---|---|---|---|---|---|
| V1 长线条主题 | 4/4 · 66–76 | 2–4 长音 | 级进下行小调句 | solo legato + 钢琴/手风琴长音和声垫 | CC1 40→75 画弧，vel 55–70 | true legato 重叠 +10–20 ms，慢宽揉 | 含蓄悲伤·主题陈述 | **8** |
| V2 分弓叙事 | 4/4 · 92–104 | 8 个八分 | 和弦音分解 | détaché 每音一弓 + 钢琴断奏 | 70→85 阶梯 | 短音 KS，不用 legato | 叙事推进·verse | **8** |
| V3 跳弓 ostinato | 4/4 · 108–120 | 16 个十六分 | 同音/邻音交替 | spiccato + 手风琴 bass pulse | 75 恒定 ±8，每 4 小节 +10 | 短音 KS | 逼近·pre-chorus | **8**（靠渐强） |
| V4 震弓渐强 | 4/4 · 100–120 | tremolo 32 分 | 属持续音 pedal point | tremolo + 钢琴八度渐强 | vel 60→115，CC11 同步 | KS + 全奏 hit 收 | 史诗铺垫·pre-chorus | **4–8** |
| V5 高把位色彩 | 自由 | 1–2 长音 | 高把位 E6–E7 | harmonics / sul ponticello + con sordino | 45–60，CC1 慢 | 长音 + 长混响 | 恐惧/虚空·bridge/outro | **4–8** |

### 4.3 手风琴（5 个）

| 编号 | 拍号 / BPM | 每小节音符 | 和弦 / 音型 | 左右手分工 | velocity 曲线 | 风箱 / 注册 | 情绪·段落 | 撑几小节 |
|---|---|---|---|---|---|---|---|---|
| A1 圆舞曲 | 3/4 · 84–96 | 3 组 | I–V–I | 左手 Bass–Chord–Chord + 右手 8' 单音旋律 | 低音 70 / 和弦 50 | 8' 单簧；每 2 小节换向 push→pull | 怀旧/乡愁·verse | **8** |
| A2 民谣分解 | 4/4 · 72–88 | 8 | i–♭VII–♭VI–V | 左手单 bass 走动 + 右手 8' 三音分解 | 55→68 | 慢推 4 小节，换向留 60 ms 气口 | 叙事·verse | **8** |
| A3 探戈 bandoneon 式 | 4/4 或 2/4 · 116–126 | habanera 附点 | Am–Dm–E7 | 左手 sforzato bass + 右手 8'+4' 柱式和弦 | 80→115 | 句尾 bellows shake + sforzato | 撕扯/悲恸·climax | **4–8** |
| A4 musette 华尔兹 | 3/4 · 100–120 | 3 组 | 大调 I–IV–V | 右手双簧 musette（detune ±15 cent）旋律 + 左手 oom-pah-pah | 65–80 | 风箱均匀 + 轻 vibrato key | 苦涩的甜/巴黎·bridge | **8** |
| A5 全注册史诗垫 | 4/4 · 90–110 | 2–4 长和弦 | i–♭VI–♭III–♭VII | 16'+8'+4' 全开 + 左手 bass 长音 | CC11 40→100 渐强 | 每 2 小节一次 bellows shake | 宏大/悲壮·climax | **4**（须换层） |

---

## §5 MIDI 制作参数（数值起点，以耳朵为准）

| 项目 | 数值 / 做法 | 依据 |
|---|---|---|
| velocity 档位 | pp 20–40 / p 40–55 / mp 55–70 / mf 70–85 / f 85–105 / ff 105–127 | 【经】对应 emotional-expression.md §3 动态 |
| velocity 浮动 | 围绕基准 **±10–20**；重拍（1、3）比弱拍（2、4）高 **10–15**；**画弧线**不平铺（平铺只触发同一采样层） | 【事】workflow.md §4.1 |
| 和弦起音错开 | 通用 strum **5–30 ms**；钢琴琶音 15–40 ms；手风琴左右手 10–25 ms；低音先落、高音后落 | 【事】workflow.md §4.1 +【经】 |
| timing humanize | 个别音符 **±5–15 ticks**（PPQN=960 约几毫秒）；钢琴/弦乐 ±8–25 ms；主旋律可整体 laid-back 后移 10–30 ms；**低音/骨架对齐网格** | 【事】workflow.md §4.1 +【经】 |
| 量化 | 骨架 1/16；和弦/弦乐 **50–80%** 部分量化；主旋律不量化 | 【事】workflow.md §4.1.3 |
| **CC64 延音踏板** | 全踩 **127** / 全放 **0**；**半踏板 20–90**（起点 60）；换和弦：新和弦落下前 **20–40 ms** 抬到 0，落下后 **10–30 ms** 踩回 127；慢速每和弦换，快段每 1–2 小节换。**禁止整曲 127 不抬** | 【经】+【事】instrument-libraries.md §0（先查库是否支持 CC64） |
| CC1 调制 | 弦乐 vibrato depth/速度；**手风琴风箱气压/动态**（Ilya Efimov 明确 CC1 控动态、velocity 不控动态） | 【事】Efimov 官网手册 2026-11-10 |
| CC11 表情 | 弦乐/手风琴长音渐强渐弱的**主控制器**，常态 80–100，渐强 40→115；**优先于 CC7 画表情线** | 【事】instrument-libraries.md §6 |
| CC7 音量 | 只做静态电平/整轨平衡，**别用来画表情**（会与 CC11 打架） | 【经】 |
| 钢琴辅助 CC | CC67 弱音踏板；Salamander 琴弦共振 **CC20**、击槌噪声 **CC21**；另有踏板噪声 / release 采样 | 【事】instrument-libraries.md §3.1、workflow.md §4.2 |
| articulation / KS | KS 写在目标音符前 **20–60 ms**（别同 tick）；同音区多声部靠不同 KS + 不同触键区分 | 【事】classic-arrangement.md 音区让位条 |
| legato 重叠量 | 叠加式 true legato 前后音重叠 **0 到 +10–30 ms** 触发过渡采样；CSS 有 **60–300 ms** 延迟，需把该轨 MIDI 整体前移 | 【经】+【事】instrument-libraries.md §3.2 CSS 行 |
| release 尾音 | 换和弦/换音色保留 **80–200 ms** release，别硬切；同音区两件乐器尾音错开衰减 | 【经】 |
| 避免机械感 | 破「三宗罪」：等力度 / 卡网格 / 和弦同起音；再加：力度弧线、RR 轮询、乐句气口、键噪/呼吸噪声层、人手声部微走音 **±3–6 cent** | 【事】workflow.md §4.1.5 +【经】 |

---

## §6 宏大叙事 vs 悲伤：两套完整配置对照表

### 6.1 配置 A —— 悲伤（含蓄 → 崩溃）

| 乐器 | 音区 | 织体 | 力度 vel | 奏法 | 踏板 / 风箱 | 层次 | 混响 RT60 | 常见坑 |
|---|---|---|---|---|---|---|---|---|
| 钢琴 | 中低 C2–C5 / 36–72 | 独奏 + 稀疏分解，留白多 | 35–60 | legato + una corda + 半踏板 | CC64 40–70 半踏板、每和弦换踩 | 1–2 层 | **1.2–1.8 s** 小房间 | 踏板不抬糊成团；低音区密集和弦发闷；力度全 64 无动态 |
| 小提琴 | 低中 G3–A5 / 55–81 | 单线条 + 极轻和声垫 | 45–70 | con sordino + legato + 慢宽揉 + 下行句 | 长音重叠 +10–20 ms | 1 主 + 1 垫 | **1.5–2.2 s** | 揉弦过快=紧张不是悲伤；高音区刺耳；乐句无气口 |
| 手风琴 | 中 F3–C5 / 53–72（8'） | oom-pah-pah 极轻 | 40–65 | 8' 单簧 + 慢风箱 + 长音 | 慢推每 4 小节换向、留 60 ms 气口 | 右手旋律 + 左手 bass 两层 | **1.0–1.6 s** | musette 全开=甜腻破坏悲伤；换向无气口；bass 与钢琴左手抢 60–120 Hz |

### 6.2 配置 B —— 宏大叙事 / 史诗

| 乐器 | 音区 | 织体 | 力度 vel | 奏法 | 踏板 / 风箱 | 层次 | 混响 RT60 | 常见坑 |
|---|---|---|---|---|---|---|---|---|
| 钢琴 | 全音区 A0–C8 | 八度 + 柱式和弦 + 琶音 | 90–127 | 八度硬击 + tremolo + 全踏板 | CC64 127 全踩、每 1–2 小节换 | 3–4 层，满编 ≤ 全曲 40% | **2.0–3.0 s** 厅堂 | 低音八度与 bass 撞 60–120 Hz；全踏板不换踩变糊；2–4 kHz harsh |
| 小提琴 | 中高 A4–E7 / 69–100 | 齐奏 tremolo + 八度旋律 | 95–120 | tremolo / sul ponticello / 宽揉上跳八度 | true legato + 分奏 | 3 层以上（一提/二提/独奏叠） | **2.2–3.2 s** | 高音区持续 ff 听觉疲劳；人少却要"大"→ 叠轨/ensemble；CSS 延迟未前移 |
| 手风琴 | 全音域 16'+8'+4' | 全注册柱式和弦 + sforzato | 85–120 | 全注册 + bellows shake + crescendo | 风箱满推 + 抖风箱 + sforzato | 3 层（bass/和弦/旋律）+ 与小提琴分层 | **2.0–2.8 s** | 全注册中频糊、频率打架；风箱方向不变无起伏；与钢琴抢 200–800 Hz |

> 结构纪律：高潮（最大密度+最高音区+最响）**全曲只出现一次**；高潮前 **4–8 小节先减层**（撤 bass/鼓），否则「大」不起来（【事】emotional-expression.md §4.5 / §5.2、arrangement.md §1）。

---

## §7 三件乐器的组合与让位

### 7.1 频率主战场（Hz）

| 层 | Hz 区间 | 谁占 | 内容与纪律 |
|---|---|---|---|
| 地基 | **20–120** | 钢琴左手低音 A0–C2（27.5–65 Hz）+ 手风琴 16' bass | 只有这两者；其余全部 HPF；**120 Hz 以下保持 mono**（【事】arrangement.md §3/§4.4） |
| 低中 body | **120–250** | 钢琴琴箱 + 手风琴 8' 左手 | 200–500 Hz 是 mud 警戒区，谨慎提升（【事】arrangement.md §3） |
| 中频和声 | **200–800** | 钢琴右手和弦、手风琴右手和弦键、小提琴 G/D 弦 | 最拥挤的一层，**必须让位**（【事】classic-arrangement.md 频段让位表） |
| 中高 presence | **800 Hz–4 kHz** | 小提琴旋律（presence 1–4 kHz）+ 钢琴高音旋律 + 手风琴 4' | 纯音乐无歌词时，**指定一件乐器当「临时主唱」独占此段**（【事】instrumental-production.md §5.1） |
| 高频光泽 | **4–8 kHz** | 小提琴泛音/弓噪、钢琴击槌与高音泛音、手风琴 musette 颤音与键噪 | 8–12 kHz 轻提加 air；只做点缀不持续 |

### 7.2 谁拿旋律 / 和声 / 低音

| 配置 | 旋律（临时主唱） | 和声 | 低音 | 备注 |
|---|---|---|---|---|
| 抒情 / 悲伤 | **小提琴**（中音区 legato） | 钢琴分解和弦 + 手风琴 8' 长音 | 钢琴左手八度 | 手风琴可休止，只留怀旧点缀 |
| 宏大 / 史诗 | **小提琴高音区 + 齐奏**，或钢琴八度旋律 | 手风琴全注册柱式和弦 + 钢琴柱式 | 钢琴左手八度 + 手风琴 16' bass（二选一为主） | 三者齐奏时按 §7.4 分层 |
| 民谣 / 叙事 | **手风琴**（8' 或 musette 单音旋律） | 钢琴分解和弦 | 手风琴 Stradella bass | 小提琴做对位副旋律或长音垫 |
| 硬规则 | 同一时刻 **800 Hz–4 kHz 只有一件**当主唱，其余让位 | — | — | 【事】instrumental-production.md §5.1 |

### 7.3 同音区重叠怎么处理

| 手法 | 做法 | 依据 |
|---|---|---|
| 音区分离 | 相邻声部**至少隔一个八度**；低音/和声/旋律各占一个八度带；低音区间距可大、高音区收窄 | 【事】arrangement.md §4.1 / §4.6 |
| 动态避让 | 长音「定住」和声、短音出颗粒；两长音并用时**主奏强奏、背景自动降动态**；弦乐拉长音 + 钢琴轻断奏 = 动静结合 | 【事】classic-arrangement.md 四类打架维度 |
| 奏法 / 触键错开 | 钢琴断奏 + 小提琴 legato + 手风琴长音；音区间隔小、音色接近时靠**不同触键**区分声部 | 【事】classic-arrangement.md 音区让位条 |
| 声像避让 | 钢琴略左 / 手风琴略右 / 小提琴居中或按舞台摆位（一提左、大提右），收窄避免过偏 | 【事】classic-arrangement.md §3 |
| 频谱避让 | 伴奏钢琴 HPF **85→240 Hz**、旋律钢琴 **180 Hz**；副歌把 1–2 kHz 挖 **2–3 dB / Q=1.0** 给主唱让位 | 【事】instrument-libraries.md §6、arrangement.md §2 |

### 7.4 三者齐奏分几层

```
第 1 层 低频 <200 Hz   ：钢琴左手八度 + 手风琴 16' bass（二选一为主，另一让）→ 120 Hz 以下 mono
第 2 层 和声 200–800 Hz：钢琴右手柱式/分解 + 手风琴 8' 和弦键（错开八度）
第 3 层 旋律 800Hz–4kHz：小提琴（或钢琴/手风琴高音区）独占，只有一件
第 4 层 光泽 >4 kHz    ：小提琴泛音、钢琴高音泛音、手风琴 4'/键噪（点缀，不持续）
```
> 和声不超过 4 声部；pad 超过 5 音易浑浊，2–3 音更通透（【事】arrangement.md §4.3）。

### 7.5 不加新乐器，做出 8 小节起伏

| 小节 | 钢琴 | 小提琴 | 手风琴 | 能量(1–10) | 可听事件 |
|---|---|---|---|---|---|
| 1–2 | 稀疏分解 vel 40 | 休止 | 8' 长音 vel 45 | 2 | 立情绪、留白 |
| 3–4 | 加转位 + 半踏板 | con sordino 长音进入 | oom-pah-pah 轻 | 4 | **新音色进入**（段落信号） |
| 5–6 | 八度叠加 vel 70 | détaché 分弓 | 换 8'+4' 注册 | 6 | **音区上移 + 注册切换** |
| 7 | 抽左手、只留高音 tremolo | 上跳八度 | 风箱满推 + shake | 8 | 音区跳变 + 渐强顶点（chills 点） |
| 8 | 全奏 hit vel 120 | ff 宽揉 | 全注册 sforzato | 10 → 骤停 | **全停 1 拍再收**（沉默是乐器，【事】emotional-expression.md §5.3） |

> 依据：每 8 小节必须改变一件明确的事；相邻段落能量必须不同；高潮前减层；高潮只一次（【事】arrangement.md §1、emotional-expression.md §5.2）。

---

## §8 音源落地

### 8.1 引用 `instrument-libraries.md` 已有的库

| 类别 | 库名 | 免费/付费 | 播放器 | 关键 articulation / CC | 本文用途 |
|---|---|---|---|---|---|
| 钢琴 | Salamander Grand Piano V3 | 免费（CC-BY 3.0） | sfizz / sforzando | 88 键 × **16 力度层**；CC64 踏板 + 踏板噪声；共振 CC20；击槌 CC21；release 采样 | §5 全套 MIDI 参数、§2.1 噪声/半踏板 |
| 钢琴 | Spitfire LABS Soft / Felt / Intimate Grand | 免费 | Spitfire 自有 | 少数奏法、少动态层 | 草图 / felt 氛围铺垫 |
| 钢琴 | NI Noire | 付费 | **完整 Kontakt** | Pure / Felt 两套真实录音；弱奏细腻 | 影视/新古典含蓄悲伤 |
| 钢琴 | Modartt Pianoteq 8 | 付费（约 60 MB） | 自有插件 | 物理建模（模拟真实三角钢琴，非合成器音色设计）；麦位自由度极高 | 低配机、精确麦位 |
| 钢琴 | Garritan Abbey Road CFX / Synthogy Ivory II | 付费 | 各自 | 多麦位、多力度层 | 暴露的古典独奏 |
| 弦乐 | Spitfire LABS Strings | 免费 | Spitfire 自有 | 14 人合奏，Short / Ensemble / Long 3 奏法 | 亲密干声铺底 |
| 弦乐 | BBCSO Discover | 免费 | Spitfire 自有（免 Kontakt） | **35 乐器 / 47 技法**，含完整弦乐 legato / long / short | 免费入门、学习配器 |
| 弦乐 | Cinematic Studio Strings（CSS） | 付费（$399） | 完整 Kontakt 6+ | 60 人 **Auto Legato**、真实 vibrato；**60–300 ms 延迟需前移 MIDI** | 抒情大旋律 / 影视 |
| 弦乐 | NI Stradivari Violin / Impact Soundworks Stroh Violin | 付费 | Kontakt | Stroh 含 pizz / spiccato / legato | 独奏旋律、民谣/室内乐 |
| 弦乐 | Strezov Minimalist Violins Legato Freebie | 免费 | Kontakt 7+ | 1 个高质量小提琴 legato；CC64 切分奏 | 「需要一条像样的小提琴旋律线」 |

### 8.2 本次补充的 4 个真实库（钢琴 / 弦乐 / 手风琴各覆盖，手风琴为重点）

> 均为 2026-11-10 官网/三方核实存在；**不写死价格**，只标免费/付费与区间参考。

| 类别 | 库名 | 免费/付费 | 播放器 | 关键 articulation / 控制 | 本次价值 |
|---|---|---|---|---|---|
| 钢琴 | **Native Instruments UNA CORDA** | 付费（价格以官网为准） | **免费 Kontakt Player 或完整 Kontakt 均可** | David Klavins × Nils Frahm 定制立式、**每键单弦**；纯 / Felt / Cotton 三声库；织物 / 机械 / **踏板** / 房间噪声可调；velocity 曲线与 **pedal mode** 可调；10 GB / 100 snapshots / 3 NKI | 直接对应 §2.1 的 una corda 弱音踏板、felt/预备泛音、抓键噪声 |
| 弦乐 | **Best Service Chris Hein Solo Violin** | 付费（约 $179 区间，不写死） | **免费 Kontakt Player 5.6.8+** | **12 种短音 note heads** + spiccato；真 legato 三模式（short / **CC64 触发 long portamento** / glide）；**CC1 控 vibrato speed·depth·intensity**；tremolo / pizzicato / **ponticello** / **flautando** / **harmonics(flageolet)** / col legno / ricochet / falls / doits / runs / gliss；6 动态层 phase-align；KS + hot key；2.73 GB（EXtended 9.4 GB / 38 奏法） | 把 §2.2 的 12 种小提琴奏法一次性配齐 |
| 手风琴 | **Ilya Efimov Accordion**（钢琴式/键盘手风琴） | 付费 | **必须完整 Kontakt 7.10+，免费 Player 不可用** | 右手 **15 注册**（piccolo / bassoon / clarinet / musette…）+ 左手 2 注册；**CC1 控动态（velocity 不控动态）**；CC21 / Auto attack；**Detune（musette）+ KS**；Key Noise / Bellow / Release；RR ×3；Sustain / Staccato / Crescendo；**和弦识别 + Chord/Bass 与 Picking Mode**；Repetition / Vibrato key；左右手分离/合并 3 patch；1.7 GB / 2288 samples | 钢琴式手风琴的注册、风箱、musette detune、Stradella 左手完整建模 |
| 手风琴 | **Best Service Accordions 2（Eduardo Tarilonte）** | 付费（再版 Collection 曾报 €/$199，仅作区间） | Kontakt Player 5.71+ 或新版 **Engine Player** | 13→10 件乐器：**Accordion（11 注册）/ Bandoneon（Alfred Arnold 探戈，含 Sforzato）/ Concert Accordion（Pigini，15 注册）/ French Musette / Folk（Mengascini）/ Steirisches / Concertina / Bass Accordion / Wooden Melodica / Folk Melodeon**；**3 动态层 × 3 RR**、**3 种 Bellow Shake**、key & button noises、左手 **14 种节奏伴奏**、U47 录音、8000+ samples | 一次覆盖 musette / bandoneon / 音乐会 / 民谣 / 低音手风琴全类型 |

### 8.3 手风琴四种类型对照（务必区分，别混用）

| 类型 | 键盘 / 按钮 | 簧片与注册 | 常见音域 | 性格 / 情绪 | 典型曲风 | 对应真实库 |
|---|---|---|---|---|---|---|
| **钢琴式手风琴 Piano accordion** | 右手钢琴键盘 + 左手 Stradella 键钮 | 8' / 16' / 4'，可带 musette | 右手 F3–A6 | 通用、叙事、怀旧 | 民谣 / 流行 / 影视 | Ilya Efimov Accordion；Accordions 2 的 Accordion / Concert |
| **Musette（法式）** | 钢琴式或按钮式 | 双/三中簧 **detune ±8–25 cent** | 中高音区 | 颤、甜中带苦、眩晕 | 巴黎香颂 / 圆舞曲 | Accordions 2「French Musette」/ 单/双簧 Musette；Ilya Efimov 的 Detune |
| **Bandoneon（班多钮）** | 全按钮、**无 Stradella 和弦键**、推拉异音 bisonoric | 双簧为主 | 中音区 | 暗、撕扯、呼吸感 | 探戈 / 皮亚佐拉 | Accordions 2「Bandoneon」（含 Sforzato） |
| **Bayan（巴扬 / 俄式按钮）** | 右手全按钮半音阶、左手 Stradella / 自由低音 | **4 簧 15 注册**、低音厚 | 右手更宽 | 深沉、宏大、东欧 | 古典 / 东欧 / 史诗 | **Ilya Efimov Bayan**（独立库：2526 samples / 2.1 GB / 15 注册 / Staccato·Crescendo·Détaché / 需完整 Kontakt） |

### 8.4 关键 articulation 齐备性核对

| 需求 | 免费方案 | 付费方案 | 结论 |
|---|---|---|---|
| 钢琴 半踏板 / una corda / 噪声层 | Salamander（CC64 + CC20/21 + release） | UNA CORDA、Noire Felt | 免费已基本齐 |
| 小提琴 12 奏法 + 真 legato + CC1 揉弦 | BBCSO Discover（基础 long/short/legato） | Chris Hein Solo Violin、CSS | 深度要付费才齐 |
| 手风琴 注册 / musette / bellows shake / Stradella 左手 | **基本缺失**（LABS 等免费库未覆盖） | Ilya Efimov Accordion + Accordions 2 | **免费三件套的最大缺口**，须单独补 |
| 播放器 | 先定播放器再买库：**Kontakt Player 只认 Player-compatible 库**；完整 Kontakt 库用免费 Player 打开会 **15 分钟演示锁**（【事】instrument-libraries.md §0、§7） | — | 买前必查 |

---

## §9 B 站可核实素材（真实 BV 号）

来源标注：`verified_bv.json` = 已二次核实；`bili_search_raw.json` = 原始检索数据中的真实编号（未二次核实，按来源标注）。**无对应素材处一律写「通用理论补充」，不编造编号。**

| 主题 | BV 号 | 来源 | 对应本文 |
|---|---|---|---|
| 流行乐器法大全（乐器法） | BV17g411t7Yj | verified_bv.json | §1 / §2 |
| 交响乐队乐器法与编配基础·川音 | BV13341147KF | verified_bv.json | §1 / §7 |
| 实用配器法指南（Jaky） | BV1Ag4y167zM | verified_bv.json | §7 |
| 100 个管弦乐编配技巧 | BV1cL4y1x74c | verified_bv.json | §7 |
| 阿德勒《配器法》教程 CD1 | BV1ys411g7Zi | verified_bv.json | §1 / §7 |
| 流行弦乐编写·超完整工程分享 | BV1mY41117b5 | verified_bv.json | §4.2 / §5 |
| 弦乐如何编写 | BV1jx411R7fG | verified_bv.json | §4.2 |
| 流行弦乐基本四重奏教学 | BV1sz42187Ui | verified_bv.json | §7 |
| 从零制作史诗级战斗管弦乐 | BV1pp4y1W73j | verified_bv.json | §6.2 |
| Lass 弦乐全套教程（1–3 代） | BV1jH4y137Bv | verified_bv.json | §8 |
| 同一个旋律·上百种编曲配器技巧 | BV1xutUeuExf | verified_bv.json | §4 / §7 |
| 编曲音源使用大全 | BV16S4y1g7CH | verified_bv.json | §8 |
| 影视配乐总谱分析合集 | BV1hh41167kq | verified_bv.json | §6 / §7 |
| 对位法在流行弦乐中的应用 | BV1QK411u7aM | verified_bv.json | §7 |
| 这弦乐绝了！钢琴与弦乐的温柔对话 | BV1GF411p7kB | bili_search_raw.json | §7 组合让位 |
| 钢琴音色哪家强？7 款原声钢琴音色对比 | BV1WN411i7Ps | bili_search_raw.json | §8 |
| 钢琴音源大乱斗！17 台钢琴 | BV1k1421C7HU | bili_search_raw.json | §8 |
| 基本乐理第 17 讲·装饰音/颤音演奏法 | BV15g411A7rF | bili_search_raw.json | §2 颤音/震音 |
| 杨立青《管弦乐配器教程》谱例+音频 | BV1zP4y1x7ra | bili_search_raw.json | §1 / §7 |
| 拍频是什么？配器必懂的声学现象（揉弦/起音先后/弦乐厚度） | BV1BxW36tEBz | bili_search_raw.json | §5 humanize / §7 |

> 三件乐器**专门的参数级写法**（半踏板 CC 数值、风箱换向毫秒、注册切换、musette detune 音分、逐奏法 velocity）在上述视频中未系统覆盖，属**通用理论补充 + 业界经验**，已用【经】【补】标注，不冒充视频结论。

---

## §10 自检清单与常见坑

**自检（写完逐条过）**
- [ ] 三件乐器有没有挤在同一音区？相邻声部是否至少隔一个八度？
- [ ] 800 Hz–4 kHz 是否只有一件在当「临时主唱」？
- [ ] 60–120 Hz 是否只有钢琴左手 / 手风琴 16' bass 在占？120 Hz 以下是否 mono？
- [ ] CC64 有没有整曲 127 不抬？换和弦有没有「抬—落—踩」？
- [ ] CC11 表情线画了吗（不是只画 CC7）？弦乐/手风琴有没有渐强弧线？
- [ ] 手风琴风箱每 2–4 小节换向、换向留 30–80 ms 气口了吗？
- [ ] 每 8 小节有没有改变一件明确的事？高潮是否只出现一次、前面是否减层？
- [ ] 关键 articulation 在所选音源里是否真的存在（KS 键位 / 是否需要完整 Kontakt）？

**常见坑**
1. 力度全 100 / 全 127 → 音源只触发同一采样层，动态扁平（【事】workflow.md §4.3）。
2. 所有和弦同一起音 → 机器感；用 5–30 ms strum 错开（【事】workflow.md §4.1.5）。
3. 延音踏板一踩到底 → 和弦叠成糊；半踏板与换踩是「悲而不浑」的关键。
4. 手风琴 musette 全开做悲伤 → 甜腻破坏情绪；悲伤用 8' 单簧。
5. 三者齐奏全注册 + 满编 → 200–800 Hz 中频糊；靠音区/动态/奏法/声像四法让位。
6. 小提琴高音区持续 ff → 疲劳；「大」来自**前面减层的对比**而非一直响。
7. 完整 Kontakt 库用免费 Player 打开 → 15 分钟演示锁；买前先查播放器（【事】instrument-libraries.md §0）。
8. CSS 等 legato 库 60–300 ms 延迟未前移 MIDI → 旋律整体拖拍（【事】instrument-libraries.md §3.2）。
9. 跨 DAW 交换 MIDI 没核对 C3/C4/C5 口径 → 整体差一个八度（【事】workflow.md §4.2）。
10. 追求「参数正确」而忽略耳朵 —— **参数表只是地图，耳朵是唯一裁判**（【事】emotional-expression.md §9.8）。

---

## 附：本文引用文件与章节对应

| 文件 | 用于本文 |
|---|---|
| `classic-arrangement.md` | §1 音域总表 / §7 声部与频段让位 / §9 BV 素材 |
| `instrument-libraries.md` | §5 CC/播放器 / §8 已有音源库 / §10 坑 |
| `workflow.md` | §0 C3/C4/C5 口径 / §5 velocity·humanize·CC·GM |
| `arrangement.md` | §1 音区情绪 / §5 结构纪律 / §6 满编占比 / §7 频率分工与声部规则 |
| `emotional-expression.md` | §1 音区与奏法情绪 / §3 情绪配方 / §6 动态·混响·高潮稀缺性 |
| `instrumental-production.md` | §7 无歌词时「临时主唱」与 800 Hz–4 kHz 优先权 |
| `verified_bv.json` / `bili_search_raw.json` | §9 真实 BV 号 |
