# GitHub Skills 学习笔记

> 整理日期：2026-11-25
> 来源：GitHub Skills <https://skills.github.com/> 及各课程仓库（skills/*）的 README 和 `.github/steps/` 步骤文件
> 说明：【官方】= 直接从 GitHub Skills 课程页面/仓库文件提取；【整理】= 结合本仓库使用经验的归纳，非官方原文。课程文件为英文，下方按钮名为中文对照，以你访问时的 GitHub 界面为准。

---

## 1. GitHub Skills 是什么、怎么用【官方】

GitHub Skills 是 GitHub 官方的**交互式课程平台**：课程以仓库形式提供，你把课程仓库**复制（模板方式）到自己账号**，等约 20 秒让 GitHub Actions 准备好第一节课，**刷新页面**后按仓库里自动创建的 issue 步骤一步步操作，Mona（章鱼猫）会自动检查进度并放出下一步。

**通用启动流程**（三门课一致）：

1. 打开课程仓库页面，点 **Use this template → Create a new repository**（即用模板新建）。
2. Owner 选自己的账号，建议选 **Public**（私有仓库会消耗 Actions 分钟数）。
3. 等待约 20 秒后刷新页面，跟随仓库 issue 中的步骤操作。
4. 若 20 秒后没准备好，到仓库 **Actions** 标签看是否有任务在跑；若显示失败，官方建议提交 issue 报 bug。

---

## 2. 官方课程地图【官方】

按 skills.github.com 页面的分区，逐条列出（名称 + 一句话简介）：

### 第一天（First day on GitHub）

| 课程 | 简介 |
| -- | -- |
| Introduction to GitHub | 不到一小时上手 GitHub |
| Communicate using Markdown | 用轻量标记语言组织想法、协作沟通 |
| GitHub Pages | 从仓库创建网站或博客 |

### 第一周（First week on GitHub）

| 课程 | 简介 |
| -- | -- |
| Introduction to Git | 用命令行和 VS Code 在 Git 版本控制下做一个游戏 |
| Review pull requests | 在 GitHub 上协作共事 |
| Resolve merge conflicts | 理解冲突为何发生以及如何解决 |
| Code with Codespaces | 用 Codespaces 和 VS Code 开发 |
| Introduction to Repository Management | 协作型、友好、健康项目的若干功能基础 |

### GitHub Copilot（AI 编程）

- Getting Started with GitHub Copilot、Customize your GitHub Copilot Experience、GitHub Copilot Code Review、Integrate MCP with GitHub Copilot、Expand your team with Copilot coding agent、Create Applications with the Copilot CLI、Modernize your legacy code with GitHub Copilot、Scale institutional knowledge with GitHub Copilot Spaces、Build applications with GitHub Copilot agent mode、Agentic Workflows that Read the Room、Agent Orchestration Build Your AI Dream Team、Idea to Merge with the Copilot App。

### GitHub Actions（自动化）

- Hello GitHub Actions、Test with Actions、Write JavaScript Actions、Publish Docker Images、Create and use reusable workflows、Work with Workflow Artifacts。

### 代码安全与分析

- Secure your repository supply chain、Introduction to CodeQL、Introduction to secret scanning、Secure code game、Ship with Quality。

### 迁移到 GitHub

- Migrate an Azure DevOps Repository。

> 完整课程与链接以 <https://skills.github.com/> 实时页面为准。本笔记重点学习下面三门与当前工作流最相关的课程。

---

## 3. 重点课程：Review pull requests（审查拉取请求）【官方】

课程页面：<https://github.com/skills/review-pull-requests>
定位：先决条件是熟悉提交、创建分支和 PR（即学完 Hello World / Introduction to GitHub）；时长不到 30 分钟；目标是审查一个简单游戏的 PR。
课程六项活动：打开 PR → 分配给自己 → 留下审查 → 建议更改 → 应用更改 → 合并 PR。

### 3.1 理论基础

**PR 的四个标签页**

| 标签页 | 作用 |
| -- | -- |
| Conversation（对话） | PR 活动的整体日志，开放的讨论空间，供协作者和社区提想法、建议、反馈 |
| Commits（提交） | 只列出该提议分支独有的提交 |
| Checks（检查） | 通过 GitHub Actions 施加的自动化检查结果（本教程不涉及） |
| Files changed（更改的文件） | Diff 视图，前后对照显示改动，可在具体行上添加评论和审查 |

> 提示：未完成的工作可以创建 **draft pull request（草稿 PR）**，避免被误合并或过早审查。

**PR 审查（review）**：其他协作者或社区成员对改动的反馈，用于保证质量、推进项目，也是学习项目、看别人如何解决问题的机会。指定审查者后，对方有三种反馈选项：

- **Comment（评论）**：一般反馈，不代表批准或拒绝
- **Approve（批准）**：在规则集、代码所有者等策略允许时可合并
- **Request Changes（请求更改）**：改动不满足预期、需要更多工作；修改后应重新请求审查

**典型审查流程**：看标题和描述是否清晰 → 看 Files changed 确认代码与描述一致 → 对多数更新实际试用改动验证意图 → 参考仓库的贡献指南了解审查要求、测试与质量验证。

**审查要点**：找出潜在问题/风险/局限、提出改进建议、指出 PR 未考虑到的即将到来的变化、提问以确认共识、肯定作者做得好的地方、优先反馈最重要的问题、简洁但有实质内容、友善且共情对待作者。

### 3.2 五步操作

**Step 1 打开 PR**：在 `update-game` 分支的改动上开 PR。
1. 顶部导航选 **拉取请求（Pull requests）** 标签。
2. 右侧点 **新建拉取请求（New pull request）**。
3. 在 Compare changes 区选 **base: main**、**compare: update-game**，点 **创建拉取请求**。
4. 标题填 `Update game over message`，描述填 `Update the game over message so people know how to play again!`，再点 **创建拉取请求**。

**Step 2 分配给自己**：PR 的 **Assignees** 一栏点 **assign yourself（分配给自己）**。指派人是最熟悉改动的人，便于追踪该找谁问问题。

- **注意**：不能对自己的 PR 选择 Approve 或 Request Changes。

**Step 3 留下审查**：
1. 点 **Files changed** 标签，查看改动（本例只是简单的措辞调整）。
2. 在对比视图上方点 **提交审查（Submit review）**。
3. 输入评论 `Looks good to me. I think this is more intuitive. Nice work!`，再点 **提交审查**。
4. 此时**先不要合并**。

**Step 4 建议更改（Suggest changes）**：适合拼写错误、改写句子这类"改起来比描述更容易"的小改动。
1. 点 **Files changed**，找到 `index.html` 的对比视图。
2. 鼠标悬停在改动行的行号旁，点加号展开行内评论表单。
3. 点 **Add a suggestion（添加建议）** 按钮，插入该行的可修改副本。
4. 按下面内容编辑建议并点 **Comment（评论）**：

   ```suggestion
   Let's make it a bit more friendly. 🤓
   ```

   GitHub 会在评论外额外提供一个 **Commit suggestion（提交建议）** 按钮，作者点一下即可把建议提交，无需打开代码编辑器。

**Step 4 应用建议**：
1. 切到 **Conversation** 标签。
2. 找到 **Commit suggestion** 按钮，提交消息填 `Make the end game experience more friendly`，点 **提交更改（Commit changes）**。

**Step 5 合并 PR**：切到 **Conversation** 标签 → 点 **合并拉取请求（Merge pull request）** → （可选）删除 `update-game` 分支。

---

## 4. 另两门相关课程大纲【官方】

### 4.1 Introduction to GitHub（GitHub 入门）

课程页面：<https://github.com/skills/introduction-to-github>
面向：新开发者、新 GitHub 用户、学生；无先决条件；不到一小时。
内容：介绍仓库、分支、提交、拉取请求；产出一份可用作个人资料 README 的 Markdown 文件。
四项活动：创建分支 → 提交文件 → 打开 PR → 合并 PR。

### 4.2 Communicate using Markdown（用 Markdown 沟通）

课程页面：<https://github.com/skills/communicate-using-markdown>
面向：新开发者、新 GitHub 用户、学生；先决条件：熟悉 PR 和编辑文件（建议先学 Introduction to GitHub）；不到一小时。
内容：用 Markdown 在评论或文本文件中添加列表、图片、链接；把纯文本文件加上 Markdown 格式，产物可用于搭建 GitHub Pages 站点。
五项活动：添加标题 → 添加图片 → 添加代码示例 → 制作任务清单 → 合并 PR。

---

## 5. 与本仓库的关系及练习建议【整理】

- 本仓库的同步流程已经覆盖 Introduction to GitHub 的四项活动（分支/提交/PR/合并可用网页补做）。
- 「Review pull requests」是下一阶技能：本仓库目前只有你一人维护，可先按第 3 节在示例课程仓库里完整走一遍；将来若有人协作维护这份笔记，审查流程即可直接套用。
- 「Communicate using Markdown」与笔记写作直接相关：本仓库的 README 和本文件都用了标题、表格、代码块、链接等语法，可对照该课程检查写法。

---

## 6. 已知限制

- 本笔记基于 GitHub Skills 课程页面的 README 与 `.github/steps/` 步骤文件的文字提取，未实际在 GitHub 上复制课程仓库逐题操作验证；按钮名为英文原文的中文对照，以你访问时的界面为准。
- 课程地图为 2026-11-25 页面所见，GitHub Skills 会持续增删课程，以 <https://skills.github.com/> 实时页面为准。
