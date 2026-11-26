---
name: video-creation-fundamentals
display_name: 视频创作能力进阶
display_name_en: Video Creation Fundamentals
description: 提供可迁移的视频创作能力——叙事结构、分镜与镜头语言、剪辑节奏（J/L-cut）、调色流程、AI 视频提示词官方公式，以及可复用的 GitHub 工具与模板库。当用户问怎么写脚本/分镜、怎么让剪辑更自然、怎么调色、AI 视频提示词怎么写、有哪些视频生成提示词库或剪辑工具时触发。
description_zh: 基于 StudioBinder、DaVinci Resolve 官方教材、Runway 官方帮助中心与 GitHub 高星仓库整理的创作方法论与资源库，补足「为什么这样拍/剪/写提示词」的上游能力。
description_en: A methodology and resource library built from StudioBinder, DaVinci Resolve official guide, Runway help center and high-star GitHub repos, covering storytelling, storyboarding, editing rhythm, color grading and AI video prompting.
examples_zh:
- "短视频脚本怎么安排结构，三幕结构怎么用"
- "分镜脚本每一格要标注什么"
- "J-cut 和 L-cut 怎么用，能让剪辑更自然吗"
- "调色的正确顺序是什么，一级和二级调色怎么分"
- "Runway 文生视频提示词怎么写，有公式吗"
- "有哪些 Seedance 提示词模板仓库可以借鉴"
examples_en:
- "How to structure a short video script with three acts"
- "What should each storyboard panel specify"
- "How to write prompts for AI video generation"
- "Recommend GitHub repos for video prompt templates"
version: 1.0.0
author: yuankuang-collab
---

# 视频创作能力进阶

当用户的问题超出「某个软件按钮怎么点」，涉及创作方法、镜头语言、剪辑节奏、调色思路、AI 提示词写法或工具选型时，使用本技能。

## 使用方式

1. 按问题类型读取参考文件（用 `@references/文件名` 引用）：
   - 叙事结构、分镜标注、镜头角度如何服务叙事、J/L-cut 剪辑节奏 → `@references/story-and-editing.md`
   - 调色顺序、一级/二级调色、量化标准 → `@references/color-grading.md`
   - AI 视频提示词官方公式（T2V/I2V）、迭代策略、时间戳 → `@references/ai-prompts-official.md`
   - GitHub 提示词库、剪辑工具、工作流仓库、选型建议 → `@references/github-resources.md`
2. 回答时保留来源等级标注：【一手-已核实】【一手-未抽查】【仅摘要】。属于【仅摘要】的内容要说明未读正文、仅供参考。
3. 具体参数（时长、页码、star 数、价格）注明获取日期与「以官方/实时页面为准」；star 数与价格会变化。
4. 不要编造 URL、仓库名或数值；资料里没有的明确说未知。

## 资料来源

StudioBinder 创作学院、Blackmagic Design《The Colorist Guide to DaVinci Resolve 20》官方 PDF、Runway 官方帮助中心（Gen-4.5）、GitHub 高星仓库（2026-11-26 API 核实）。整理日期 2026-11-26。

## 边界

本技能收录方法论、提示词模板与工具索引，不含视频原片，也不执行剪辑或 GitHub 写操作。需要逐帧教学时给出对应课程/文档链接。与 `capcut-video-guide` 的分工：本技能管「为什么这样拍/剪/写」，那个技能管「剪映/即梦具体按钮怎么点」。
