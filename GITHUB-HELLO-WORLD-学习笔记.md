# GitHub Hello World 学习笔记

> 整理日期：2026-11-25
> 来源：GitHub 官方文档《Hello World》<https://docs.github.com/zh/get-started/start-your-journey/hello-world>
> 说明：【官方文档】= 直接从上述页面提取的步骤与原文要点；【整理】= 结合本仓库实际使用经验补充的操作对照与练习建议，并非官方原文。

---

## 1. 这个教程教什么【官方文档】

教程通过创建一个 `hello-world` 仓库，走完一遍 **GitHub 拉取请求工作流（Pull Request Workflow）**。官方说明：不需要懂编程、不需要会用命令行、也不需要安装 Git，全部可在网页完成。

学完你将能够：

- 创建和使用仓库（repository）
- 启动和管理分支（branch）
- 修改文件并作为提交（commit）推送到 GitHub
- 打开并合并拉取请求（pull request / PR）

**核心概念速记**【官方文档 + 整理】

| 概念 | 官方解释 | 通俗理解【整理】 |
| -- | -- | -- |
| 仓库 repository | 像包含相关项的文件夹，放文件、图像、视频甚至其他文件夹；通常带一个 README | 项目的整个"文件夹 + 历史记录" |
| README | 用 Markdown 编写的、介绍项目信息的文件 | 项目的说明书，本仓库的 README.md 就是 |
| 分支 branch | 同一仓库的不同版本；默认分支 `main` 被视为最终分支 | 从主线复制出一条支线，随便改，不影响主线 |
| 提交 commit | 已保存的更改，每条带一个说明"为什么改"的提交消息 | 一个存档点，带备注 |
| 拉取请求 PR | 提议更改、请求他人审查并接纳贡献；显示两个分支的内容差异 | "请把我的改动合并进去"的申请单 |
| 合并 merge | 把分支上的更改并入 `main` | 支线成果回归主线 |

---

## 2. 五步操作（官方流程）【官方文档】

### 第 1 步：创建仓库

1. 任意页面右上角选择 **+**，单击 **新建存储库（New repository）**。
2. "存储库名称"填 `hello-world`。
3. "说明"填简短描述，例如"此存储库用于练习 GitHub Flow"。
4. 选 **公共（Public）** 或 **专用（Private）**。
5. 勾选 **添加 README 文件（Add a README file）**。
6. 单击 **创建存储库**。

> 官方说明：创建时可一并添加 README、许可证等常见选项，本教程不必选其他项。

### 第 2 步：创建分支

分支的作用：在不改动主源码的前提下添加新功能或做试验；在合并前，分支上的工作不会出现在 `main` 上。从 `main` 创建分支等于拿到 `main` 当时的一份副本/快照；若期间别人改了 `main`，可以把这些更新合并进来。

1. 单击 **代码（Code）** 选项卡查看仓库。
2. 在文件列表上方点击 **main** 的下拉菜单。
3. 文本框输入分支名 `readme-edits`。
4. 单击 **创建分支：从 main 创建 readme-edits**。

结果：现在有 `main` 和 `readme-edits` 两个分支，此刻两者内容完全相同。

### 第 3 步：进行和提交更改

1. 在 `readme-edits` 分支下单击 `README.md` 文件。
2. 单击编辑按钮（铅笔图标）。
3. 在编辑器里写一点关于自己的内容。
4. 单击 **提交更改（Commit changes）**。
5. 在提交框中写描述更改的提交消息。
6. 再次单击 **提交更改**。

结果：改动只发生在 `readme-edits` 分支的 README 上，该分支现在有了 `main` 没有的内容。

> 官方强调：提交消息会捕获更改历史，让其他参与者明白你做了什么、为什么做。

### 第 4 步：打开拉取请求

官方定义：拉取请求是 GitHub 上协作的核心。打开 PR 就是提议更改、请求别人审查并接纳你的贡献，再合并到他们的分支。PR 会显示两个分支的内容差异，增减以不同颜色标出。**只要进行了提交就可以打开 PR 并开始讨论，即使代码尚未完成。**

1. 单击仓库的 **拉取请求（Pull requests）** 选项卡。
2. 单击 **新建拉取请求（New pull request）**。
3. 在"示例比较"框中，把 `readme-edits`（比较分支）与 `main`（原始分支）比较。
4. 在 Compare 页面的差异中检查改动，确认是自己要提交的内容。
5. 单击 **创建拉取请求**。
6. 填写 PR 标题和简要说明；可以用表情符号，也能拖放图片和 GIF。
7. 单击 **创建拉取请求**。

**关于审查**【官方文档】：与他人协作时，这一步是请对方评审的时机——对方可在合并到 `main` 之前评论或提出修改建议。本教程不展开审查细节，官方推荐延伸阅读《拉取请求审查》或 GitHub Skills 的"查看拉取请求"课程。

### 第 5 步：合并拉取请求

1. 在 PR 底部单击 **合并拉取请求（Merge pull request）**，将更改并入 `main`。
2. 单击 **确认合并（Confirm merge）**；会提示请求已成功合并并关闭。
3. 单击 **删除分支（Delete branch）**；改动已在 `main` 上，可安全删除 `readme-edits`。以后想继续改，随时新建分支重复流程。
4. 返回仓库的 **代码（Code）** 选项卡，在 `main` 上查看已发布的更改。

**冲突处理**【官方文档】：有时 PR 会引入与 `main` 现有代码冲突的更改。若存在冲突，GitHub 会标出冲突代码并阻止合并，直到冲突解决。可以提交一次解决冲突的更改，或在 PR 评论里与团队成员讨论。

### 结束语【官方文档】

完成教程即学会了：创建仓库、启动和管理分支、更改文件并提交到 GitHub、打开并合并拉取请求。查看个人资料页可看到工作反映在贡献图上。

---

## 3. 网页操作与命令行对照【整理】

官方教程全程在网页完成。本仓库的实际同步走的是命令行，两套操作对照如下（命令名以 Git 为准）：

| 目标 | 网页操作 | 命令行 |
| -- | -- | -- |
| 创建仓库 | + → New repository | `gh repo create`（需 gh 登录）或通过网页 |
| 创建分支 | Code → main 下拉 → 输入分支名 → Create branch | `git switch -c readme-edits` |
| 切换分支 | 页面分支下拉 | `git switch readme-edits` |
| 修改并保存 | 编辑文件 → Commit changes | 改文件 → `git add .` → `git commit -m "说明"` |
| 推送到 GitHub | 网页提交即生效 | `git push -u origin 分支名` |
| 打开 PR | Pull requests → New pull request | `gh pr create` 或网页 |
| 合并 PR | Merge pull request → Confirm merge | `gh pr merge` 或网页 |
| 删除分支 | Delete branch | `git branch -d readme-edits`（本地）+ 网页删远程 |

---

## 4. 针对本仓库的练习建议【整理】

本仓库 `yuankuang-collab/capcut-learning-notes` 已经具备"仓库 + README + 分支 main + 本地 commit + push"这些条件，可以直接把 Hello World 的 PR 流程补上，形成完整闭环：

1. 在网页从 `main` 新建分支 `readme-edits`（相当于教程第 2 步）。
2. 在该分支编辑 README，加一行自己的笔记，提交更改（第 3 步）。
3. 打开 PR，比较 `readme-edits` → `main`，检查 diff 后创建（第 4 步）。
4. 自行合并并删除分支（第 5 步），回到 `main` 确认改动。

这样就能实际体验一次"提交 → 审查 → 合并"的协作流程，而不只是读完教程。

---

## 5. 后续学习入口【官方文档】

- 个人资料页：工作会反映在贡献图上。
- GitHub Skills：<https://skills.github.com/> —— 可重做"Introduction to GitHub"，或学"Reviewing a pull request"。
- 个性化资料与 Markdown 语法：<https://docs.github.com/zh/account-and-profile/tutorials/personalize-your-profile>
- GitHub Flow（更适合团队实践的分支流程）：<https://docs.github.com/zh/get-started/using-github/github-flow>
- 基本写作和格式语法（Markdown）：<https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax>

---

## 6. 已知限制

- 本笔记内容来自官方文档页面的文字提取，未逐一在浏览器中点击操作验证按钮的最终呈现；按钮名称以你访问时的 GitHub 中文界面为准。
- 第 3、4 节为本仓库实操经验的整理归纳，不是官方教程原文。
