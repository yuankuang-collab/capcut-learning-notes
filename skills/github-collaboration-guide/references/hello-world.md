# GitHub Hello World：拉取请求工作流

来源：GitHub 官方文档《Hello World》<https://docs.github.com/zh/get-started/start-your-journey/hello-world>。整理日期 2026-11-25。按钮名为原文中文对照，以实际界面为准。

## 核心概念【官方】

| 概念 | 官方解释 |
| -- | -- |
| 仓库 repository | 像包含相关项的文件夹，放文件、图像、视频甚至其他文件夹；通常带一个 README |
| README | 用 Markdown 编写的、介绍项目信息的文件 |
| 分支 branch | 同一仓库的不同版本；默认分支 `main` 被视为最终分支 |
| 提交 commit | 已保存的更改，每条带一个说明“为什么改”的提交消息 |
| 拉取请求 PR | 提议更改、请求他人审查并接纳贡献；显示两个分支的内容差异 |
| 合并 merge | 把分支上的更改并入 `main` |

官方说明：教程不需要懂编程、不需要会用命令行、也不需要安装 Git，全部可在网页完成。

## 五步操作【官方】

### 第 1 步：创建仓库

1. 任意页面右上角选择 **+**，单击 **新建存储库（New repository）**。
2. “存储库名称”填 `hello-world`。
3. “说明”填简短描述，例如“此存储库用于练习 GitHub Flow”。
4. 选 **公共（Public）** 或 **专用（Private）**。
5. 勾选 **添加 README 文件（Add a README file）**。
6. 单击 **创建存储库**。

### 第 2 步：创建分支

分支用于在不改动主源码的前提下做试验和编辑；从 `main` 创建分支等于拿到 `main` 当时的副本/快照，合并前该分支的工作不会出现在 `main` 上。若期间别人改了 `main`，可把这些更新合并进自己的分支。

1. 单击 **代码（Code）** 选项卡查看仓库。
2. 文件列表上方点击 **main** 的下拉菜单。
3. 文本框输入分支名 `readme-edits`。
4. 单击 **创建分支：从 main 创建 readme-edits**。

结果：`main` 与 `readme-edits` 两个分支此刻内容完全相同。

### 第 3 步：进行和提交更改

官方强调：提交消息会捕获更改历史，让其他参与者明白你做了什么、为什么做。

1. 在 `readme-edits` 分支下单击 `README.md`。
2. 单击编辑按钮。
3. 在编辑器里写一点关于自己的内容。
4. 单击 **提交更改（Commit changes）**。
5. 提交框中写描述更改的提交消息。
6. 再次单击 **提交更改**。

### 第 4 步：打开拉取请求

官方定义：PR 是 GitHub 上协作的核心，显示两个分支的内容差异，增减以不同颜色标出。**只要进行了提交就可以打开 PR 并开始讨论，即使代码尚未完成。**

1. 单击 **拉取请求（Pull requests）** 选项卡。
2. 单击 **新建拉取请求（New pull request）**。
3. 比较 `readme-edits` 与 `main`，检查差异。
4. 单击 **创建拉取请求**。
5. 填写标题和简要说明（可用表情符号、拖放图片和 GIF），再次单击 **创建拉取请求**。

**关于审查**：与他人协作时，这一步请对方评审，对方可在合并到 `main` 前评论或提出修改建议。延伸阅读《拉取请求审查》或 GitHub Skills 的“查看拉取请求”课程。

### 第 5 步：合并拉取请求

1. PR 底部单击 **合并拉取请求（Merge pull request）**。
2. 单击 **确认合并（Confirm merge）**，请求会显示成功合并并关闭。
3. 单击 **删除分支（Delete branch）**，安全删除 `readme-edits`。
4. 返回 **代码（Code）** 选项卡，在 `main` 上查看已发布的更改。

**冲突处理**【官方】：PR 可能引入与 `main` 冲突的更改。GitHub 会标出冲突代码并阻止合并，直到冲突解决。可提交一次解决冲突的更改，或在 PR 评论里与团队讨论。

## 网页操作与命令行对照【整理】

| 目标 | 网页操作 | 命令行 |
| -- | -- | -- |
| 创建仓库 | + → New repository | `gh repo create` 或通过网页 |
| 创建分支 | Code → main 下拉 → 输入分支名 → Create branch | `git switch -c 分支名` |
| 切换分支 | 页面分支下拉 | `git switch 分支名` |
| 修改并保存 | 编辑文件 → Commit changes | 改文件 → `git add .` → `git commit -m "说明"` |
| 推送到 GitHub | 网页提交即生效 | `git push -u origin 分支名` |
| 打开 PR | Pull requests → New pull request | `gh pr create` 或网页 |
| 合并 PR | Merge pull request → Confirm merge | `gh pr merge` 或网页 |
| 删除分支 | Delete branch | `git branch -d 分支名`（本地）+ 网页删远程 |

## 后续入口【官方】

- 个人资料页：工作会反映在贡献图上。
- GitHub Skills：<https://skills.github.com/>
- GitHub Flow：<https://docs.github.com/zh/get-started/using-github/github-flow>
- Markdown 基本语法：<https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax>
