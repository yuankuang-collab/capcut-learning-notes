# 调色流程与量化标准

> 来源：Blackmagic Design《The Colorist Guide to DaVinci Resolve 20》官方 PDF（496 页）<https://documents.blackmagicdesign.com/UserManuals/DaVinci-Resolve-20-Colorist-Guide.pdf>。调研任务提取正文，本轮未逐页复查（【一手-未抽查】）。方法可迁移到任何调色软件。整理 2026-11-26。

---

## 1. 顺序铁律

1. **Color Correction（技术校正）**：用一级工具调整整个画面，手段是 normalization、balancing、shot matching。
2. **Creative Grading / Creating a Look（风格化）**：此时仔细考虑场景的情感与叙事含义。

先校正再风格化，顺序不可颠倒。

## 2. 一级色轮三亮度段

- **Lift = 阴影**
- **Gamma = 中间调**
- **Gain = 高光**

## 3. Normalization 量化标准

- 阴影浮在黑点（0）之上约 **5–10%**；
- 高光停在白点之下约 **90%**；
- 剩余 **10%** 留给超白元素（车灯、窗户、金属高光）作 headroom；
- 波形上低于 **0** 或高于 **1023** 会被裁切、丢失细节。

## 4. Shot matching（镜头匹配）

比较片段并**精确匹配对比度与颜色**；当大多数镜头已相近、只需微调少数例外时尤其高效。

## 5. 二级调色（Secondary）

只调整画面的一部分：

- **Qualifier** 负责提取元素（追求干净边缘）；
- **Power Window** 把 qualifier 的影响限制在画面特定区域；
- 二者配合最强；
- 节点顺序上，primary corrections 放在靠近 Input 的上游节点。

---

## 边界

以上数值出自官方教材，具体到不同软件/版本的面板名称与实现方式可能不同；以官方文档原文和你使用的工具为准。本轮未逐页验证 496 页全文，关键参数使用前建议查原文确认。
