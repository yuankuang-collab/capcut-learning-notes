# AI 视频提示词：Runway 官方指南

> 来源：Runway 官方帮助中心（针对 Gen-4.5）。三篇正文均已打开核实（【一手-已核实】）。整理 2026-11-26。
> 注意：文生视频指南正确链接是 `articles/42460036199443`（我抽查时修正了调研给的错误 ID）。

---

## 1. Introduction to Prompting

<https://help.runwayml.com/hc/en-us/articles/46182941379347>

- **心法**：把提示词当给同事的创意指导，但模型**更字面、缺乏共享语境**——「a beautiful landscape」对模型是随机的。
- **迭代三步**：`A serene pond with koi fish` → `High angle looking down at a serene pond` → `+ A koi fish emerges and breaches the surface, sending gentle ripples through the lily pads`。
- **两种策略**：Simple（快、给模型自由、适合探索）vs Detailed（减少歧义、跨次一致、适合明确需求）；**详细≠永远更好**。
- **五问法加细节**：Who / What / When / Where / How；目标是消除歧义，不是控制每个像素——过度具体反而产出不自然结果。
- **三条最佳实践**：
  - 正向表述：✅ `sharp focus, high detail` / ❌ `not blurry`
  - 避免模糊概念词：✅ `a sunset with vibrant orange and pink clouds` / ❌ `a beautiful sunset`
  - 避免冲突指令：❌ `dramatic shadows with soft, even lighting` / ✅ `dramatic shadows with strong directional light`
- **JSON 提示词只是安慰剂效应**，模型忽略格式，真正起作用的是内容细节。

## 2. Text to Video Prompting Guide

<https://help.runwayml.com/hc/en-us/articles/42460036199443>

- **两类核心元素**：Visual（主体外观、环境、光线、构图/取景、风格）+ Motion（主体动作、环境运动、摄影机运动、运动风格与时机、方向与速度）。
- **官方公式**：
  ```
  [Camera] shot of [a subject/object] [action] in [environment]. [Supporting component descriptions]
  ```
  例：`Medium shot of a cowboy perched on a horse in a dusty environment. The horse rears violently... Backlit, western epic, cinematic, golden hour...`
- 自然语言通常比关键词更可控；元素**出现顺序不重要**，关键是清晰、减少歧义。
- 长度无理想值，重清晰不重字数；T2V 通常比 I2V 长，但过长会产生冲突请求。
- **Timestamp prompting**：`[00:00 through 00:02] looking away, then turns towards camera` / `[00:02 through 00:03] rapidly crash zoom to eyes`；与自然语言配合最佳；按动作合理耗时设定（走完房间 00:00–00:03，不是 00:00–00:00.5）。
- T2V 优势：不需先出图，适合 B-roll、素材特效、背景板；不受起始画面约束，能处理复杂运动序列。

## 3. Image to Video Prompting Guide

<https://help.runwayml.com/hc/en-us/articles/48324313115155-Image-to-Video-Prompting-Guide>

- **分工原则**：输入图作为**首帧**提供构图、主体、光线、风格；提示词**几乎只描述运动**，不重复画面已有的东西。
- **官方公式**：
  ```
  The camera [motion description] as the subject [action]. [Additional descriptions]
  ```
  例：`The camera slowly pushes in as the person scales the giant soda.`
- 运动五组件：主体动作、环境运动、摄影机运动、运动风格与时机、方向与速度。
- 需要写视觉描述的例外：引入图中没有的元素 / 相对起始图的大幅变化 / 指定变形细节 / 指定两个以上元素互动。
- **Sequential prompting**：`X occurs, then Y. Finally Z.` 或 `[00:01] X. [00:03] Y. [00:04] Z.`
- **做长片**：取已完成片段的**最后一帧**作为新生成的输入图（播放器拖到末尾 → Use → Use current frame），最后在剪辑软件合并两段并删掉重复帧。
- 两个坑：
  - 图中隐含运动线索（运动模糊、尘云）会与「静止」指令冲突，需先清除；
  - 想减少运镜就明写 `The locked-off camera remains perfectly still.` 或 `The camera must start and end on the exact same frame to create a perfect loop.`
- 出现不想要的切镜：增加 duration；仍有问题就加 `Continuous, seamless shot`。

---

## 边界

以上为 Runway Gen-4.5 官方文档要点，其他模型（即梦 Seedance、可灵、Sora 等）结构类似但参数与可用性不同；跨模型使用请查对应官方文档。
