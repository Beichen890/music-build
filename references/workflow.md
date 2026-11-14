# 工作流、工程规范与 MIDI 制作

## 1. 工程基础参数

| 项目 | 取值 | 依据 |
|---|---|---|
| 采样率 | **44.1 kHz**（纯音频发行）/ **48 kHz**（含视频、影视交付） | 全程保持**单一原生采样率**，不要中途重采样 |
| 位深 | 混音工程 **24-bit** | 约 144 dB 动态余量，内部处理无顾虑 |
| 位深降低 | 仅在最终降至 16-bit 时加 dither | 这是唯一需要 dither 的环节 |
| 缓冲 | 录制 128–256 samples；混音 1024+ | |

**响度纪律（做工程时就要守）：**
- 混音母线峰值 ≤ **-6 dBFS**，给母带留 3–6 dB。
- 全程 true peak 控制在 **-3 dBFS** 以下。
- **对齐参考曲时用 LUFS，不要用 peak。**

## 2. 工程组织

**轨道命名公式**：`序号_乐器_作用`
```
01_DRUM_kick      12_SYN_pad_warm
02_DRUM_snare     20_VOX_lead
10_BASS_sub       21_VOX_harmony
```
禁止保留 `Track 1` / `Audio 1`。

**分组母线固定四组**，各挂一条 bus 处理，再汇入 mix bus：
```
DRUMS / BASS / MUSIC / VOX  →  MIX BUS
```
混音时做的是 bus 压缩，不是逐轨乱压。

**版本命名**：`SongName_v01_rough` → `v05_mix` → `v09_master`。大改存新版本，不要覆盖。

> openDAW 用户注意：浏览器 DAW 的工程存在 IndexedDB，**不能当作持久存储**，
> 要定期往本地导出/备份。

## 3. 导出格式

| 用途 | 格式 |
|---|---|
| 母带交付 | 24-bit WAV，44.1/48 kHz，true peak ≤ -1 dBTP |
| 流媒体上传 | 同母带（平台自行转码） |
| 试听分享 | 320 kbps MP3 或 256 kbps AAC |
| 发给混音师的分轨 | 24-bit WAV，**全部从 0:00 对齐**，备注是否已带处理 |

## 4. MIDI 制作

### 4.1 人性化

1. **力度浮动**：不要全 127 或全 100。围绕基准值 **±10–20** 浮动；
   重音拍（1、3）比弱拍（2、4）高 **10–15**。
2. **时值微调**：整体前移/后移几毫秒做 laid-back 或 push 感；
   个别音符随机偏移 **±5–15 ticks**（PPQN=960 时约几毫秒）。
   **只对人手演奏的音域做，鼓的 kick 要对齐网格。**
3. **量化取舍**：
   - 鼓、bass 骨架 → 量化到 1/16，或加 swing 55–62%
   - 和弦、pad、弦乐 → 部分量化（50–80%）或不量化
   - 主旋律 → 不量化或轻量化
4. **力度要画弧线**：很多音源按力度切换采样层，平铺的力度会触发同一层，动态扁平。
5. **避免机器感三宗罪**：所有音符等力度、所有音符卡网格、所有和弦同一起音
   （和弦可用 5–30 ms 的 strum 错开）。

### 4.2 GM 音色表要点

**128 个旋律音色**分 16 组：Piano(1–8)、Chromatic Percussion(9–16)、Organ(17–24)、
Guitar(25–32)、Bass(33–40)、Strings(41–48)、Ensemble(49–56)、Brass(57–64)、
Reed(65–72)、Pipe(73–80)、Synth Lead(81–88)、Synth Pad(89–96)、Synth Effects(97–104)、
Ethnic(105–112)、Percussive(113–120)、Sound Effects(121–128)。

**通道 10 专用于打击乐**，该通道内音高代表不同鼓件。

**GM 鼓映射关键音高**（范围 35–81，共 47 件）：

| 音高 | 鼓件 | 音高 | 鼓件 |
|---|---|---|---|
| 35 | Acoustic Bass Drum | 46 | Open Hi-Hat |
| **36** | **Bass Drum 1（kick）** | 49 / 57 | Crash |
| 37 | Side Stick | 51 / 59 | Ride |
| **38** | **Acoustic Snare** | 53 | Ride Bell |
| 39 | Hand Clap | 54 | Tambourine |
| 40 | Electric Snare | 56 | Cowbell |
| 41/43/45/47/48/50 | Toms | **42** | **Closed Hi-Hat** |

> **音符命名陷阱**：Note 60 在 Cubase/Ableton/Logic 叫 **C3**，
> 在多数其他 DAW 和 GM 标准叫 **C4**。跨 DAW 交换 MIDI 后"鼓件错位"，
> 十有八九是这个原因。

**常用 CC**：CC1 Modulation、CC7 Channel Volume、CC10 Pan、CC11 Expression、CC64 Sustain。

### 4.3 MIDI 常见坑

- 忘了切 drum map，kick 打到 cowbell 上
- 用 GM 音色做正式编曲（GM 只适合打谱/草图，成片要换真实音源）
- 导出时丢了 tempo / 拍号变化，重新导入后节拍全乱
- 力度全 100，音源只触发中间采样层
- 没做 velocity → filter/volume 映射，表情控制失效

### 4.4 用 GM 之外的选择

GM 音色干净但廉价。要提升质感，优先换掉三样：**鼓、贝斯、主音色**。
免费方案见 `resources.md`。
