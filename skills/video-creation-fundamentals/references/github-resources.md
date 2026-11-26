# GitHub 视频创作资源索引

> 全部条目经 GitHub API 读取 README 核实（调研任务）；带 ★ 的 7 个仓库经我二次抽查 star/许可证一致。star 为 2026-11-26 实时值，会变化。整理 2026-11-26。

---

## A. 提示词库（取用模板）

| 仓库 | Star | 许可 | 用途 |
| -- | -- | -- | -- |
| ★ [ai-boost/awesome-image-video-prompts](https://github.com/ai-boost/awesome-image-video-prompts) | 3,531 | GPL-3.0 | 按模型分章，每条含效果图+完整 prompt+来源+点赞；结构示范「主体→服装→环境光线→镜头语言→画质参数」 |
| ★ [ZeroLu/awesome-seedance](https://github.com/ZeroLu/awesome-seedance) | 2,882 | MIT | 分镜式模板 `[00-05s] Shot 1:` + 场景 + 动作 + Dialogue Cue；七类用途；六语 README |
| ★ [LearnPrompt/awesome-seedance](https://github.com/LearnPrompt/awesome-seedance) | 2,658 | MIT | 1,109 案例 + 494 次跨模型复测 + 27 模板 + 85 Skill；**5 步上手**：选模板→复制→替换 `[括号]`→让 AI 补全→粘贴生成 |
| [UnderleveledBuilder/awesome-short-drama-skills](https://github.com/UnderleveledBuilder/awesome-short-drama-skills) | 2,883 | CC0-1.0 | 121 skill + 16 平台，按「选题→剧本→骨架→分镜→视频提示词」组织；盲测对照评估并公开局限 |
| [geekjourneyx/awesome-ai-video-prompts](https://github.com/geekjourneyx/awesome-ai-video-prompts) | 92 | MIT | 系统教程；**电影语言模块**把景别/运镜/构图转成 prompt 词；含各模型官方指南索引 |

## B. 剪辑与自动化工具

| 仓库 | Star | 许可 | 用途 |
| -- | -- | -- | -- |
| ★ [Zulko/moviepy](https://github.com/Zulko/moviepy) | 15,213 | MIT | Python 剪辑库，帧转 numpy 像素级可控；v2 链式写法；v1 已停维护 |
| ★ [harry0703/MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo) | 145,799 | MIT | 端到端：主题→脚本→素材→字幕→BGM→合成；WebUI + API |
| ★ [OpenMontageInc/OpenMontage](https://github.com/OpenMontageInc/OpenMontage) | 83,516 | AGPL-3.0 | AI 编程助手变视频工作室；真实动态片段工作流；公开成本 60 秒约 $1.33；Veo/Kling + Remotion 合成 |
| [GuanYixuan/pyCapCut](https://github.com/GuanYixuan/pyCapCut) | 790 | 未显示 | 生成/编辑剪映草稿；模板模式替换素材/文本保留特效；支持 SRT、关键帧、转场、花字、混合模式 |
| [hclivess/whisperer](https://github.com/hclivess/whisperer) | 85 | MIT | Whisper 批量字幕 GUI；3 遍校验抗幻觉；按 VAD 对齐；字幕重同步 |

## C. 创作工作流

| 仓库 | Star | 许可 | 用途 |
| -- | -- | -- | -- |
| ★ [LudwigKienle/ai-video-production-editor](https://github.com/LudwigKienle/ai-video-production-editor) | 194 | GPL-3.0 | 本地工作站全流程；**按镜头选模型 Auto 路由**；3D previs；导出恢复原始音轨 |
| [sirioberati/Genjustsu-Open-Source-Workflow](https://github.com/sirioberati/Genjustsu-Open-Source-Workflow) | 1,679 | MIT | 主体替换工作流；两阶段生成先草稿预览再 1080p 控成本 |
| [coleam00/hyperframes-ai-video-generation](https://github.com/coleam00/hyperframes-ai-video-generation) | 160 | 未显示 | 一条命令出竖屏 Short；调研→旁白→TTS→合成→预览，渲染手动 |
| [MushroomFleet/DJZ-Workflows](https://github.com/MushroomFleet/DJZ-Workflows) | 120 | 未显示 | 1,000+ ComfyUI 工作流，每个配套教程 |
| [qzw881130/AI-NovelFlow](https://github.com/qzw881130/AI-NovelFlow) | 124 | NOASSERTION | 小说转视频全链路；⚠️ 原版停维护，V2 付费开源（50 元），以归档原版为准 |

## D. 学术/全景清单

| 仓库 | Star | 用途 |
| -- | -- | -- |
| [showlab/Awesome-Video-Diffusion](https://github.com/showlab/Awesome-Video-Diffusion) | 5,854 | 视频扩散模型学术清单，单列评估基准章节 |
| [AlonzoLeeeooo/awesome-video-generation](https://github.com/AlonzoLeeeooo/awesome-video-generation) | 796 | 按任务×年份组织论文，追踪演进 |
| [jianzhnie/awesome-text-to-video](https://github.com/jianzhnie/awesome-text-to-video) | 758 | 产品对比表 + How to Choose 选型；归档停服产品 |

---

## 选型速查

- 想学提示词写法 → LearnPrompt/awesome-seedance 的 5 步法 + geekjourneyx 的电影语言模块
- 要自动剪素材 → moviepy（代码可控）/ pyCapCut（直接生成剪映草稿）
- 要自动字幕 → whisperer（抗幻觉、可重同步）
- 要理解完整生产流程 → LudwigKienle/ai-video-production-editor + coleam00/hyperframes
- 要建立技术视野 → showlab/Awesome-Video-Diffusion + jianzhnie/awesome-text-to-video

## 边界

star、许可证、更新时间会变化，决策前打开仓库确认；许可证（尤其 GPL/AGPL/CC0）影响商用与二次分发，使用前自行核对。本索引只做学习与参考，不构成工具推荐背书。
