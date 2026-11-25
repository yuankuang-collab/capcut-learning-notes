---
name: github-collaboration-guide
display_name: GitHub 协作指南
display_name_en: GitHub Collaboration Guide
description: 讲解 GitHub 仓库/分支/提交/拉取请求工作流与 GitHub Skills 交互课程，指导开 PR、审查 PR、建议更改、解决协作问题。当用户询问 GitHub 怎么建分支、提 PR、合并、审查代码、学 GitHub 或找 GitHub Skills 课程时触发。
description_zh: 基于 GitHub 官方文档 Hello World 与 GitHub Skills 课程整理的协作知识库，覆盖 PR 工作流与审查方法。
description_en: A collaboration knowledge base built from GitHub's official Hello World guide and GitHub Skills courses, covering pull request workflows and reviews.
examples_zh:
- "怎么在 GitHub 上开一个 pull request"
- "审查 PR 时怎么给出修改建议"
- "GitHub Skills 有哪些入门课程"
examples_en:
- "How do I open a pull request on GitHub"
- "How do I suggest changes during a pull request review"
- "What beginner courses does GitHub Skills offer"
version: 1.0.0
author: yuankuang-collab
---

# GitHub 协作指南

当用户询问 GitHub 协作流程、拉取请求、分支管理或 GitHub Skills 课程时，使用本技能。

## 使用方式

1. 判断问题类型，读取对应参考文件（用 `@references/文件名` 引用）：
   - 创建仓库、分支、提交、打开与合并 PR、网页与命令行对照 → `@references/hello-world.md`
   - GitHub Skills 平台机制、课程地图、PR 审查方法与建议更改 → `@references/github-skills.md`
2. 回答时区分来源：【官方】表示来自 GitHub 文档或课程仓库原文；【整理】表示结合实操经验的归纳。不要把整理内容说成官方规定。
3. 按钮名称以用户访问时的 GitHub 界面（中文/英文）为准；官方课程会更新，课程列表以 <https://skills.github.com/> 实时页面为准。
4. 不编造 GitHub 未提供的功能或课程名；资料里没有的明确说未知。

## 资料来源

GitHub 官方文档《Hello World》<https://docs.github.com/zh/get-started/start-your-journey/hello-world>、GitHub Skills <https://skills.github.com/> 及各课程仓库的 README 与 `.github/steps/` 步骤文件。整理日期 2026-11-25。

## 边界

本技能收录的是文档知识，不包含可执行的 GitHub 写操作。实际读写仓库需通过用户已授权的 GitHub 连接器或用户自己的终端完成。
