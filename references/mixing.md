# 混音

## 1. 增益架构：处理顺序不能乱

```
修电平（clip gain / 音量自动化） → EQ → 压缩 → 空间效果
```

**不要用压缩去修一个本来就电平乱跳的素材。**

电平目标：
- 单轨 peak 约 **-12 至 -6 dBFS**
- bus 汇入后 mix bus peak 约 **-6 dBFS**

**A/B 时务必做响度匹配。** 很多压缩器只是把轨道变响了，
不匹配响度根本听不出真实效果。

## 2. EQ

### 顺序：减法优先 → 扫频定位 → 窄切问题 / 宽提音色

1. **HPF 先行**。除 kick 与 bass 外几乎每个元素都做 gentle HPF：

   | 元素 | HPF 起点 |
   |---|---|
   | 人声 | 80–120 Hz |
   | 吉他 | 100 Hz 以下切 |
   | Hi-hat / 镲 | 300 Hz 以下切 |

2. **扫频找问题**：把 band 增益推到 **+8 至 +12 dB、Q=6–10**，在可疑频段来回扫，
   听到最刺耳/最浑浊的点就是病灶频率。然后**反向 -2 至 -4 dB、Q=1–3** 削掉。

3. **Cut narrow, boost wide**——切问题用窄 Q，提音色用宽 Q。

4. **动态 EQ**：刺耳只在某些时刻出现时（齿音、镲片峰值），
   用动态 EQ 只在超阈值时压该频段，比静态 EQ 自然。

### 常见冲突与处方

| 冲突 | 处理 |
|---|---|
| 人声 vs 吉他 | 冲突常在 **200–400 Hz**：在吉他上 **-2 至 -3 dB / Q≈1.2**，人声侧不动 |
| Kick vs 钢琴 | 钢琴低端常 60–80 Hz 轰鸣：在钢琴 **60–80 Hz 挖 2–3 dB** |
| 人声被埋 | 人声 **2–5 kHz +2 至 +3 dB**，同时在竞争乐器同频段 **-1 至 -2 dB** |
| 低频单薄 | kick/bass **80–120 Hz +2 至 +3 dB**，并复查 HPF 是否切太狠 |

## 3. 压缩器

### 参数语义

| 参数 | 越小/越短 | 越大/越长 |
|---|---|---|
| Attack | 压掉瞬态（听感变平，失去 attack） | 放过瞬态（保留 punch） |
| Release | 紧、易抽吸（pumping） | 自然，但可能来不及回弹 |
| Ratio | 2:1 温和 glue | 4:1 控制 / 8:1+ 强限制 |

**固定顺序：先定 ratio → 再调 threshold 到目标 gain reduction。**
**release 应对齐 tempo**，常用 1/4 或 1/8 音符时长。

### 起步参数表

| 素材 | Ratio | Attack | Release | 目标 GR |
|---|---|---|---|---|
| Kick / Snare | 4:1–6:1 | 20–30 ms | 50–100 ms | 3–5 dB |
| Drum bus | 2:1–4:1 | 10–30 ms | 100–300 ms | 3–6 dB |
| Bass（E-Bass） | 4:1–8:1 | 5–30 ms | 50–200 ms | 4–8 dB |
| Synth Bass | 3:1–5:1 | 10–20 ms | 100–300 ms | 3–6 dB |
| Lead Vocal | 3:1–6:1 | 1–10 ms | 50–150 ms | 3–6 dB |
| Backing Vocal | 2:1–4:1 | 5–15 ms | 100–300 ms | 2–4 dB |
| E-Guitar clean | 3:1–6:1 | 1–10 ms | 50–150 ms | 3–6 dB |
| E-Guitar distorted | 2:1–4:1 | 5–20 ms | 100–200 ms | 2–4 dB |
| Piano | 3:1–5:1 | 5–15 ms | 100–300 ms | 3–6 dB |
| **Mix bus（glue）** | **1.5:1–2:1** | 30 ms+ | Auto / 100–500 ms | **仅 1–2 dB** |

- **侧链（sidechain）**：让 bass 在 kick 触发时瞬间让位，是"低频打架"的标准解法。
- **平行压缩**：压缩后信号与干信号混合，既控动态又保瞬态，母带和人声常用。

## 4. 混响与延迟

**混响/延迟一律用 send（aux return），不要每轨挂一个。**
这样所有元素"在同一个空间里"，省 CPU，还能在 return 上统一处理。

插入式只用于特殊效果（单轨夸张空间、reverse reverb）。

| 类型 | 衰减时间 | 用途 |
|---|---|---|
| Room / Ambience | 0.4–0.8 s | 鼓、节奏吉他，加维度不长尾 |
| Plate | 1.5–2.5 s | 流行人声、snare 的标准选择 |
| Hall | 3.0 s+ | 弦乐、pad、氛围主音 |

**预延迟（最被低估的参数）**——让主音保持"贴脸"同时拥有长尾：

- 人声：**20–60 ms**
- 鼓：**10–20 ms**（保住瞬态 punch）

**Reverb return 做 HPF 600 Hz + LPF 10 kHz**，避免低频糊和过亮刺耳。

口诀：要"贴脸但有大空间"用**短 pre-delay + 长 decay**；
要"远"用**长 pre-delay + 短 decay + 高 wet**。

延迟常用 **1/8、1/8 dotted、1/4** 对齐 tempo，dotted 1/8 是万能选择。

## 5. 声像与立体声

- **LCR 派**：kick、snare、bass、lead vocal **全部居中**；
  节奏吉他/pad/伴唱分到 **100L / 100R**；hi-hat、toms 用 30L/30R 填缝。
- **120 Hz 以下 mono**，用 mid/side 工具把 low band 的 side 收干。
- **Mono 兼容检查**：用 correlation meter，读数在 +1 到 0 之间，
  **不应低于 0**，否则 mono 播放会相位抵消。
- **每个混音阶段都 collapse 到 mono 听一遍**。

## 6. 诊断表

| 症状 | 病因 | 处方 |
|---|---|---|
| **浑浊 muddy** | 200–500 Hz 堆积 | 节奏吉他/synth 在 **150–400 Hz 减 2–3 dB**；除 kick/bass 外全部 HPF 80–120 Hz |
| **轰 boomy** | 低频单频共振 | 找 kick/bass 重叠点，一方减 2–3 dB；检查 60–120 Hz |
| **盒音/鼻音 boxy** | 400–800 Hz 堆积 | 人声/乐器 **400–800 Hz 窄切 2–4 dB** |
| **刺耳 harsh** | 2–4 kHz 过多 | **2–4 kHz 减 2–4 dB**，先用窄 Q 扫出精确频率 |
| **齿音重 sibilant** | 5–8 kHz | 用 **de-esser** 而非宽带高频减；lossy 转码会放大此问题 |
| **单薄 thin** | 低频被 HPF 太狠 | kick/bass **80–120 Hz +2 至 +3 dB**，复查 HPF |
| **高频糊** | 混响过多 / return 低频 | reverb return HPF 600 Hz；缩短 decay；降 wet |
| **动态死 lifeless** | 压缩过量 / 母线过度限制 | 降 GR 至 1–2 dB；用平行压缩替代串联重压；A/B 匹配响度验证 |
| **人声被埋** | 2–5 kHz 被抢 | 人声 +2 至 +3 dB，竞争乐器同频 -1 至 -2 dB |

## 7. 混音顺序总表

```
1. 修电平（clip gain / 自动化）
2. HPF 每个元素
3. 扫频找病灶 → 窄切
4. 需要时上动态 EQ
5. 压缩（先 ratio 后 threshold）
6. send 混响/延迟（人声 pre-delay 20–60 ms）
7. 声像（LCR + 120 Hz 以下 mono）
8. 按诊断表对症处理
9. mono 检查 + 多系统试听
```
