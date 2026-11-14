# 真实乐器音源与采样库

> **来源**：B 站公开教程 / 专栏 / 测评整理（采集 2026-11-11，973 条去重视频、8 个课程视频下载抽帧）。逐条来源见文末「来源索引」，学习清单见 `bilibili-study-map.md`。
> **制作口径**：默认在 DAW 里作曲编曲（MIDI + 采样音源 + 合成器 + 自动化 + 混音）；真实乐器、采样、合成器音色都是合法音色来源，不做「原声 vs 电子」的出身审查。
> **范围分流**：不默认做吵闹的电子舞曲风格（EDM / House / Techno / Trap / Dubstep / 鼓机 drop / riser / 泵感侧链 / supersaw lead），这类内容单独收在 `references/electronic-styles.md`，主线不混。
> **主用途**：情绪驱动 + 场景感双轴 + 钢琴 / 小提琴 / 手风琴三件套；合成器在这里是色彩与空间层（pad / bell / soft lead / 铺底），不是舞曲骨架。
> **用法**：数值是起点不是法则，以耳朵为准；与本技能既有硬规则冲突时，以技能规则为准。
> **情绪驱动**：按情绪查配方 `emotion-arrangement-recipes.md`、按情绪查和弦 `emotion-chord-index.md`、钢琴/小提琴/手风琴写法 `core-instruments.md`。
> **标注**：【源】/【事实】= 可核实；【验】= 交叉验证；【经验】/【通用理论补充】= 惯例或未单条核实，可放心改。

---


> 服务场景：古典、管弦、爵士、流行、摇滚、民谣、中国风 / 古风、影视 / 游戏配乐等**真实乐器编制**。
> **本清单聚焦**真实乐器采样库；吵闹电子舞曲素材、合成器预设与 808 采样见 `electronic-styles.md` / `resources.md`，**属另一用途，不是禁用**。DAW 软件教程不计入编曲写作知识。
> 某库若同时含真实与电子音色（如 Trilian 含 synth bass、Keyscape 含合成器、Superior Drummer 含电子套件），**只取真实乐器部分**，电子部分不写。

## 来源标注约定（先读，避免误判可信度）

**主数据源**：`_bili_research/bili_search_raw.json` —— **973 条去重 B 站视频**，字段 `bvid / title / author / play / duration / description / keywords`，按播放量降序，核实时间 **2026-11-10**。本文件所有 B 站 BV 号、UP 主名、播放量均取自该文件的 `bvid / author / play`，可逐条回查；已按标题剔除「全专音源 / 落雪·洛雪音乐 / 听歌软件 / 蓝牙耳机」等同名噪声，以及 DAW 教程与电子编曲内容。

| 标记 | 含义 | 可信度 |
|---|---|---|
| `【B·BV… ｜ UP主 ｜ 播放量】` | B 站真实视频，来自 raw json，可核 | **有出处的事实** |
| `【B·检索补充 BV…】` | WebSearch 得到的 B 站视频 BV，真实可点开，但**不在 raw json 的 973 条内**（仅 2 条，见附录） | **有出处的事实**（较弱，需自行点开复核） |
| `【B·专栏 cv…】` | B 站专栏，标题 / cv 号来自 WebSearch 摘要（非 raw json） | **有出处的事实**（较弱） |
| `【官网 2026-11-10】` | 厂商官网页面交叉验证的价格 / 体积 / 技法数 | **有出处的事实**（硬信息） |
| `【三方】` | 非 B 站第三方文章（少数派、什么值得买、微信公众号、专业测评站） | **有出处的事实**（转述） |
| `【口碑】` | 业界经验 / 多篇测评共识，无单一可核实结论 | **业界经验 / 口碑** |
| `【通用理论补充】` | 无法核实到具体 BV 的通用方法论 | **通用理论补充** |

> **仍存限制（如实披露）**：B 站视频 / 专栏页需登录，WebFetch 抓取一律返回登录墙，因此**视频字幕、简介正文、评论区干货未能读取**。凡涉及「测评结论 / 口碑共识」的表述，均由 raw json 中的**视频标题 + 多篇横评交叉印证 + 第三方转述**得出，不伪称读到了字幕内容；具体参数（价格 / 体积 / 技法数）一律以官网为准并标注核实时间。
> 价格 / 体积为动态信息，官网常年促销（常见 5 折～对折），下单前以官网 / 代理实时价为准。

---

## 0. 三条先读结论

1. **先定播放器，再买库。** 大量「Kontakt 库」必须完整付费 Kontakt，免费的 Kontakt Player 只能加载官方授权 Player-compatible 的库，买错是最常见的浪费 `【三方：Future Sound Academy 2026 / 官网 2026-11-10】`。B 站播放量最高的音源教程正是 `【B·BV1JW41117qg ｜ 音律屋 ｜ 296965】《【合集】编曲采样器Kontakt（康泰克）全套教程！》`——先把播放器吃透再买库。
2. **免费库足够做草图，成片必须换「鼓、贝斯、主音色」三样** `【出处：技能 references/resources.md】`。换之前先查 MIDI 里有没有 ≥8 档力度、CC64 踏板、CC11 表情；全曲 0 个 CC 就先加表情，否则换来的钢琴只是「更响的电子琴」`【出处：技能 references/sample-instrument-swap.md】`。
3. **体积 ≠ 好坏，映射策略才决定手感。** 同一 3GB 的两个库，一个只是样本多，另一个把演奏逻辑写进 Kontakt 脚本（KSP）里 `【三方：kbid《Kontakt采样音源机制》】`。判断标准见第 2 节，全是可量化的及格线；B 站已有可直接当验收素材的大规模横评（见 2.1）。

---

## 1. 采样播放器对照（先选容器）

| 播放器 | 价格 | 格式 / 授权 | 关键机理 | 短板 | 落地场景 | 来源 |
|---|---|---|---|---|---|---|
| **Kontakt 8**（完整版） | 约 $299 / £300 | NKI 专有，商业库主流 | Instrument→Group→Zone 三层；KSP 脚本做 RR / 无键切换奏法识别 / 智能 legato / 人性化 timing；DFD 磁盘直读；官方最低 4GB RAM、推荐 6GB | 贵；界面重；不买就打不开大量第三方库 | 要用 CSS、Noire、多数商业弦乐 / 民乐库的唯一入口 | `【三方：Future Sound Academy、kbid、goldmidi】` `【B·BV1JW41117qg ｜ 音律屋 ｜ 296965】` |
| **Kontakt Player**（免费） | $0 | 仅加载 Player-compatible 库 | 与完整版同引擎；未授权库 15 分钟后进演示锁 | 不能自建乐器；不兼容非 Player 库 | 免费起步、跑 LABS / Project SAM Free Orchestra / The Orchestra Elements | `【官网 2026-11-10】` `【B·BV1Vq4y1i7Ms ｜ 江户川青山丶 ｜ 17508】《Freepiano/EOP加载音源【Kontakt音源入库】》` |
| **Spitfire 自有播放器 / Splice INSTRUMENT** | 免费 | LABS / BBCSO 专用 | 免 Kontakt；BBCSO 三档同在 Maida Vale，声场一致 | 历史上有需联网加载、更新后文件丢失的报告；2025-10 Splice 收购 Spitfire 后 LABS 目录迁入 Splice INSTRUMENT，旧 LABS 仍并行可用 | LABS 全套、BBCSO Discover / Core / Pro | `【官网 2026-11-10 产品对比页】` `【三方：Bedroom Producers Blog】` |
| **Decent Sampler** | 免费 | DSF，社区库在 Pianobook | 轻量，keyswitch 奏法、力度 / 延音响应，内置混响 | 只跑 DSF，不能随手导入 WAV 建乐器；无真正 legato 引擎、RR 管理基础、不能单 patch 内混多麦位 | Pianobook 免费钢琴 / 氛围织体 | `【三方：Bedroom Producers Blog、Lord Reverb 2026】` |
| **sforzando**（Plogue） | 免费 | SFZ 开放格式事实标准 | 读 SFZ / SoundFont，键区映射可靠，音频质量好 | 界面极简；SFZ 库之间构建质量参差 | VPO、Sonatina、VSCO2、Salamander | `【三方：Lord Reverb、Future Sound Academy】` `【B·BV1jtvPzVEBd ｜ RE_Media_Prod ｜ 2418】《Soundfont音源系列：sf2钢琴音源The Grand》` |
| **sfizz** | 免费（BSD-2） | SFZv1 + 部分 SFZv2 | v1.2.3（2024-01-14）；win64 仅 7.9MB；VST3i / AU / LV2 / JACK；按需流式加载并回收内存；热重载 | 仓库 2026-06-21 已归档只读；SFZv2 支持不全；命令行渲染**必加 `--use-eot`**，否则尾音无限渲染 | 离线批量渲染 SFZ（配合技能 sample-instrument-swap.md 的 Salamander 流程） | `【出处：技能 references/sample-instrument-swap.md】` `【三方：Position Is Everything 2026】` |
| **SINE / Synchron / Opus / Engine / ARIA** | 随库免费 | 各厂专有 | Orchestral Tools / VSL / EastWest / Best Service / Garritan 各自播放器 | 一家一个账号、一个下载器，模板膨胀 | 柏林系列、VSL BBO、Hollywood Orchestra、黄河古筝（Engine） | `【三方】` `【B·专栏 cv12072633】` |

> **安装逻辑** `【B·BV1uQ4y1k7XF ｜ 橙子味の卜卜星 ｜ 13929】《一个视频搞定所有音源的安装方法，软音源的安装逻辑》`：先搞清 NKI / SFZ / DSF / 自有引擎分别走哪条入库路径，再装库，能省掉大半「音源加载不出来」的问题。
> **SFZ 是唯一值得长期投入的开放格式** `【通用理论补充】`：NKI 是 Kontakt 专有、DSF 绑死 Decent Sampler，而 SFZ 可被 sforzando / sfizz / ARIA / 多数 DAW 内置采样器读取，免费管弦库（VPO、Sonatina、VSCO2、Salamander）几乎全有 SFZ 版。

---

## 2. 如何判断一个音源好不好（5 个硬指标 + 现场验收）

**验收顺序**：先拉长音推 Mod Wheel → 再跑一段连奏旋律 → 再连续敲同一音 16 次 → 再松开踏板听尾音 → 最后全开麦位看资源占用。全程不插效果器、不加混响。

| 指标 | 是什么 | 及格线（可执行数值） | 怎么测 | 典型坑 | 来源 |
|---|---|---|---|---|---|
| **动态层 velocity layer** | 同一音在 pp→ff 录多套样本，重建「音色随力度变」的非线性 | 木管 / 铜管 **3–5 层**；钢琴 **8–16 层**，顶级 >20；电贝斯 **8–9 层**已够 | 拉住长音，缓慢推高 Mod Wheel / CC1，听**质地**（气流噪声、泛音、瞬态）是否变，而非只变音量 | 1–2 层靠插值硬推＝弱奏「假安静」、强奏「假激动」；中高音区层切换突兀 | `【三方：kbid《木管音源核心参数解析》、audioscene.org】` |
| **Legato 过渡** | 音与音之间的过渡采样 + 速度识别阈值 | 90–140 BPM 抒情线，过渡采样 **≤250ms** 句尾才不拖沓；CSS 类引擎有 **60–300ms** 前瞻延迟，需把 MIDI 音符前移补偿 | 弹 8 小节连奏旋律，慢速与快速各一遍，听每个音是否像「重新按下去」 | 阈值过低→正常句法被判分音；过高→快速音群糊成一片；双簧管最明显 | `【三方：kbid、CSS 测评共识】` |
| **Round Robin（轮替）** | 同一音同力度录多个 take，循环触发 | 短音 **≥4 组**；高频重复 / ostinato **6–8 组**更稳；带「智能重置」「随机起点」加分 | 同一键连敲 16 次，听是否像复印；两小节单簧管 ostinato 最暴露 | 无 RR＝「机关枪效应」da-da-da-da | `【三方：kbid、becomeaprocomposer.com、audioscene.org】` |
| **麦克风摆位 mic position** | close / tree / outrigger / room 等多组话筒 | **不是越多越好**：室内配器双簧管 / 英国管「主麦 + 少量近距」即可；新手一律先用默认 mix | 逐轨拉推子：近距加 proximity / attack，远 / 房间麦加距离与模糊感 | 近距过多→簧片 / 按键噪声顶前；环境麦过重→旋律边缘发虚；麦位越多内存 / 磁盘压力越大 | `【三方：kbid、becomeaprocomposer.com】`；BBCSO Pro 20 麦位 / 600GB+ 为极端案例 `【官网 2026-11-10】` |
| **Release 尾音** | `trigger=release` 的释音采样、踏板噪声、琴弦共振 | 必须有独立 release 采样；踏板踩下时测的是整段衰减不是单音 | 弹单音后突然松键、再踩踏板弹一串后松，听断裂是否突兀 | 无 release 采样＝断音像被切掉；踏板连着时 attack / tail 测量指标全部失效 | `【出处：技能 references/sample-instrument-swap.md】` `【通用理论补充】` |
| **复音真实连奏（进阶）** | 和弦内每个声部各自有滑音过渡，且同音程多次演奏有变化（Round Robin True Legato） | 不靠宣传列表，靠实测：和弦进行时内声部是否仍有真实滑音、重复演奏是否有可感变化 | 弹一段四声部和弦进行，反复三遍 | 每声部每过渡都要额外重复采样，是某些库达 105GB 的主因 | `【三方：kbid《复音真实连奏采样原理》】` |

### 2.1 直接拿 B 站横评当验收素材（真实 BV，省去自己堆 20 个库）

| 横评内容 | UP 主 / 播放量 / BV | 用来验什么 |
|---|---|---|
| 弦乐大乱斗：CSS、LASS、沁弦乐、如歌、波西米亚、喷火、SWAM、BBC 等 **12 款** | `【B·BV1WF4m1j788 ｜ 汪叔聊编曲 ｜ 22880】` | 同一乐句下对比 legato 过渡、动态层平滑度、厅堂一致性；顺带补齐弦乐库名单 |
| 钢琴音源大乱斗：**17 台钢琴** | `【B·BV1k1421C7HU ｜ 汪叔聊编曲 ｜ 20541】` | 逐台听力度层切换、踏板共振、release 尾音 |
| **25 款弦乐音源大排名：从最佳到最差，买谁不踩坑** | `【B·BV1qSeM66EcX ｜ 老王Mix ｜ 3017】` | 选购避坑顺序 |
| 7 款原声钢琴音色推荐及试听对比 | `【B·BV1WN411i7Ps ｜ 音乐制作大澄子 ｜ 31004】` | 盲听判别「真钢 vs 电子琴味」 |
| kontakt 音源对比 pianoteq（爱丽丝 / 斯坦威 / My Grandeur） | `【B·BV1Gb411i7RA ｜ 索尼音质更赞 ｜ 70129】` | 采样派 vs 物理建模派的差别 |
| 钢琴音源现场对比试听：象牙钢琴 3 / Pianoteq 9 / Keyscape | `【B·BV1BRC9B4EaP ｜ 七线阁官方 ｜ 9256】` | 三款旗舰同台 |
| 鉴定 3 款网红弦乐编曲音源，都适合怎么用 | `【B·BV15j421Z751 ｜ 欧阳箐宇OY_Music ｜ 17296】` | 「场景选库」而非「谁最好」 |
| 弦乐音源的选择 | `【B·BV19c411577k ｜ Flu老师创作课 ｜ 18708】` | 入门判断框架 |
| 流行弦乐编写思路、画表情、小技巧、实录对比 | `【B·BV1bnRnYHEmR ｜ 汪叔聊编曲 ｜ 12602】` | 换源后怎么画 CC11 才不假 |

> **一条反直觉结论** `【出处：技能 references/sample-instrument-swap.md】`：「GM 高频占比只有 0.1%，换音源补高频」是错的。实测真实钢琴比 GM **暗**：1kHz 处 GM 只降 1.6dB（金属味），真实钢琴降 12.1dB（基频主导）。别用宽带 FFT 频段占比判断音源，要用 1/3 倍频程逐带 RMS 且两版同法测。

---

## 3. 分类音源目录

> 表内「来源」列即该行关键结论的出处标记，含义见开头约定。价格 / 体积标注核实时间 2026-11-10。

### 3.1 钢琴 / 电钢

| 库 | 价格 | 体积 | 播放器 | 采样深度 | 授权 | 强项 / 短板 | 场景建议 | 来源 |
|---|---|---|---|---|---|---|---|---|
| **Salamander Grand Piano V3** | 免费 | 716MB | sfizz / sforzando | Yamaha C5，88键×**16 力度层**＝641 FLAC；cc64 踏板、踏板噪声、琴弦共振 cc20、击槌噪声 cc21、release 采样 | CC-BY 3.0（需署名，可商用） | 免费里动态层最扎实；无多麦位 | 古典 / 流行钢琴成片、离线渲染首选 | `【出处：技能 references/sample-instrument-swap.md】` |
| **Spitfire LABS 系（Soft / Felt / Intimate Grand Piano 等）** | 免费（注册即下） | 单件数百 MB 级 | Spitfire 自有 | 单件多为少数奏法、少动态层 | 免费可商用；注意 2025-10 迁 Splice INSTRUMENT、历史需联网 | 音色有性格、加载极快；深度浅，撑不住独奏 | 草图、氛围铺底、影视留白 | `【B·专栏 cv12072633】` `【三方：少数派 2025】` |
| **Piano One（Yamaha C7）/ Keyzone Classic / 99Sounds Piano / The Grand(sf2) / True Pianos** | 免费 | 百 MB～1GB | 各自 / 免费 / sf2 | 单层为主 | 免费，逐款查 EULA | 零成本可用；「堪比付费」是口碑夸张 | 预算为零的草图 | `【B·BV1Vf4g6oEkS ｜ 三减水 ｜ 1504】《免费音源/经典钢琴/Keyzone Classic》` `【B·BV12J41157JW ｜ 辣鸡aMura ｜ 8551】《99Sounds Piano立式钢琴音源》` `【B·BV1jtvPzVEBd ｜ RE_Media_Prod ｜ 2418】` `【B·BV1qFdvBvEY5 ｜ 优音公益 ｜ 2854】《True Pianos 钢琴插件》` `【B·BV1AoWu6bE9E ｜ 睿轩Rayson ｜ 210】《这可能是最好的免费钢琴音源》` |
| **EMP / Electro-Mechanical Piano Mark II**（Sonokinetic） | 限免 | 小 | **Kontakt Player 7+** | 采样 Rhodes Mark II 可能性大；界面仅低音提升 + 音量，点箭头可进高音提升 / 释放 / 调制 | 限免领取，看 EULA 是否限个人 | 电钢开箱即用；领取有截止风险 | 爵士 / 流行电钢 | `【B·专栏 cv20410121《EMP来袭!Kontakt免费电钢琴音色库限时免费》】` |
| **电钢替代方案（软音源顶真钢）** | — | — | — | 让 3 千的电钢用上三万的琴的音色 | — | 键盘手现场 / 家用省成本 | `【B·BV17D4y127JZ ｜ WANG志晟 ｜ 79383】《让你3千的小电钢用上三万的琴的音色：软音源替代》` `【B·BV1pqLV6JEfN ｜ Jony不会即兴 ｜ 36725】《最强音源pianoteq9推荐！用电钢弹出真钢的感觉》` |
| **NI Noire** v1.2.0 | 约 $199 区间 + **必须完整 Kontakt** | **「15G」** | 完整 Kontakt（Player 会 15 分钟演示锁） | Nils Frahm 的 Yamaha CFX，Pure / Felt 两套真实录音；Particles 附加纹理层 | 商业可商用 | 强：影视 / 新古典氛围、弱奏细腻；短：单一立体声像无多麦混合、不适合爵士 / 流行硬朗独奏 | 影视配乐、neoclassical 钢琴 | `【B·BV1LH4yK7QE ｜ 编曲助手 ｜ 23850】《雅马哈三角钢琴音色 NI Noire v1.2.0 KONTAKT「15G」》（版本号与体积来源）` `【三方：Lord Reverb 2026】` |
| **Modartt Pianoteq 9** | 付费 | **约 60MB** | 自有插件 | **物理建模非采样**，参数全可调、无采样噪声、麦位自由度极高 | 商业可商用 | 强：体积 / CPU 极省、清澈；短：不如采样华丽，需调教 | 低配机、现场、需精确麦位 | `【B·BV142yaB7Ebc ｜ 七线阁官方 ｜ 33938】《地球最强钢琴综合音色Modartt Pianoteq 9》` `【B·BV1mp2FB8E5A ｜ 汪叔聊编曲 ｜ 16486】《钢琴音源天花板？PianoTEQ9教学》` `【B·BV179zPBgEmu ｜ 键盘科学 ｜ 8567】《PIANOTEQ9仍是钢琴音源之王？》` `【三方：微信公众号（约 60MB）】` |

> **采集口径说明**：下表是本轮 B 站素材的筛选记录，只说明「哪些视频没被选进这批研究稿」，**不代表技能禁用合成器或 DAW**；吵闹电子舞曲内容已单独归档到 `electronic-styles.md`。

| **Spectrasonics Keyscape** | 付费（高端） | **77GB** | 自有插件 | 36 种键盘、500+ 预设，含 LA custom C7 / Rhodes / Wurli / 羽管键琴 / tack piano，收录机械噪声与共振 | 商业可商用 | 强：音色广度、开箱即用；短：为 35 个用不上的乐器付钱；**只取原声钢琴 / 电钢 / 风琴等真实键盘，合成器部分排除** | 工作室「随时要一台稀有键盘」 | `【B·BV1BRC9B4EaP ｜ 七线阁官方 ｜ 9256】（与象牙3/Pianoteq9 同台对比）` `【三方：微信公众号《这10款虚拟乐器…》】` |
| **象牙钢琴 3（Ivory 3）/ Garritan Abbey Road CFX / 施坦威 D274 / Cinesamples CinePiano / Galaxy Steinway / My Grandeur** | 付费 | CFX 约 **122GB** | 各自 | 多麦位、多力度层，音乐会大钢琴 | 商业可商用 | 强：古典独奏 / 大动态；短：体积巨大、价格高 | 古典奏鸣曲、暴露的独奏钢琴、影视钢琴 | `【B·BV1BRC9B4EaP ｜ 七线阁官方 ｜ 9256】` `【B·BV13KpD6DEcg ｜ 古河汐Pia_Official ｜ 5424】《施坦威D274音源 音色鉴赏及对比》` `【B·BV1ri4y1s7QN ｜ 来悟空视频素材网 ｜ 2372】《电影钢琴音源CinePiano演示》` `【三方：pianoworld.cn】` |

**落地顺序（钢琴）** `【通用理论补充】`：免费 Salamander / Keyzone / LABS 起草图 → 暴露的古典独奏上 Garritan CFX / Ivory 3 / 施坦威 D274 → 影视氛围上 Noire Felt 或 CinePiano → 低配 / 现场上 Pianoteq 9 → 啥都要且预算够最后才 Keyscape。别一上来买「全集」。
**短小精悍需求** `【B·BV16Q4y1M74p ｜ MoVear ｜ 19321】《网上的钢琴音源太大没时间下载？康康这个钢琴吧！短小精悍！》`：硬盘紧张时的替代思路。

### 3.2 弦乐（独奏 / 合奏 / 群）

| 库 | 价格 | 体积 | 播放器 | 采样深度 | 强项 / 短板 | 场景建议 | 来源 |
|---|---|---|---|---|---|---|---|
| **Spitfire LABS Strings / Frozen Strings / Strings 2** | 免费 | 单件小 | Spitfire 自有 | Strings 14 人合奏、3 奏法（Short / Ensemble / Long）；Frozen Strings 6 人干声、超级 sul tasto | 强：亲密、干、暖；短：非大编制、无 divisi | 流行弦乐垫、室内乐、氛围织体 | `【B·专栏 cv12072633】` `【三方：Bedroom Producers Blog、pixel-mixers】` |
| **BBCSO Discover** | **免费**（注册） | 轻量 | Spitfire 自有、**免 Kontakt** | **35 乐器 / 47 技法**，单一预混「Performer」麦位，含完整弦乐 legato / long / short | 强：免费里最像真乐团、声场统一、加载快；短：单麦位、技法有限 | 管弦入门、草图、学习配器 | `【B·专栏 id=13957449】` `【官网 2026-11-10 产品对比页：Free / 47 Techniques / Maida Vale】` `【B·BV1NT411M7pF ｜ EasonYanMusic ｜ 281】《把 BBC SO Pro 独有乐器及演奏法"迁移"到 Core 与 Discover 里使用》（进阶技巧）` |
| **Easy Strings / Monster String / LABS 免费弦乐** | 免费 | 小 | 各自 | 基础长音 / 断奏 | 强：初学够用；短：做不出付费弦乐的效果 | 草图 | `【B·BV16g4y1k7Hd ｜ 吃瓜王萌零 ｜ 9027】《免费小品弦乐音源——Easy Strings》` `【B·BV1hSth67E2a ｜ 三减水 ｜ 3106】` `【三方：少数派 2025】` |
| **Strezov Minimalist Violins Legato Freebie** | 免费（官网领注册码） | **2GB** | **Kontakt 7+** | 仅 1 个小提琴连奏，取自 AFFLATUS Chapter I Strings（约 $800）；CC64 切换分奏 | 强：免费里罕见的高质量 legato；短：只有 1 个音色；需在 NA1 安装、官网下载后手动定位 | 需要一条像样的小提琴旋律线 | `【B·专栏 cv24786959】` |
| **VSCO 2 CE / Sonatina Symphonic Orchestra 4.0 / VPO** | 免费 / 开源 | Sonatina 4.0 **1.39GB**；VPO 约 0.6–4GB | sforzando / sfizz（SFZ） | Sonatina 含弦 / 管 / 铜 / 打 + 钢琴 / 羽管键琴 / 合唱，looped sustains；VPO 汇总 Sonatina + VSCO2 + 爱荷华大学公共领域录音 | 强：无账号、无 Kontakt、跨平台、MuseScore 可用；短：多场次拼盘，声场不统一，需统一厅堂混响 | 打谱软件回放、无 Kontakt 环境、教学 | `【出处：技能 references/sample-instrument-swap.md】` `【三方：Bedroom Producers Blog】` `【授权：Sonatina CC Sampling Plus 1.0，商用需署名】` |
| **Cinematic Studio Strings（CSS）** | **$399** | 约 5–8GB RAM | **完整 Kontakt 6+** | 60 人编制，Auto Legato（踏板切换）、自然过渡、真实 vibrato | 强：业界公认最「会呼吸」的 legato；短：单一麦位、60–300ms 延迟需前移 MIDI | 影视 / 电视 / 预告、抒情大旋律 | `【B·BV1WF4m1j788 ｜ 汪叔聊编曲 ｜ 22880】（12 款横评含 CSS）` `【三方：musicproductionwiki 2026】` |
| **LASS（LA Scoring Strings 1–3 代）/ MSS** | 付费 | 大 | 完整 Kontakt | 分奏细、多奏法 | 强：分声部写作；短：学习成本高 | 精细分奏、影视 | `【B·BV1jH4y137Bv ｜ 音律屋 ｜ 35289】《编曲必备Lass弦乐全套教程（14集），1至3代全讲解》` `【B·BV1z54y187cR ｜ 音律屋 ｜ 53617】《弦乐巨头MSS快速上手教程【7集全】》` `【B·BV1WF4m1j788 ｜ 汪叔聊编曲 ｜ 22880】` |
| **沁弦乐 / 如歌（Best Service Chris Hein Strings Compact）/ 波西米亚 / SWAM / LUX Orchestral Strings** | 付费 | 中～大 | Kontakt / 各自 | 各自定位（Compact 精简、SWAM 物理建模、LUX 教程向） | 短：具体参数未核实，按横评试听挑 | 特定音色诉求 | `【B·BV1WF4m1j788 ｜ 汪叔聊编曲 ｜ 22880】（12 款横评列出库名）` `【B·BV1Rt421A7LD ｜ 编曲助手 ｜ 9438】《如歌弦乐音源 Best Service Chris Hein Strings Compact Kontakt》` `【B·BV174muBkERW ｜ 七线阁官方 ｜ 10891】《极品好弦乐LUX Orchestral Strings使用教程》` `【注：以上库名出自 B 站横评标题，具体体积 / 价格 / 技法数未核实，不作断言】` |
| **Spitfire BBCSO Core / Pro** | Core **£399 / $449**；Pro **£899 / $999** | Pro **600–630GB**、20 麦位 | Spitfire 自有 | Core 44 乐器 / **344 技法**，含 legato(portamento & slurred)、long CS、flautando、sul tasto / pont、Bartók pizz、col legno、trill 等 | 强：全团同厅同链、声部零混音成本；短：Pro 声场固定偏大、**瞬态不如柏林**、多麦位致体积失控 | Core 覆盖 90% 制作人；Pro 给要精确麦位的终混 | `【官网 2026-11-10：首页 $449/$999、对比页 £399/£899】` `【B·专栏 cv23992169《柏林系列和喷火BBC哪个更好?》】` `【三方：微信公众号 BBC 深度解析】` |
| **Orchestral Tools Berlin Strings / Hollywood Strings Diamond / VSL Synchron Duality** | Berlin **$540**；HSD 走 ComposerCloud+ **$29.99/月**；Duality **$595** | HSD 满麦位需 30–40GB RAM | SINE / Opus / Synchron | HSD 60 人、16 麦位、Eastwood Stage、全套 legato / 短弓 / sul pont / col legno / harmonics；柏林瞬态强、分奏细节强 | 短：HSD 吃内存、柏林电影味偏重不适合纯古典 | 纯古典选 VSL；重瞬态 / 分奏细写选柏林；好莱坞大编制选 HSD | `【B·专栏 cv23992169】` `【B·BV1WF4m1j788 ｜ 汪叔聊编曲 ｜ 22880】（横评含喷火 / BBC）` `【三方：artistsindsp 2026】` |
| **独奏：PocketBlakus（大提琴）/ NI Stradivari Violin / Impact Soundworks Stroh Violin** | 免费 / $199 / 付费 | 小 | Kontakt | PocketBlakus spiccato 带 **7 组 RR**；Stroh 含 pizz / spiccato / legato | 短：独奏库音色个性强，别塞进大编制 | 民谣、室内乐、独奏旋律 | `【三方：pixel-mixers、artistsindsp】` |

**口碑共识** `【B·专栏 cv23992169 + B·BV1qSeM66EcX ｜ 老王Mix ｜ 3017 + 口碑】`：没有任何一套管弦库适合所有曲风，最少备 2–4 套；「稍重选柏林、稍轻选 BBC」是常见分法；购买前去官网听 AudioDemo，国内可正常试听，信耳朵不信参数表。

### 3.3 木管 / 铜管

| 库 | 价格 | 播放器 | 关键技法 | 强项 / 短板 | 场景 | 来源 |
|---|---|---|---|---|---|---|
| **BBCSO Core / Discover 木管铜管组** | 免费 / $449 起 | Spitfire 自有 | 长笛 / 短笛 / 双簧 / 单簧 / 巴松、3 重奏组；圆号 / 小号 / 长号；Extended Legato（Slurred & Fast Runs）、Multitongue、Flutter、Cuivré、Sfz、Muted、Rips / Falls | 强：全团同厅、奏法齐全、A3/A4 重奏组现成；短：Discover 仅预混单信号 | 管弦总谱、影视配乐 | `【官网 2026-11-10 产品对比页】` `【三方：微信公众号 BBC 深度解析（列全技法表）】` |
| **Spitfire LABS / VPO / Sonatina 木管** | 免费 | 自有 / sforzando | 基础 long / short | 强：零成本凑齐声部；短：无多动态层、无真 legato | 草图、教学 | `【B·专栏 cv12072633】` `【三方：Bedroom Producers Blog】` |
| **Cinematic Studio Woodwinds / Brass** | 付费 | 完整 Kontakt | 与 CSS 同套 legato 逻辑 | 强：与 CSS 弦乐同生态、写法统一 | 已有 CSS 的项目 | `【三方：musicproductionwiki】` |
| **柏林 / VSL / Hollywood 管乐** | 付费 / 订阅 | SINE / Synchron / Opus | 多麦位、分奏控制 | 短：体积与内存吃紧 | 大编制终混 | `【通用理论补充】` |

> **木管验收要点** `【三方：kbid《木管音源核心参数解析》】`：盯 5 个参数——动态层 3–5、legato 速度阈值与过渡长度 ≤250ms、短音 RR ≥4 组、麦位数量克制、奏法切换入口要少（把长音 / 连奏 / 断奏 / 重音压到少量 keyswitch，否则每写两小节找一次键位，灵感掉得比音符快）。

### 3.4 吉他（木 / 古典 / 电吉他 clean）

| 库 | 价格 | 体积 | 播放器 | 采样深度 | 强项 / 短板 | 场景 | 来源 |
|---|---|---|---|---|---|---|---|
| **Ample Guitar M Lite / Shreddage 3 Stratus Free / Impact Soundworks 免费电吉他** | 免费 | 小 | 各自 / Kontakt Player | 基础分解与 clean | 一木一电，免费里够用；技法少 | 草图、节奏吉他垫 | `【三方：少数派 2025】` `【B·BV19GhWznEM1 ｜ 仲景Zy ｜ 17736】《免费ample音源下载与使用讲解》` |
| **Ample Guitar M（Martin D-41）/ T（Taylor 714CE）/ L（Alhambra 古典尼龙）** | AGM **$169** | 约 5GB | 自有插件 | 逐音编程、弦噪 / 品噪 / capo 逻辑、滑音 / 击勾弦 / 泛音、Tab Player、Riffer 4 Strum Note | 强：细节最可编程、独奏 / 指弹逼真；短：界面密、需要 MIDI 功底 | 民谣 / 指弹 / singer-songwriter 主音吉他 | `【B·BV1cd4y1T7FN ｜ 音律屋 ｜ 256019】《最强吉他音源Ample Guitar全套教程！》` `【三方：modwheel.net 2026、Lord Reverb 2026】` |
| **Ample Guitar WF（Gretsch 1959 Falcon 半空心）** | 付费 | **20+GB** | 自有插件 | Fingerstyle + Pick 双采样库、12 技法、Guitar Pro GP3–GP8 导入 | 强：爵士 / 布鲁斯 / 复古摇滚 clean 最像；短：体积大、现代流行 / 金属不适用 | 爵士和弦、复古 clean riff | `【三方：Lord Reverb 2026】` `【B·BV1cd4y1T7FN ｜ 音律屋 ｜ 256019】` |
| **Ample Sound 5in1 Acoustic Bundle** | **$543** | 5 件合计大 | 自有插件 | SJ-200 / 12 弦 / 古典 / 714CE / D-41 五把，共用一套逻辑 | 强：一套覆盖民谣 / 古典 / 12 弦；短：单音独奏在部分琴上不匀、首启需联网 | 影视 / 制作型工作室 | `【三方：Lord Reverb 2026】` |
| **NI Strummed Acoustic** | 付费 | 中 | Kontakt | 仅扫弦节奏型 | 强：不会弹吉他也能出扫弦；短：**无单音 / 指弹 / 独奏** | 流行 / 民谣伴奏扫弦 | `【三方：微信公众号《这10款虚拟乐器…》】` |
| **Ample China / Ample Guitar 全系** | 付费 | 单件数 GB | 自有插件 | 民乐与吉他同一套技法引擎 | 强：国产、技法全；短：需逐款买 | 见 3.7 民乐 | `【官网 amplesound.net 2026-11-10：全系 v4.1，AG 系列 2026-06-18 更新】` `【B·BV1aoat6SEFv ｜ 汪叔聊编曲 ｜ 9399】《Amplesound民乐4.0教程！还有新发布的《埙 幽鸣》》` |

**落地** `【通用理论补充】`：分解和弦 / 扫弦垫用 Strummed Acoustic 或 LABS 类即可；只要吉他进 foreground（前奏、间奏、指弹独奏），就必须上可逐音编程的 Ample Guitar 系并手动放滑音 / release 噪声。

### 3.5 贝斯（原声 / 电贝斯）

| 库 | 价格 | 体积 | 播放器 | 采样深度 | 强项 / 短板 | 场景 | 来源 |
|---|---|---|---|---|---|---|---|
| **60s P-Bass（IK 免费）/ Ample Bass P II Lite / Impact Soundworks 免费电贝司** | 免费 | 小 | 各自 / Kontakt Player | 基础指弹 / 拨奏 | 免费里质量已很高 | 草图、流行低音 | `【三方：少数派 2025】` `【B·BV1XFrfBQEGc ｜ 睿轩Rayson ｜ 5267】《免费正版四大件音源推荐》` |
| **Ample Bass J（Fender Jazz）/ P（Precision）** | **$119** | 20+GB | 自有 | 13 技法、复音 legato、降至 B0、双采样库 | 强：低频谐波重量真实、800Hz–1.2kHz 中频特征准；短：前两次要背 keyswitch、必须 SSD | 爵士 / 放克 / R&B / 流行 / 摇滚 | `【三方：Lord Reverb 2026】` `【B·BV1cd4y1T7FN ｜ 音律屋 ｜ 256019】（同厂引擎）` |
| **Spectrasonics Trilian** | 付费 | 大 | 自有 | 电贝斯 / 木贝斯 / 合成贝斯 | 强：一库通吃多风格；短：**只取电 / 木贝斯，synth bass 部分排除** | 需要一把琴覆盖全曲风 | `【三方：微信公众号《这10款虚拟乐器…》、Lord Reverb】` |
| **IK MODO Bass** | 付费 | 极小 | 自有 | 物理建模非采样 | 强：零磁盘、实时塑形；短：低频重量不如采样 | 低配 / 需自定义琴型 | `【三方：Lord Reverb 2026】` |

> **贝斯 8–9 个力度层足以让同一根弦在弱拨与狠扫之间出现明显性格差异** `【三方：kbid《Kontakt采样音源机制》】`。GM 贝斯只有音量变化，是「换源收益最直接」的声部之一。

### 3.6 鼓与打击乐（原声鼓组 / 管弦 / 民族打击）

> **本清单聚焦**真实鼓组采样（Acoustic Kit / Rock / Jazz / Folk / Country / Blues / Orchestral / 民族打击）；电子鼓机 / 808 / Trap 素材见 `electronic-styles.md`，属另一用途，不是禁用。

| 库 | 价格 | 体积 | 播放器 | 采样深度 | 强项 / 短板 | 场景 | 来源 |
|---|---|---|---|---|---|---|---|
| **MT Power Drum Kit 2 / SSD 5 Free / BFD Player** | 免费 | 小～中 | 各自 | 原声鼓组，MT Power 带 grooves 可拖进 MIDI 改 | 强：初学者完全够；短：麦位与力度层少 | 草图、流行 / 摇滚 demo | `【出处：技能 references/resources.md】` `【三方：少数派 2025】` `【B·BV1XFrfBQEGc ｜ 睿轩Rayson ｜ 5267】` |
| **Toontrack EZdrummer 3** | **$99** | 中 | 自有 | 预混成品鼓、Bandmate 自动配 groove、Song Track 快速排段落 | 强：开箱即成片、EZX 分风格扩展；短：麦位级控制少 | singer-songwriter、快速写歌 | `【三方：Violet Recording、Drum Spy、Lord Reverb 2026】` |
| **Toontrack Superior Drummer 3** | **$399** | **约 230–235GB** | 自有 | 多麦位 / 房间声 / bleed 控制、Tracker 音频转 MIDI、内置调音台 | 强：真实度天花板、可当多轨鼓录音混；短：默认 raw 不是 mix-ready、学习曲线陡、吃 CPU / 磁盘 | 专辑级摇滚 / 流行 / 影视鼓 | `【三方：Drum Spy、Drum Faster、Lord Reverb、微信公众号（约 235GB）】` |
| **XLN Addictive Drums 2** | **$149** | 轻 | 自有 | 每 kit 预混、瞬态控制好（军鼓 250Hz −4dB / 3kHz +2dB / decay 180ms 直接坐进混音） | 强：省机、预设精；短：原始麦位选项少 | 快速成片、笔记本能跑 | `【三方：Lord Reverb 2026】` |
| **流行「万金油」鼓音源** | — | — | — | 一套通吃流行编曲 | 短：具体型号见视频，未核实 | 流行 demo | `【B·BV13KYYe9Eoy ｜ Listenyoyoyo ｜ 8336】《推荐一套流行万金油鼓音源》` `【B·BV11KBwB6E7S ｜ 程子是做咖啡的混音师 ｜ 2058】《使用有鼓音源打一个李荣浩的〈不遗憾〉》` |
| **中国民族鼓音源（免费 VST）** | 免费 | 小 | VST | 大鼓 / 排鼓 / 板鼓 / 木鱼 / 梆子 / 锣钹铙等 | 强：国产、免费、民族打击质感好 | 古风 / 中国风 / 民族管弦 | `【B·BV1gq4y1c7v2 ｜ 陆铭扬 ｜ 47293】《国产音源，打击音源，非常漂亮的中国民族鼓音源。免费VST音源》` `【B·BV1VN411k7ES ｜ 默习 ｜ 9580】《中国风音乐—如何编写民族打击乐》（编写向）` |
| **管弦打击 / 戏曲打击** | — | — | — | 定音鼓、军鼓、大鼓、镲、编钟、钵、碰铃 | — | 管弦总谱、戏曲风 | `【三方：微信公众号《国风歌曲知识》】` |
| **Best Service Peking Opera Percussion / Ethno World / Vir2 World Impact** | 付费 | 中～大 | Engine / Kontakt | Ethno World 收录 200+ 世界民族乐器 / 打击 / 人声；World Impact 为非 / 亚 / 中东民族打击合辑 | 强：戏曲编钟 / 钵 / 碰铃首选；短：Ethno World 作点缀可以，当主奏品质不足 | 戏曲风、纪录片 / 游戏配乐 | `【B·专栏 id=701250《音乐人养成攻略之软件篇15：当今主流民族乐器音源》】` `【三方：什么值得买民乐账】` |

**磁盘提醒** `【三方：Lord Reverb 2026】`：SD3 的 230GB 走磁盘流送，CPU 反而轻（现代机约 3–8%），**瓶颈在硬盘**——5400 转机械盘中途会 buffer 报错，NVMe SSD 无此问题。

### 3.7 民乐（古筝 / 琵琶 / 二胡 / 笛箫 / 唢呐等）

| 库 | 价格 | 播放器 | 覆盖乐器 / 技法 | 强项 / 短板 | 场景 | 来源 |
|---|---|---|---|---|---|---|
| **Kong Audio 空音「吹拉弹打」** | 国产付费，**一整套 699 元**档 | 自有宿主多通道 | **22 件**民乐合集：二胡 / 京胡 / 高胡 / 板胡 / 马头琴 / 笛 / 箫 / 巴乌 / 埙 / 管子 / 笙 / 唢呐 / 葫芦丝 / 琵琶 / 阮 / 三弦 / 柳琴 / 古筝 / 古琴 / 箜篌 / 扬琴 / 打击；含表情、颤音、滑音、花舌、装饰音、人性化等控制 | 强：一套凑齐吹拉弹打、性价比高、真实度在合集里较好；短：单件技法不如单品库多 | 中国风 / 古风入门「一套够用」 | `【B·BV11UWve8EZi ｜ 肖闻Xiaowenn ｜ 7458】《【性价比国产音源】空音…一整套699，隔壁只够买一个音源！》（699 元来源）` `【B·专栏 id=701250（列 13 件中乐、称其时品质最高）】` `【三方：微信公众号（22 件、界面控件表）】` |
| **三体声音科技 Chinese Traditional** | 单件约 **599 元**档（国产单乐器参考线） | 自有 | 6 款：月下（葫芦丝）/ 凤鸣鸾和（唢呐）/ 苍穹（埙）/ 千里（洞箫）/ 新雨（曲笛）/ 落英（扬琴）；另覆盖笛 / 埙 / 扬琴 / 唢呐 / 箫 / 葫芦丝 | 强：超强可控性、纯净音色、细腻技法、**无缝技法衔接**、声场好；短：单件价格高、件数少 | 进阶 / 配乐、要求技法逼真的主奏 | `【B·检索补充 BV1tp4y167kT（经音频应用论坛转述：三体+空音给深圳卫视国风节目做音乐，直出未混音即达电视节目品质；新雨笛子颤音偏平静，空音笛子颤音更有张力）】` `【B·BV11UWve8EZi ｜ 肖闻Xiaowenn ｜ 7458】` `【B·BV1AWbv61Eow ｜ 夏66的Studio ｜ 1477】《全球顶级古风音源也不过如此了》` `【三方：微信公众号（6 款清单）、什么值得买民乐账（599 元）】` |
| **Strezov Sampling JADE / JADE Evolutions（中国民族管弦）** | 付费 | Kontakt | 中国民族乐器集合 / 民族管弦乐团 | 强：海外厂牌做的民乐团编制、适配合奏；短：具体乐器表未核实 | 民族管弦合奏、影视 | `【B·BV1uK411J7mM ｜ AnProphet ｜ 8182】《最全的民乐团音源Jade测评》` `【B·BV17s4y1P78V ｜ 口袋酷影_大脸猫 ｜ 8505】《Strezov Sampling JADE Evolutions KONTAKT介绍》` `【B·BV1G7gNzkEeQ ｜ MusicProducers ｜ 1701】《JADE Ethnic Orchestra Library》` |
| **East Asia 东亚民乐音源 / 综合古风音源套装 / 免费国风民乐 3 款** | 免费 / 付费 | 各自 | 古筝、琵琶、二胡、笛箫、扬琴、古琴等 | 强：免费款零成本入门；短：深度浅 | 草图、古风入门 | `【B·BV1Br4y1V73W ｜ 音律屋 ｜ 25444】《East Asia东亚民乐音源全套教程，古风编曲必备音源！》` `【B·BV1if4y1y7zZ ｜ 卡什么特 ｜ 58606】《【免费插件/vst】免费国风/民乐音源，我只服这3款》` `【B·BV1cf4y1n7ej ｜ Amu音乐 ｜ 9587】《综合古风音源套装的推荐使用和经验分享》` `【B·BV1Xt8dziEhc ｜ CRAT西略 ｜ 3144】《可以闭眼入的民乐私藏音源大盘点》` |
| **Ample China 系（凝月二胡 / 沧海箫 / 紫云君古筝 / 风雷鼓 / 敦煌箜篌 / 凤尾琵琶 / 埙《幽鸣》等）** | 付费 | Ample 自有 **v4.0 / v4.1** | 与 Ample Guitar 同套技法引擎；ACEH 二胡、CAEH（CatAudio）二胡为近年两大对比主角 | 强：技法全面、界面统一；短：逐款购买 | 需要与其他 Ample 库统一工作流 | `【B·BV1aoat6SEFv ｜ 汪叔聊编曲 ｜ 9399】《Amplesound民乐4.0教程！还有新发布的《埙 幽鸣》》` `【官网 amplesound.net 2026-11-10：Ample China 全系 v4.1，2026-09-25 更新】` `【三方：什么值得买（ACEH vs CAEH《星河叹》对比、CAEH 每技法附带表情可不画表情线）】` |
| **黄河古筝（Best Service）** | 付费 | **Engine 采样器** | 传统五声调音阶 + 十二平均律，技法丰富、自带空间预制 | 强：技法最齐、仿真度高；短：安装 / 加载麻烦 | 古筝独奏、需要完整古筝技法 | `【B·专栏 id=701250】` `【三方：微信公众号（需 Engine 加载）】` |
| **EastWest Silk** | 付费 | Opus（原 Play） | 笙管笛箫、琵琶、二胡、古筝 | 强：一库通收丝路乐器；短：**测评结论不客气——音色僵硬，连「假的好听」都难做到** | 不推荐作主奏 | `【口碑：什么值得买民乐账转述 B 站测评共识】` |
| **民乐技法键位（写 MIDI 前必查）** | — | — | 古筝：勾 / 抹 / 托、大撮 / 小撮、摇指、刮奏、颤音、轮指、琶音、上下滑音；笛：单吐 / 双吐 / 三吐、颤音、叠音、打音；二胡：揉弦（滚 / 压 / 滑）、长弓 / 短弓 / 跳弓 / 大击弓 / 顿弓 / 快弓（≥120BPM 十六分音符） | — | 决定音源能不能「演奏」而非「按键」 | `【B·BV1bX4y1C7SC ｜ 默习 ｜ 8258】《7分钟就能学会古筝编写吗？》` `【B·BV1Zg4y1K7Kv ｜ 默习 ｜ 2121】《四步学会编写二胡！》` `【三方：微信公众号《国风歌曲知识》】` |

> **口碑共识** `【口碑：什么值得买民乐账转述 B 站评论区 + B·BV11UWve8EZi】`：被顶最高的购买建议是「少走弯路，音源直接上三体科技或者 amp 系列」；空音被叫多年「国风编曲经典神器」，一整套 699 元的性价比是高频论点；二胡曾是「国风编曲最大遗憾」，近年才被 ACEH / CAEH 补齐。
> **落地顺序** `【通用理论补充】`：免费 3 款国风音源 / DSK Asian Dreams 起草图 → 一套 Kong Audio 或 JADE 凑齐编制 → 主奏乐器（笛 / 唢呐 / 古筝）按曲买单件三体 / Ample China / 黄河古筝。写民乐前先把上表技法键位查清楚，否则只会「写几个 12356」，成品既没传统味也没流行味 `【三方：微信公众号】`。

### 3.8 人声 / 合唱 / 无歌词人声

| 库 | 价格 | 播放器 | 内容 | 授权 / 短板 | 场景 | 来源 |
|---|---|---|---|---|---|---|
| **Spitfire LABS Choir / Eric Whitacre Choir 采样** | 免费 | Spitfire 自有 | 氛围合唱织体、无歌词「啊」声 | 免费可商用；注意需账号 | 宗教感、宏大铺底 | `【三方：akihabara-bc 免费音源清单】` `【B·专栏 cv12072633】` |
| **Voxos 人声音源** | 付费 | Kontakt | 影视配乐人声采样 / 无歌词人声 | 强：解决「配乐没人声采样」；短：具体参数未核实 | 影视 / 游戏配乐人声 | `【B·BV1zB4y1d7Zi ｜ 乐才派 ｜ 9043】《还在头疼写配乐没有人声采样？Voxos人声音源解决你的问题》` |
| **BBCSO / The Orchestra Elements 合唱团** | 免费 / 付费 | Spitfire / Kontakt Player | 合奏预设中带合唱团 | 与乐团同厅，声场统一 | 管弦 + 合唱总谱 | `【B·检索补充 BV14E4m1R7DL】` `【官网 2026-11-10】` |
| **Strezov Sampling 合唱 / Balkan 民族管弦免费版** | 免费 / 付费 | Kontakt | 东欧 / 巴尔干合唱与民族人声 | 短：偏异域，非通用合唱 | 民族风、史诗感 | `【三方：akihabara-bc】` |
| **EastWest Hollywood Choir / Soundpaint 人声** | 订阅 / 免费起 | Opus / 自有 | 可拼唱词 syllables、无歌词人声 | 订阅制；注意商用条款 | 影视 / 游戏配乐人声 | `【三方：少数派 2025、musicproductionwiki】` |

> `【通用理论补充】` 无歌词人声在真实乐器编制里定位是「织体 / 色彩」，不要写成主旋律；先确认库是否允许把采样单独分发或用于 AI 训练素材，这是近年 EULA 收紧最多的条款。

### 3.9 管弦综合库（一套凑齐整个乐团）

| 库 | 价格 | 体积 | 播放器 | 内容 | 强项 / 短板 | 场景 | 来源 |
|---|---|---|---|---|---|---|---|
| **Sonuscore The Orchestra Elements** | **免费** | **4.01GB** | **Kontakt Player 6.7.1+** | 30 个合奏预设、23 弦乐、8 铜管、8 木管、竖琴、合唱团 | 强：免费里质量相当可以、加载快、支持免费 Player；短：限制多（The Orchestra 精简版） | 管弦入门、快速出气势草图 | `【B·检索补充 BV14E4m1R7DL《试用最新免费Kontakt管弦音源The Orchestra Elements…》（含官方序列号 + Native Access 手动定位入库流程）】` `【B·BV1vszrYLEj6 ｜ 黑帽Dokimusic ｜ 22004】（raw json 中的免费管弦综合库线索）` |
| **Project SAM The Free Orchestra** | 免费 | 中 | **Kontakt Player** | 从付费产品抽样的史诗断奏等 | 强：免费 Player 可跑、包络 / 八度 / 反向可调；短：偏声音设计 | 想试 Kontakt 库又不想买完整版 | `【B·专栏 id=13957449】` |
| **七个顶级管弦综合音源免费分享** | 免费 | — | — | 见视频清单（具体库名未核实） | 强：一次性收齐 | 免费起步 | `【B·BV1vszrYLEj6 ｜ 黑帽Dokimusic ｜ 22004】《『免费｜音源』七个顶级管弦综合音源免费分享（附下载）》` |
| **VSL Big Bang Orchestra（BBO）** | 免费 | 中 | **Synchron Player**（免费） | 全团同时录音、按力度触发声部；长音 / Marcato / swells / runs；keyswitch 切技法 | 强：同声场、内置调音台预混、配乐上手极快；短：每音符触发很多乐手，分声部控制弱 | 管弦编曲入门、干活快的配乐 | `【B·av95233653（经音频应用论坛转述的旧式 av 号，UP 主未核实，非 BV）】` |
| **BBC Symphony Orchestra Discover** | 免费 | 轻 | Spitfire 自有 | 35 乐器 / 47 技法，全团预混 | 强：免费里最完整、可「模式切换」分享给 Core / Pro 合作者编辑 | 学习配器、轻量总谱 | `【B·专栏 id=13957449】` `【官网 2026-11-10】` |
| **BBC Symphony Orchestra Core / Professional** | Core **£399 / $449**；Pro **£899 / $999** | Pro **600–630GB** | Spitfire 自有 | Core 44 乐器 / 344 技法；Pro 20 麦位、全技法、Atmos 麦混 | 强：性价比巅峰 / 终极控制；短：Pro 存储「冒犯性」大、瞬态不如柏林、需 purge 保内存 | 影视 / TV 主力；专业终混 | `【官网 2026-11-10】` `【B·专栏 cv23992169】` `【三方：微信公众号深度解析（Core 最推荐、全球销量最高）】` `【B·BV1NT411M7pF ｜ EasonYanMusic ｜ 281】（Pro 技法迁移到 Core/Discover 的技巧）` |
| **Spitfire Symphony Orchestra / Discover** | **$629** / 免费档 | 中～大 | Spitfire 自有 | 旗舰全团 | 短：与 BBCSO 定位重叠，二选一即可 | 已有 Spitfire 生态 | `【官网 2026-11-10 首页】` `【B·BV1VC4y1p7RY ｜ 来悟空视频素材网 ｜ 6877】《喷火弦乐Spitfire Symphonic Strings演示》` |
| **Edirol HQ Orchestral（罗兰交响乐）/ The Total Composure Orchestra / VPO / Sonatina** | 免费 / 老综合库 | 618MB～4GB | 完整 Kontakt / sforzando | TCO 1500 样本（公共领域）；VPO 全套弦管铜打 | 强：VPO 免账号免 Kontakt；短：拼盘声场、老旧 | MuseScore / Linux / 无 Kontakt 环境 | `【B·BV1nq4y1n7VX ｜ 听否音乐网 ｜ 9247】《Edirol HQ Orchestral罗兰交响乐64位管弦乐音色综合音源安装教程》` `【B·专栏 id=13957449】` `【出处：技能 references/sample-instrument-swap.md】` |

---

## 4. 免费库起步组合：草图 → 成片三级配置

> 原则 `【三方：Future Sound Academy 2026】`：**装 5 个懂的，胜过装 200 个没记忆的**。先 Kontakt Player + 一个 LABS 上真实曲子，用到什么再装什么。B 站播放量最高的免费音源导航是 `【B·BV1NaUmYME6V ｜ Metalion ｜ 315046】《免费好用的正版音源&交流网站推荐》` 与 `【B·BV19M411W78T ｜ PRODUCERGROUP_TV ｜ 54960】《【新手入门】如何免费获取音源插件》`。

| 级别 | 目标 | 具体配置（全部免费） | 升级触发条件 |
|---|---|---|---|
| **L0 草图** | 24 小时内把和声 / 结构 / 配器写出来 | Spitfire **LABS**（Strings + Soft Piano）+ **BBCSO Discover**（35 乐器 / 47 技法）+ **MT Power Drum Kit 2** + **Ample Guitar M Lite** + **Ample Bass P II Lite** + **sforzando + VPO / Sonatina** | 结构定稿，开始挑音色毛病 |
| **L1 可听 demo** | 给客户 / 导演听，不露怯 | 在 L0 上换：**The Orchestra Elements**（4.01GB）、**Salamander Grand Piano V3**（16 层）、**SSD 5 Free / BFD Player**（原声鼓）、**Strezov 免费小提琴 legato**、**Easy Strings**（`BV16g4y1k7Hd`）、**DSK Asian Dreams / LABS Choir** | 客户问「能不能再真一点」 |
| **L2 成片** | 发行 / 交付 | 按第 6 节顺序，把**鼓、贝斯、主音色**三样换成付费真实采样；钢琴上 Garritan CFX / Noire / Pianoteq 9；弦乐上 CSS（$399）或 BBCSO Core（$449）；民乐主奏上三体 / Ample China 单件 | — |

**免费资源线索（真实 BV）**：`【B·BV18k4y197pg ｜ 汪叔聊编曲 ｜ 33882】《一定要花钱买插件才能做音乐？这些免费你甚至没正眼瞧过！》`、`【B·BV1XFrfBQEGc ｜ 睿轩Rayson ｜ 5267】《免费正版四大件音源推荐》`、`【B·BV1UP411D74B ｜ 三减水 ｜ 23438】《免费音源/三角钢琴/Grand Piano/VST》`、`【B·BV1Vf4g6oEkS ｜ 三减水 ｜ 1504】《免费音源/经典钢琴/Keyzone Classic》`、`【B·BV1if4y1y7zZ ｜ 卡什么特 ｜ 58606】《免费国风/民乐音源，我只服这3款》`、`【B·BV1gq4y1c7v2 ｜ 陆铭扬 ｜ 47293】《免费中国民族鼓音源》`。
**限免信息的获取** `【三方：少数派 2025】`：B 站 UP 主「吃瓜王萌零」（`BV16g4y1k7Hd` 已可核）、「肖闻Xiaowenn」（`BV11UWve8EZi` 已可核）不定时发布可限时领取的正版音源 / 效果器动态；Pianobook、Soundpaint、Fracture Sounds、Impact Soundworks 常发免费库。
**授权提醒** `【通用理论补充】`：限免（如 EMP / Vivace Legacy）领取后要读 EULA 是否限个人使用；B 站专栏提到国内音源盗版曾普遍，商用项目一律走正版 `【B·专栏 id=701250】`。

---

## 5. 采样库文件组织与加载优化（全是可执行数值）

### 5.1 目录与工程设置

| 项 | 数值 / 做法 | 理由 | 来源 |
|---|---|---|---|
| 工程采样率 | **48kHz**，不要 96kHz | 96kHz 不提升听感，却显著增加 RAM 占用 | `【三方：musicproductionwiki 2026】` |
| 样本盘 | **NVMe SSD**，禁止 5400 转机械盘 | SD3 230GB 流送、大库麦位全开时机械盘会中途 buffer 报错 | `【三方：Lord Reverb 2026】` |
| 目录组织 | 按「厂商 / 库名 / 版本」三级；一个库一个根文件夹，NKI / SFZ / Samples 不混放；模板里存相对路径 | 换机 / 迁移时一次定位即可 | `【通用理论补充 + B·BV1JW41117qg ｜ 音律屋 ｜ 296965（入库 ADD / remove / reload / sort / change 封面 / 拖拽排序）】` `【B·专栏 cv21193769】` |
| 未用乐器 | 从 multi 中移除后**另存**为新 multi | 直接省 RAM 与加载时间 | `【三方：Loot Audio V-METAL 手册】` |

### 5.2 预加载缓冲（第一步就该改）

`【三方：Prominy《Preload buffer size configuration》、Loot Audio V-METAL 手册】`

1. Kontakt 5/6：`Options(齿轮) → Memory`；Kontakt 7+：`FILE → Options → Memory`。
2. 勾选 **`Override Instrument's preload size`**，拉到最小 **6kB**；大 multi 建议 **12kB**，若起音有噪声再往上加，直到 RAM 吃紧为止。
3. 默认预加载缓冲过大；减小后**加载时间变短、RAM 显著下降**。大 multi 起音若有杂音，改的是**声卡 latency（调大，不是调小）**，与预加载缓冲是两回事。

### 5.3 Purge 四步顺序（顺序错了会清空正在用的样本）

`【B·BV1JW41117qg ｜ 音律屋 ｜ 296965】《【合集】编曲采样器Kontakt（康泰克）全套教程！》第 7 节「快速加载音色及节省内存」` `【B·专栏 cv21193769（同教程专栏笔记）】` `【三方：goldmidi、Westwood Instruments 帮助中心、Loot Audio 手册】`

| 步 | 操作 | 作用 / 注意 |
|---|---|---|
| ① | **Reset markers** | 清掉旧工程残留的「使用标记」；看似危险，其实是安全起点 |
| ② | **完整播放一遍全曲** | 不 solo、不 mute、跑到尾音结束；只在最后 8 小节出现的样本也要触发；tempo 变化与 keyswitch 都算 |
| ③ | **Update sample pool** | 卸载所有未标记样本，并重载「已 purge 但被触发过」的样本；这一步才真正降内存，兼作缺音修复 |
| ④ | 需要时 **Purge all samples** | 全清后静音重放重建标记；**Reload all samples** 是撤销键，两者在同一菜单隔一个点击，误点会毁掉一次 take |

> Kontakt 8 官方最低 **4GB RAM / 推荐 6GB**；purge 菜单在 **Classic View** 的 instrument header，Kontakt 8.12 界面改版中仍不在新 UI；**没有 purge 快捷键、也没有「以 purge 状态加载」选项**，所以每次重开大模板都要重做一遍；macOS 的 Memory Server 只在单实例寻址不了的超大库才开 `【三方：goldmidi 2026】`。
> 部分新库（如 Westwood Evergreen 框架）自带 **AUTO-PURGE MICS**（麦位推子拉到底即卸载该麦位样本）与 **PURGE NOW**（清掉未选中的奏法），比全局 purge 更精准 `【三方：Westwood 帮助中心】`。

---

## 6. 音源与 GM 音色的替换顺序

**前置判断（先做，别急着换）** `【出处：技能 references/sample-instrument-swap.md】`

| MIDI 里有的 | GM 的处理 | 真实采样的处理 | 值得换？ |
|---|---|---|---|
| 力度 ≥8 档 | 只影响音量 | 8–16 层采样切换 | ✅ 直接可听 |
| **CC64 延音踏板** | **完全忽略** | 踏板采样 + 踏板噪声 + 共振 | ✅ **最强理由** |
| 表情 CC11 / CC1 / CC10 | 部分 / 不支持 | 动态层 + 表情交叉淡化 | ✅ |
| 单一力度、无踏板、全曲 0 CC | — | — | ❌ 白换，先补表情 |

**替换顺序（按「听感收益 / 成本」从高到低）** `【出处：技能 references/resources.md 原话「成片至少要换掉鼓、贝斯、主音色这三样」 + sample-instrument-swap.md】`

| 序 | 声部 | 为什么先换 | 换完必做 |
|---|---|---|---|
| ① | **鼓** | RR（≥4 组）+ 多力度层 + 房间麦，机关枪效应最明显 | 检查 groove 力度与 hi-hat 开合 CC |
| ② | **贝斯** | 8–9 层让弱拨 / 狠扫有性格差，低区谐波重量 | 与底鼓分频（低频归底鼓） |
| ③ | **主音色 / 钢琴** | 踏板采样、release 尾音、16 力度层 | 见下方混音重做 |
| ④ | **弦乐 / 管弦铺底** | 真 legato + 动态层交叉淡化 | 补 CC11 表情线，别只画 CC7 |
| ⑤ | **色彩 / 民乐 / 人声点缀** | 收益最小、最贵 | 最后换 |

**换源后必须重做混音（真实采样频谱形状与 GM 完全不同）** `【出处：技能 references/sample-instrument-swap.md 实测】`

| 症状 | 处方（数值） |
|---|---|
| 总线 60–120Hz 涨超 8 个点、发闷 | 伴奏钢琴 HPF **85 → 240Hz**；旋律钢琴 → **180Hz**；Pad → **260Hz** |
| 底鼓与琴箱撞车 | 底鼓 `peak 85Hz −3dB`、`gain −3.5dB`；镲片 `highshelf 7000 +5dB` |
| 250–500Hz 变薄 | 别硬补——真实钢琴该段天然低约 17 个点，是「从闷到透」的正常交换 |
| 伴奏钢琴低音区琴箱共鸣暴涨 | 实测 60–120Hz 占比 **2.3% → 17.1%（+14.9）**，低音区乐器普遍涨 10–15 倍 |

**A/B 纪律** `【出处：技能 references/sample-instrument-swap.md】`：对照组其余分轨**字节完全相同**（从同一份 MIDI 渲染），段落级归一到相同 LUFS，选「乐器最少的留白段」最容易听出差别，每段间留 1.5s 静音 + 2.5s 停顿，一次只变一个变量。

---

## 7. 商用授权速查

| 类型 | 能否商用 | 必须确认 |
|---|---|---|
| 免费采样库（LABS、BBCSO Discover、The Orchestra Elements、VPO、DSK 等） | 一般可 | 是否需注册 / 联网验证；LABS 2025-10 迁 Splice INSTRUMENT 后的条款变更 `【三方：Bedroom Producers Blog】` |
| CC 类（Salamander **CC-BY 3.0**、Sonatina 4.0 **CC Sampling Plus 1.0**、VSCO2 CE 开源） | 可 | **需署名**；CC Sampling Plus 禁止原样转售采样 `【出处：技能 references/sample-instrument-swap.md】` `【三方：Bedroom Producers Blog】` |
| 公共领域汇编（TCO 1500 样本、爱荷华大学录音、BBC Sound Effects） | 可 | 曲子 / 录音公有领域≠扫描件 / 排版可自由用，逐条看页面标注 `【B·专栏 cv12072633（BBC 官方音色库专门给出商业用途条款）】` |
| 商业付费库（Spitfire、CSS、SD3、Keyscape、Ample、三体、空音等） | 可（royalty-free 用于作品） | 普遍**禁止把采样再分发 / 做成竞品采样库 / 单独售卖音色**；订阅制（ComposerCloud+、Splice INSTRUMENT）停订后授权是否延续 |
| 播放器绑定 | — | **Kontakt Player 只认 Player-compatible 库**；完整 Kontakt 库用免费 Player 打开会 15 分钟演示锁 `【官网 2026-11-10】` `【B·BV1Vq4y1i7Ms ｜ 江户川青山丶 ｜ 17508】（入库实操）` |
| 限免 / 免费领（EMP、Vivace Legacy、各厂节日礼） | 看 EULA | 是否限个人 / 非商业；领取截止不明时尽早领 `【B·专栏 cv20410121】` |
| 国产民乐正版 | 可 | 走官方渠道（空音淘宝店等）；B 站专栏明确提到盗版曾普遍，商用一律正版 `【B·专栏 id=701250】` `【B·BV11UWve8EZi ｜ 肖闻Xiaowenn ｜ 7458】（正版性价比讨论）` |

**商用前必查 3 件事** `【通用理论补充】`：① 是否允许商业发行；② 是否需署名 / 是否禁止再分发采样；③ 是否需要完整 Kontakt 或持续订阅（这决定长期成本）。

---

## B 站学习地图（真实 BV，按「免费起步 → 播放器 → 判断 → 分类选购」排序）

> 以下 **12 条全部来自 `bili_search_raw.json`（973 条真实视频）**，UP 主名取自 `author`、播放量取自 `play`，BV 号可点开复核。已剔除同名噪声（全专音源 / 落雪音乐 / 听歌软件）、DAW 软件教程与电子编曲内容。

| # | UP 主 / 播放量 / BV | 标题 | 看什么 |
|---|---|---|---|
| 1 | Metalion ｜ 315046 ｜ `BV1NaUmYME6V` | 免费好用的正版音源&交流网站推荐 | 免费起步总导航，先建「从哪找正版免费库」的地图 |
| 2 | 音律屋 ｜ 296965 ｜ `BV1JW41117qg` | 【合集】编曲采样器Kontakt（康泰克）全套教程！ | 播放器必看：入库管理、快速加载、**purge all samples 省内存**（配合本文 5.3） |
| 3 | 汪叔聊编曲 ｜ 33882 ｜ `BV18k4y197pg` | 一定要花钱买插件才能做音乐？这些免费你甚至没正眼瞧过！ | 免费音源 + 效果器插件盘点，L0 配置清单 |
| 4 | 黑帽Dokimusic ｜ 22004 ｜ `BV1vszrYLEj6` | 『免费｜音源』七个顶级管弦综合音源免费分享（附下载） | 一次性收齐免费管弦综合库 |
| 5 | 汪叔聊编曲 ｜ 22880 ｜ `BV1WF4m1j788` | 弦乐大乱斗！CSS,LASS,沁弦乐,如歌,波西米亚,喷火,SWAM,BBC 等 12 款 | 弦乐横评：练「同一乐句听 legato / 动态层 / 厅堂」的耳朵 |
| 6 | 汪叔聊编曲 ｜ 20541 ｜ `BV1k1421C7HU` | 钢琴音源大乱斗！17 台钢琴，你最喜欢那一台？ | 钢琴横评：力度层切换、踏板共振、release 尾音 |
| 7 | 老王Mix ｜ 3017 ｜ `BV1qSeM66EcX` | 25 款弦乐音源大排名：从最佳到最差，买谁不踩坑？ | 选购避坑顺序，配合本文 3.2 表 |
| 8 | 音乐制作大澄子 ｜ 31004 ｜ `BV1WN411i7Ps` | 钢琴音色哪家强？！7 款原声钢琴音色推荐及试听对比 | 盲听判别「真钢 vs 电子琴味」 |
| 9 | 音律屋 ｜ 256019 ｜ `BV1cd4y1T7FN` | 最强吉他音源Ample Guitar全套教程！超详细编曲音源教程 | 木 / 电吉他 clean 逐音编程，配合本文 3.4 |
| 10 | 卡什么特 ｜ 58606 ｜ `BV1if4y1y7zZ` | 【免费插件/vst】免费国风/民乐音源，我只服这 3 款 | 民乐零成本起步，配合本文 3.7 |
| 11 | 肖闻Xiaowenn ｜ 7458 ｜ `BV11UWve8EZi` | 【性价比国产音源】空音…一整套 699，隔壁只够买一个音源！ | 空音「吹拉弹打」22 件、国产民乐价格锚点 |
| 12 | 陆铭扬 ｜ 47293 ｜ `BV1gq4y1c7v2` | 国产音源，打击音源，非常漂亮的中国民族鼓音源。免费 VST 音源 | 民族打击免费方案，古风 / 中国风鼓组 |

**补充（非 raw json，交叉印证用）**：少数派《2025年可免费获得的正版编曲音源》（免费钢琴 / 吉他 / 贝斯 / 鼓 / 弦乐分级清单）；什么值得买《做国风电子，音源到底要花多少钱…》（民乐价格账、ACEH vs CAEH 二胡对比）——**该文含国风电子 / Future Bass / AI 工具内容，按本文件边界只取「国产民乐音源价格与口碑」部分**；Spitfire 官网产品对比页（Discover / Core / Pro 三档技法、麦位、价格，核实 2026-11-10）；B 站专栏 `cv21193769`（Kontakt 全套教程的文字笔记）、`cv23992169`（柏林 vs BBC）、`cv24786959`（Strezov 免费小提琴 legato）、`cv20410121`（EMP 电钢琴）、`cv12072633`（18 套免费工具）、`id=701250`（主流民族乐器音源）、`id=13957449`（10 个免费管弦 VST）——专栏号来自 WebSearch 摘要，非 raw json。

---

## 附：数据来源、核实时间与未核实项

- **主数据源**：`_bili_research/bili_search_raw.json`，973 条去重 B 站视频，字段 `bvid / title / author / play / duration / description / keywords`，按播放量降序。文中 **59 个 BV + 对应 UP 主 / 播放量均取自此，可逐条回查，未编造**；另有 **2 个 BV 标注为 `【B·检索补充】`**（`BV14E4m1R7DL` The Orchestra Elements、`BV1tp4y167kT` 三体+空音民乐），来自 WebSearch 检索结果 / 论坛转述，真实可点开但不在 973 条内，已单独标记以免混淆。B 站学习地图 12 条**全部**来自 raw json。
- **筛选口径**：按标题保留「音源 / 采样库 / Kontakt / 具体乐器音源 / 免费音源 / 横评对比 / 教程」；剔除「全专音源 / 落雪·洛雪音乐 / 听歌软件 / 蓝牙耳机」等同名噪声、DAW 软件教程（Cubase / 库乐队 / FL Studio / Logic）、以及全部电子编曲内容（EDM / 808 / 鼓机 / Lo-fi / Trap / 合成器预设 / 国风电子素材包）。
- **核实时间**：价格 / 体积 / 技法数硬信息 **2026-11-10**。官网价取自 Spitfire 首页与产品对比页（$449 / $999 / $629、£399 / £899、Discover Free / 47 Techniques / Maida Vale），amplesound.net 全系 v4.1 与更新日期取自官网。促销价（1909 元 / 4252 元 / 599 元 / 699 元）来自 B 站视频标题与第三方转述，仅作区间参考。
- **仍未核实项**：① B 站登录墙导致**视频字幕 / 简介正文 / 评论干货未读取**，口碑结论由标题 + 多篇横评 + 第三方转述交叉印证得出；② `av95233653` 为论坛转述的旧式 av 号、非 BV，UP 主未核实；③ BV1tp4y167kT 链接经音频应用论坛转述，标题为帖文描述；④ 沁弦乐 / 波西米亚 / SWAM / LUX / JADE 等库的具体体积、价格、技法数未核实，仅记录「B 站横评中出现过」，未作参数断言；⑤ VPO 体积 0.6–4GB、Sonatina ~1.39GB / ~2GB 因打包版本不同并存，以实际安装包为准。
- **边界遵守**：只写本文件；未写 `references/bilibili-study-map.md`，未改动 `skills/music-build` 下任何文件。

---

## 附录：手风琴与三件套补充音源（补 §3 分类缺口）

> 用户主做情绪驱动编曲，主体编制为**钢琴 + 小提琴 + 手风琴**；§3 分类目录未列手风琴，这里补齐。
> 数据与 `core-instruments.md` §8.2 / §8.3 同源（2026-11-10 官网与三方核实存在）；
> **不写死价格**，只标免费 / 付费与区间参考，采购前以官网为准。
> **播放器判据**：Kontakt Player 只认 Player-compatible 库；标「需完整 Kontakt」的库
> 用免费 Player 打开会进 **15 分钟演示锁**（见 §0 / §7）。

| 类别 | 库名 | 免费 / 付费 | 播放器 | 关键能力 | 落地用途 |
|---|---|---|---|---|---|
| 钢琴 | **Native Instruments UNA CORDA** | 付费 | 免费 Kontakt Player 或完整 Kontakt 均可 | David Klavins × Nils Frahm 定制立式、**每键单弦**；纯 / Felt / Cotton 三声库；织物 / 机械 / **踏板** / 房间噪声可调；velocity 曲线与 pedal mode；10 GB / 100 snapshots | 含蓄悲伤、una corda 弱音踏板、预备泛音 |
| 弦乐 | **Best Service Chris Hein Solo Violin** | 付费（约 $179 区间） | 免费 Kontakt Player 5.6.8+ | **12 种短音 note heads** + spiccato；真 legato 三模式（**CC64 触发 long portamento**）；**CC1 控 vibrato speed / depth / intensity**；ponticello / flautando / harmonics / col legno / ricochet / runs；6 动态层 phase-align；2.73 GB（EXtended 9.4 GB / 38 奏法） | 独奏小提琴旋律线，一次配齐 12 种奏法 |
| 手风琴 | **Ilya Efimov Accordion**（钢琴式） | 付费 | **必须完整 Kontakt 7.10+，免费 Player 不可用** | 右手 **15 注册** + 左手 2 注册；**CC1 控动态（velocity 不控动态）**；CC21 / Auto attack；Detune（musette）+ KS；Key Noise / Bellow / Release；RR×3；Sustain / Staccato / Crescendo；**和弦识别 + Chord/Bass 与 Picking Mode**；1.7 GB / 2288 samples | 注册切换、风箱、musette detune、Stradella 左手完整建模 |
| 手风琴 | **Best Service Accordions 2**（Eduardo Tarilonte） | 付费（再版约 €/$199 区间） | Kontakt Player 5.71+ 或新版 Engine Player | 10 件乐器：Accordion（11 注册）/ **Bandoneon**（Alfred Arnold 探戈，含 Sforzato）/ Concert Accordion（Pigini，15 注册）/ French Musette / Folk / Steirisches / Concertina / Bass Accordion / Melodica 等；**3 动态层 × 3 RR**、**3 种 Bellow Shake**、key & button noises、左手 **14 种节奏伴奏**；U47 录音 / 8000+ samples | 一次覆盖 musette / bandoneon / 音乐会 / 民谣 / 低音手风琴全类型 |
| 手风琴 | **Ilya Efimov Bayan**（巴扬） | 付费 | 需完整 Kontakt | 2526 samples / 2.1 GB / **15 注册** / Staccato·Crescendo·Détaché | 东欧、深沉、宏大叙事 |

### 手风琴四类型对照（选型前必看，别混用）

| 类型 | 键盘 / 按钮 | 簧片与注册 | 性格 / 情绪 | 典型曲风 | 对应库 |
|---|---|---|---|---|---|
| **钢琴式 Piano accordion** | 右手钢琴键盘 + 左手 Stradella 键钮 | 8' / 16' / 4'，可带 musette | 通用、叙事、怀旧 | 民谣 / 流行 / 影视 | Ilya Efimov Accordion；Accordions 2 的 Accordion / Concert |
| **Musette（法式）** | 钢琴式或按钮式 | 双 / 三中簧 **detune ±8–25 cent** | 颤、甜中带苦、眩晕 | 巴黎香颂 / 圆舞曲 | Accordions 2「French Musette」；Ilya Efimov 的 Detune |
| **Bandoneon（班多钮）** | 全按钮、**无 Stradella 和弦键**、推拉异音 | 双簧为主 | 暗、撕扯、呼吸感 | 探戈 / 皮亚佐拉 | Accordions 2「Bandoneon」（含 Sforzato） |
| **Bayan（巴扬 / 俄式按钮）** | 右手全按钮半音阶、左手 Stradella / 自由低音 | 4 簧 15 注册、低音厚 | 深沉、宏大、东欧 | 古典 / 东欧 / 史诗 | Ilya Efimov Bayan |

### 三件套 articulation 齐备性核对

| 需求 | 免费方案 | 付费方案 | 结论 |
|---|---|---|---|
| 钢琴 半踏板 / una corda / 噪声层 | Salamander（CC64 + CC20/21 + release） | UNA CORDA、Noire Felt | 免费已基本齐 |
| 小提琴 12 奏法 + 真 legato + CC1 揉弦 | BBCSO Discover（基础 long / short / legato） | Chris Hein Solo Violin、CSS | 深度要付费才齐 |
| 手风琴 注册 / musette / bellows shake / Stradella 左手 | **基本缺失**（LABS 等免费库未覆盖） | Ilya Efimov Accordion + Accordions 2 | **免费三件套的最大缺口** |

> 落地顺序：草图用 Salamander 钢琴 + BBCSO Discover 弦乐，手风琴暂用 GM Accordion 占位；
> 成片前**必须**换掉手风琴（注册、风箱、musette 是这件乐器的情绪主体，GM 给不了），
> 再按 `sample-instrument-swap.md` 做严格 A/B 与低频重分工。
