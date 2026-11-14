# 电子舞曲 / 吵闹电子风格（独立存档）

> **本文件是隔离区，不是主线。** 默认创作路径 = 情绪驱动 + 场景感双轴 + 三件套（钢琴 / 小提琴 / 手风琴），**全程在 DAW 里完成**：MIDI + 采样音源 + 合成器 + 自动化 + 混音。
> **合成器是正常音色来源，不归本文件管。** 只有明确要做「吵的电子风格」时才读这里：EDM / House / Techno / Trance / Dubstep / Trap / Drum & Bass / Phonk、鼓机 drop、riser、侧链泵感、supersaw lead。
> 要用合成器做**梦幻 / 神秘 / 空灵 / 宏大 / 悲壮**但不想要舞曲感 → 走 `scene-texture-recipes.md`，别读这里。
> 数值是起点不是法则，以耳朵为准；【经验】= 业界惯例，可放心改。

---

## 0. 判据与分流

**判据不是「有没有用合成器」，而是「骨架是不是鼓机 + drop + 循环能量爬升」。**
用合成器弹卡农、铺弦乐底、做氛围 pad、写 soft lead，都属于主线，不受本文件约束。

| 需求 | 去哪 |
| --- | --- |
| 用合成器 pad / bell / soft lead 铺氛围，服务情绪与场景感 | `scene-texture-recipes.md`、`emotion-arrangement-recipes.md` |
| 选免费合成器 / 采样器 / 鼓音源（作为普通音色工具） | `resources.md`「免费合成器 / 采样音源」 |
| 做 EDM / House / Trap 这类以鼓机与 drop 为骨架的曲子 | 本文件 |
| 在 DAW 里写 MIDI、画 CC、做自动化 | `workflow.md`、`audio-transcript-notes.md` §2 |
| 三件套 + 合成器混合编制的频率让位 | `core-instruments.md`、`arrangement.md` §3 |

---

## 1. 结构（自 `arrangement.md` 迁出）

| 段落 | 长度 (bars) | 职能 | 手法 |
| --- | --- | --- | --- |
| Intro | 16–32 | 留混接空间、逐步立 tempo | 底鼓先入，每 8 小节加一层，不带满编 |
| Build-up | 8–16 | 累积张力 | riser / 白噪上升 / snare roll 加速 / 逐步 HPF 扫频 / 抽掉 bass |
| Drop | 16–32 | 纯器乐能量爆发 | 精简后回填 full drums + bass + lead；第一拍留 1 拍静音更狠 |
| Breakdown | 16–32 | 情绪中心 | 剥到 pad + vocal，再重建 |
| Outro | 8–16 | 退场 / 混接 | 逐层抽走，尾留可 loop 的 4 小节 |

**4 小节递进法**【经验】：drop 在第 64 小节，则 48 / 56 / 60 逐级加码（加层 → 加密 → 加亮），第 63 小节达到最大张力，第 64 小节全放。
相邻段落能量值必须不同（drop 8–10、breakdown 2–3）；满编时段不超过全曲 30–40%。

---

## 2. 纯器乐电子曲（自 `instrumental-production.md` §7.6 迁出）

- **没有唱词时，drop 的记忆点必须由 lead 音色自己承担**：lead 的分层（主音 + 和声层 + 宽度 + 侧链闪避）比旋律本身更重要。
- 鼓组是「主唱」：kick / snare 的音色选择就是这首歌的嗓音。
- 音色设计优先于旋律写作：先做出一个「没听过但想再听」的 lead，再给它写旋律。
- 必查 mono 兼容：supersaw / wide bass 在手机单声道下会不会塌。
- 循环结构：4 / 8 小节 loop 靠音色分层进出制造段落，首尾要做成能无缝接起来。
- 前 15–30 秒决定完播率，核心音色或主题必须在开头出现一次。

---

## 3. 常用手法与数值【经验】

| 手法 | 参数起点 | 用途 |
| --- | --- | --- |
| 侧链闪避 (sidechain ducking) | kick 触发 pad/bass 压 2–4 dB，attack 1–5 ms、release 100–250 ms（跟 1/8 或 1/16 走） | 给 kick 让位、制造泵感 |
| Ambient pad 轻闪避 | ducking 2–3 dB，release 300–500 ms | 不吵的前提下的「呼吸」，主线也可用 |
| riser / 白噪上升 | 最后 2–4 小节，带宽 200 Hz → 12 kHz 扫、音量 +6 dB | build-up 张力 |
| 滤波自动化 (filter LFO) | pad 低通 800 Hz → 4 kHz，周期 8–16 小节，速率 0.05–0.1 Hz | 静止织体也能「呼吸」 |
| 808 / sub bass | 40–80 Hz 为主，轻微饱和让手机听见泛音；120 Hz 以下保持 mono | 低频纪律同主线 |
| supersaw | 7–9 个 saw 声部、detune ±8–15 cent，展宽只在 120 Hz 以上做 | lead 宽度 |
| 鼓组 swing | hat 微晚 10–20 ms、snare 微晚 5–15 ms | Lo-fi / Chillhop 松弛感 |
| 磁带 / 降采样做旧 | 12-bit 风味、高频 roll-off <10–12 kHz、黑胶噪音 | Lo-fi 质感 |
| 多段上下压缩 (OTT 类) | 轻混 10–25%，别默认挂全轨 | 电子制作招牌染色 |

---

## 4. 分风格速查

| 风格 | BPM | 骨架 | 关键一件 |
| --- | --- | --- | --- |
| House | 120–130 | 4/4 底鼓 + offbeat hat/clap | 摇摆的 bassline 与和声 loop |
| Techno | 125–150 | 机械 4/4、极少和声变化 | 音色与滤波的长时间演变 |
| Trance | 130–145 | 长 build-up + 分解和弦 arp | 一个延展的 supersaw lead |
| Dubstep | 140（半速 70） | 半拍 wobble bass + 重 snare | LFO 调制 bass 的节奏型 |
| Trap / Phonk | 60–80（半速 140–160） | 808 + 密集 hi-hat roll | 808 滑音与 hat 三连音 |
| Drum & Bass | 160–180 | 切分 breakbeat + sub | Amen break 的重排 |
| Lo-fi / Chillhop | 70–90 | 软 kick + swing + maj7/m7/9 | 磁带饱和与留噪音「喘息」 |

---

## 5. 与主线的接口：不吵但用合成器

用户主用途是情绪驱动的三件套叙事，合成器在这里的角色是**色彩与空间**，不是舞曲骨架：

| 场景感 | 合成器用法 | 边界 |
| --- | --- | --- |
| 梦幻 S01 | 慢起音 pad、长混响 3–5 s RT60、轻微合唱 | 不加 riser、不加 drop |
| 神秘 S04 | 低通缓慢扫动、无调性纹理、极弱奏（pp–mp） | 不用 wobble / 密集 hat |
| 空灵 / 圣洁 | bell / glass 音色叠原声钟琴 | 保持留白，别铺满 |
| 宏大 S02 / 悲壮 S03 | pad 垫在弦乐下面补 200–500 Hz 厚度，音量比弦乐低 6–10 dB | 合成器不抢前景，不作主奏 |
| 黎明 | pad RT60 从 3.0 s 自动化降到 1.5 s | 用空间变化而非能量爬升 |

> 完整六大杠杆（音区 / 织体 / 和声色彩 / 空间 / 动态 / 时间形状）见 `scene-texture-recipes.md`。
> **裁決**：情绪定调式与弧线，场景感定音区与空间；电子舞曲手法与这两轴冲突时，一律让位。

---

## 6. 工具

免费合成器、采样器、鼓音源、效果器清单见 `resources.md`（Vital / Surge XT / Dexed / OB-Xd / Helm / Spitfire LABS / Decent Sampler / MT Power Drum Kit 2 / Sitala / OTT / Valhalla Supermassive 等）。
这些工具在主线里同样是合法音色来源，不因列在本文件指针里而被视为「只做电子风格」。

> **来源说明**：本文件由技能原有 `arrangement.md` §1、`instrumental-production.md` §7.6 / §4.1 / §5、`resources.md` 的电子相关条目归拢而成，均为通用制作惯例【经验】，未编造 B 站 BV 号或出处。
