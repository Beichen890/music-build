# music-build — 音乐制作全流程知识与参数级操作指南

面向独立创作者与 AI agent 的音乐制作知识库。**核心原则：所有建议都给可执行的数值和顺序，
不给"要合理使用 EQ"这种废话。**

覆盖编曲配器、混音、母带、MIDI 制作、纯音乐（器乐）写作、情绪表达与参考曲逆向分析。
环境假设为 Windows + DAW（含浏览器 DAW）+ MIDI 工具链 + 采样音源 + 合成器；
吵闹电子舞曲风格单独放在 `references/electronic-styles.md`。

## 什么时候用

- 用户描述的是**情绪 / 画面 / "某种感"**而不是技术需求（"想写那种宏大的悲伤""要梦幻一点""要悲壮"）→ 走情绪驱动工作流
- 要做一段音乐、编曲、混音、母带、导出成品
- 描述听感问题（浑浊 / 刺耳 / 单薄 / 糊 / 动态死 / 人声被埋）
- 给出参考曲说"我要这种效果" → 走参考曲逆向分析流程
- 问和弦怎么走、有哪些万能和弦、音程调式、乐器音域、选哪套音源、钢琴/小提琴/手风琴怎么写
- 问去哪系统学编曲（B 站学习地图 + 抽帧谱例 + 口述转写笔记）

## 仓库结构

```
SKILL.md                         技能入口：何时使用 + 工作流路由 + 核心流程
references/
  编曲与写作
    arrangement.md               编曲配器总纲
    arrangement-philosophy.md    编曲哲学：留白、层次、主次
    classic-arrangement.md       经典编曲手法
    core-instruments.md          钢琴 / 小提琴 / 手风琴三件主体乐器写法
    instrumental-production.md   纯音乐（器乐）制作
    loop-and-rhythm.md           律动与 loop 设计
    melody-revision.md           旋律修改流程
    sample-instrument-swap.md    采样与音源替换
  和声与乐理
    chord-library.md             可复用和弦库
    theory-cheatsheet.md         乐理速查（音程 / 调式 / 音域）
    emotion-chord-index.md       情绪 → 和弦索引
  情绪与场景
    emotional-expression.md      情绪表达方法
    emotion-arrangement-recipes.md  按情绪分类的编曲配方
    scene-texture-recipes.md     场景与感受塑造配方（梦幻/宏大/悲壮/神秘）
    scene-emotion-matrix.md      情绪 × 场景组合矩阵
  风格
    electronic-styles.md         EDM / House / Techno / Trap / drop
  混音与母带
    mixing.md                    混音
    mastering.md                 母带
    stem-mix-pipeline.md         分轨混音流水线
  分析与资料
    reference-analysis.md        参考曲逆向分析
    frame-notes.md               抽帧谱例与口述转写笔记
    bilibili-study-map.md        B 站学习地图
    bilibili-up-map.md           UP 主 / 教程索引
    audio-transcript-notes.md    音频转写笔记
    instrument-libraries.md      音源与采样库选型
    lmms-tone-libraries.md       LMMS 音色库
    resources.md                 外部资源
    workflow.md                  完整工作流
```

## 与其他仓库的关系

- [lmms-cli](https://github.com/Beichen890/lmms-cli) — 把本仓库的知识落地成可执行命令的 LMMS 无头 CLI
- [music-mixing-craft](https://github.com/Beichen890/music-mixing-craft) — 混音维度的深挖版（频率掩蔽、动态让位、空间深度、诊断清单 + 声场规划脚本）

## 使用方式

`SKILL.md` 的 frontmatter 符合 Agent Skill 规范，可整体放进 agent 的 skills 目录直接加载；
也可以纯当文档读——所有 `references/` 都是独立的 Markdown，按需检索，不需要顺序阅读。
