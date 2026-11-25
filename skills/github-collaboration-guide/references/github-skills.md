# GitHub Skills 课程与 PR 审查

来源：GitHub Skills <https://skills.github.com/> 及各课程仓库（`skills/*`）的 README 与 `.github/steps/` 步骤文件。整理日期 2026-11-25。

## GitHub Skills 平台机制【官方】

GitHub Skills 是 GitHub 官方的**交互式课程平台**：课程以仓库形式提供，把课程仓库用模板复制到自己账号，等约 20 秒让 GitHub Actions 准备好第一节课，刷新页面后按仓库里自动创建的 issue 步骤操作，Mona（章鱼猫）自动检查进度并放出下一步。

启动流程：打开课程仓库 → **Use this template → Create a new repository** → Owner 选自己账号、建议选 Public（私有仓库消耗 Actions 分钟数）→ 等约 20 秒刷新 → 按 issue 步骤操作。若没准备好，到 **Actions** 标签查看任务是否在运行；失败则官方建议提交 issue 报 bug。

## 官方课程地图【官方】

**第一天**：Introduction to GitHub（不到一小时上手 GitHub）、Communicate using Markdown（用轻量标记语言组织想法、协作沟通）、GitHub Pages（从仓库创建网站或博客）。

**第一周**：Introduction to Git（用命令行和 VS Code 在 Git 下做游戏）、Review pull requests（在 GitHub 上协作）、Resolve merge conflicts（理解冲突并解决）、Code with Codespaces、Introduction to Repository Management。

**GitHub Copilot**：Getting Started with GitHub Copilot、Customize your GitHub Copilot Experience、GitHub Copilot Code Review、Integrate MCP with GitHub Copilot、Expand your team with Copilot coding agent、Create Applications with the Copilot CLI、Modernize your legacy code with GitHub Copilot、Scale institutional knowledge with GitHub Copilot Spaces、Build applications with GitHub Copilot agent mode、Agentic Workflows that Read the Room、Agent Orchestration Build Your AI Dream Team、Idea to Merge with the Copilot App。

**GitHub Actions**：Hello GitHub Actions、Test with Actions、Write JavaScript Actions、Publish Docker Images、Create and use reusable workflows、Work with Workflow Artifacts。

**代码安全与分析**：Secure your repository supply chain、Introduction to CodeQL、Introduction to secret scanning、Secure code game、Ship with Quality。

**迁移到 GitHub**：Migrate an Azure DevOps Repository。

课程列表以 <https://skills.github.com/> 实时页面为准。

## Review pull requests 课程【官方】

课程页面：<https://github.com/skills/review-pull-requests>。先决条件：熟悉提交、创建分支和 PR；时长不到 30 分钟。六项活动：打开 PR → 分配给自己 → 留下审查 → 建议更改 → 应用更改 → 合并 PR。

### PR 的四个标签页

| 标签页 | 作用 |
| -- | -- |
| Conversation（对话） | PR 活动的整体日志和开放的讨论空间 |
| Commits（提交） | 只列出该提议分支独有的提交 |
| Checks（检查） | GitHub Actions 施加的自动化检查结果 |
| Files changed（更改的文件） | Diff 视图，前后对照显示改动，可在具体行上添加评论和审查 |

提示：未完成的工作可创建 **draft pull request（草稿 PR）**，避免误合并或过早审查。

### 三种审查反馈

- **Comment（评论）**：一般反馈，不代表批准或拒绝
- **Approve（批准）**：在规则集、代码所有者等策略允许时可合并
- **Request Changes（请求更改）**：改动不满足预期、需要更多工作；修改后应重新请求审查

注意：不能对自己的 PR 选择 Approve 或 Request Changes。

### 典型审查流程与要点

流程：看标题和描述是否清晰 → 看 Files changed 确认代码与描述一致 → 对多数更新实际试用改动验证意图 → 参考仓库贡献指南了解审查要求、测试与质量验证。

要点：找出潜在问题/风险/局限、提出改进建议、指出 PR 未考虑到的即将到来的变化、提问以确认共识、肯定作者做得好的地方、优先反馈最重要的问题、简洁但有实质内容、友善且共情对待作者。

### 五步操作

1. **打开 PR**：Pull requests → New pull request → base: `main`、compare: `update-game` → 创建；标题 `Update game over message`，描述 `Update the game over message so people know how to play again!`。
2. **分配给自己**：PR 右侧 Assignees 一栏点 **assign yourself**。
3. **留下审查**：Files changed → 查看改动 → **提交审查（Submit review）** → 评论 `Looks good to me. I think this is more intuitive. Nice work!` → 提交。此时先不要合并。
4. **建议更改**：Files changed → 找到 `index.html` 对比视图 → 悬停改动行行号旁点加号 → **Add a suggestion** → 编辑为 `Let's make it a bit more friendly. 🤓` → **Comment**。GitHub 会额外提供 **Commit suggestion** 按钮，作者点一下即可提交建议。切到 Conversation → 点 Commit suggestion → 提交消息填 `Make the end game experience more friendly` → **提交更改**。
5. **合并 PR**：Conversation → **合并拉取请求（Merge pull request）** → （可选）删除 `update-game` 分支。

## 另两门相关课程【官方】

- **Introduction to GitHub**：<https://github.com/skills/introduction-to-github>，面向新开发者/新用户/学生，无先决条件，不到一小时；介绍仓库、分支、提交、PR，产出一份可用作个人资料 README 的 Markdown 文件。四项活动：创建分支 → 提交文件 → 打开 PR → 合并 PR。
- **Communicate using Markdown**：<https://github.com/skills/communicate-using-markdown>，先决条件为熟悉 PR 和编辑文件，不到一小时；用 Markdown 在评论或文本文件中添加列表、图片、链接，产物可用于 GitHub Pages。五项活动：添加标题 → 添加图片 → 添加代码示例 → 制作任务清单 → 合并 PR。

## 已知限制

本资料基于课程页面与步骤文件的文字提取，未实际逐题操作验证；按钮名为英文原文的中文对照，以访问时的界面为准。
