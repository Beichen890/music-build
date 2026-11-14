# 母带

## 1. 各平台响度标准

| 平台 | 归一化目标（integrated LUFS） | 备注 |
|---|---|---|
| Spotify | **-14** | 默认 Normal；Loud=-11 / Quiet=-19 |
| Apple Music | **-16** | 唯一明显更保守的大平台；只下调不做 limiting |
| YouTube | **-14** | 始终开启，只下调不上调 |
| Tidal | -14 | 全场景专辑归一化（含歌单） |
| Amazon Music | -14 | 仅下调 |
| Deezer | **-15** | 始终开启，用户不可关 |
| Pandora | ~-14 | 唯一会**上调**安静曲目的平台 |
| SoundCloud | **无归一化** | 按原始响度播放且转 lossy，过热会削波 |

### 三条反常识但有据的认知

1. **平台只下调不上调（Pandora 例外）**——做得比目标更响没有任何收益。
2. **榜单热歌普遍远高于 -14 LUFS**，几乎都超过 -1 dBTP 的建议值。
3. **按风格定目标**才合理：acoustic/folk/jazz/classical 用 **-14 至 -16 LUFS**；
   密集电子/trap 用 **-9 至 -11 LUFS** 是正当的艺术选择。

**通用折中目标**：**-9 至 -11 LUFS integrated，true peak ≤ -1.0 dBTP**（保守用 -1.5）。

## 2. True Peak 与限幅

- **true peak 上限 -1.0 dBTP** 是最低要求；经 lossy 编码建议 **-0.3 至 -0.5 dBTP**。
- **必须开启 limiter 的 true-peak 模式**。

**为什么不能只看采样峰值**：实测中，-0.1 dBFS 未做 true peak 的母带，
经分发转 AAC 后最高 inter-sample peak 达 **+1.7 dBFS**——
在 DAW 里看着干净，实际已削波。转码会使峰值抬升 **0.5–3 dB**
（Spotify→Ogg Vorbis，Apple→AAC）。

Limiter 起点：ceiling **-1.5 dBTP**、目标 **-11 LUFS integrated**、
attack fast、release auto/fast。

## 3. 母带 EQ 顺序

**修正型处理在前，增强型在后：**

```
1. HPF 去 sub-20 Hz rumble
2. 窄切硬共振（harsh resonance）
3. 音色平衡 EQ（宽 Q / shelf 微调整体倾斜）
4. （可选）多段压缩 / 宽带压缩加 cohesion
5. 立体声展宽：只在 200–300 Hz 以上动 side
6. （可选）谐波增强
7. 最终限幅（true-peak limiter）
```

> 顺序的根据：先解决"这里不对劲"，再决定"我想让它更好听"。
> 反过来做，增强处理会掩盖问题频率，导致反复返工。

## 4. 检查项

| 指标 | 目标 |
|---|---|
| Integrated LUFS | 按平台/风格（见 §1） |
| True peak | ≤ -1.0 dBTP（保守 -1.5） |
| **LRA（Loudness Range）** | 流行/摇滚典型 **6–10 LU** |
| 段落动态 | 短于 3 秒的段落用 short-term LUFS 单独检查 |

**LRA 过高**说明段落间动态差太大（手机/车载上小声段落会听不见）；
**LRA 过低**说明压死了。

## 5. 最终验证清单

- [ ] Youlean 或同类表确认 LUFS / dBTP / LRA
- [ ] 多系统试听：监听音箱、车载、手机外放、耳机
- [ ] mono 兼容检查（correlation 不为负）
- [ ] 编码兼容检查（导出 mp3/aac 后再听一遍，确认转码没劣化）
- [ ] 与参考曲 A/B（**响度匹配后**再比，否则比的是响度不是质量）

## 6. 用参考曲母带风格自动匹配

开源工具 **Matchering**（https://github.com/sergree/matchering）可以用一首参考曲的
母带风格自动匹配你的混音，适合快速得到"和参考曲同一水准"的响度与频响。
仅作起点——它不理解你的音乐意图，最终仍需人工判断。
