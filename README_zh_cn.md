[查看中文版](./README_zh_cn.md) | [View in English](./README.md)

# Vibe 编程终极指南 V1.0
**作者：** [Nicolas Zullo, https://x.com/NicolasZu](https://x.com/NicolasZu)  
**日期：** 2025年3月12日  

---

## 入门
开始 Vibe 编程，你只需要两个工具：  
- **Grok 3 Thinking**  
- **Cursor 搭配 Claude Sonnet 3.7 Thinking**  

正确设置一切是关键。如果你认真想要创建一个功能齐全且视觉吸引力强的游戏，请花时间建立一个坚实的基础。  

**关键原则：** *计划就是一切。* 不要让 AI 自主规划，否则你的代码库将变得不可管理。

---

## 设置一切

### 1. 游戏设计文档
- 将你的游戏创意交给 **Grok 3 Thinking**，让它创建一个简单的 **游戏设计文档**，格式为 Markdown (`.md`)。  
- 审核并完善文档，确保它符合你的愿景。即使它很基础也没关系——目标是为 AI 提供关于游戏结构和意图的上下文。  

### 2. 技术栈和 `.cursor/rules`
- 让 **Grok 3 Thinking** 推荐适合你游戏的最佳技术栈（例如，ThreeJS 和 WebSocket 用于多人 3D 游戏）。  
  - 挑战它提出*最简单但最可靠的栈*。  
- 下载 [https://docs.cursor.com/context/rules-for-ai](https://docs.cursor.com/context/rules-for-ai) 的 PDF 版本，上传并让 Grok 编写一组 6-10 条规则，假设它是你选择的技术栈的资深游戏开发者。  
  - 确保其中一条规则强调 **模块化**（多个文件）并避免 **单体结构**（一个巨大的文件）。  
  - 示例：规则可能包括网络最佳实践。  
  - *如果你想要一个尽可能优化的游戏和尽可能干净的代码，这是必须的。*

### 3. 实施计划
- 提供 **Grok 3 Thinking**：  
  - 游戏设计文档  
  - 技术栈推荐  
  - Cursor 规则  
- 让它创建一个详细的 **实施计划**，格式为 Markdown (`.md`)，包含 AI 开发者的逐步说明。  
  - 步骤应小而具体。  
  - 每个步骤必须包括验证正确实施的测试。  
  - 不需要代码——只需清晰、具体的说明。  
  - 关注*基础游戏*，而不是完整的功能集（细节稍后再补充）。  

### 4. 记忆库
- 创建一个新文件夹，在 Cursor 中打开它，再创建一个文件夹，命名为 `memory-bank`。  
- 添加以下文件：  
  - `game-design-document.md`  
  - `tech-stack.md`  
  - `implementation-plan.md`  
  - `progress.md`（用于跟踪已完成的步骤）  
  - `architecture.md`（用于记录文件用途）  

### 5. 设置 `.cursor/rules`
- 在 Cursor 中，按 `Cmd + Shift + P`，输入 "rules"，然后按回车。  
- 输入第 2 步中由 Grok 3 生成的规则。  

---

## Vibe 编程基础游戏
现在开始有趣的部分！

### 确保一切清晰
- 在 Cursor 中选择 **Claude Sonnet 3.7 Thinking**。  
- 提示：阅读 `/memory-bank` 中的所有文档，`implementation-plan.md` 是否清晰？你有什么问题可以让它对你来说 100% 清晰？  
- 它通常会问 9-10 个问题，回答这些问题并提示它编辑 `implementation-plan.md`，使其更完善。

### 第一个实施提示
- 在 Cursor 中选择 **Claude Sonnet 3.7 Thinking**。  
- 提示：阅读 `/memory-bank` 中的所有文档，并执行实施计划的第 1 步。我将运行测试。在我验证测试之前，不要开始第 2 步。一旦我验证了它们，打开 `progress.md` 并记录你为未来开发者所做的工作。然后将任何架构见解添加到 `architecture.md`，以解释每个文件的作用。

- **极致 Vibe：** 安装 [Superwhisper](https://superwhisper.com)，以便与 Claude 进行随意对话，而不是打字。  

### 工作流程
- 完成第 1 步后：  
- 将更改提交到 Git（如果不熟悉，请向 Grok 3 寻求帮助）。  
- 开始一个新的 composer（`Cmd + N`，`Cmd + I`）。  
- 提示：现在浏览记忆库中的所有文件，阅读 `progress.md` 以了解之前的工作，并继续实施计划的第 2 步。在我验证测试之前，不要开始第 3 步。  
- 重复此过程，直到完成整个 `implementation-plan.md`。

---

## 添加细节
恭喜你，你已经构建了基础游戏！它可能很粗糙且缺乏功能，但现在你可以进行实验和改进。  
- 想要雾、后期处理、特效或声音？更好的飞机/汽车/城堡？一个华丽的天空？  
- 对于每个主要功能，创建一个新的 `feature-implementation.md` 文件，包含简短的步骤和测试。  
- 逐步实施和测试。  

---

## 修复错误和卡住问题
- 如果提示失败或破坏了游戏：  
- 点击 Cursor 中的“恢复”，并完善你的提示，直到它有效。  
- 对于错误：  
- **如果是 JavaScript：** 打开控制台（`F12`），复制错误并粘贴到 Cursor 中——或者为视觉问题提供截图。  
- **懒人选项：** 安装 [BrowserTools](https://browsertools.agentdesk.ai/installation)，跳过手动复制/截图。  
- 如果卡住：  
- 恢复到你最后的 Git 提交（`git reset`），并使用新提示重试。  
- 如果*真的*卡住：  
- 使用 [RepoPrompt](https://repoprompt.com/) 并向 **Grok 3 Thinking** 寻求帮助。  

---

## 其他提示
- **小编辑：** 使用 Claude Sonnet 3.5。  
- **优秀的文案：** 使用 GPT-4.5。  
- **更好的提示输出：** 添加“尽可能长时间思考以确保正确，我不着急。重要的是你要完全按照我的要求执行。如果我不够精确，请向我提问。”

---

## 常见问题
**问：你的飞机很棒，但我无法通过一个提示复制它！**  
**答：** 这不是一个提示——而是大约 30 个提示，由一个 `plane-implementation.md` 文件指导。使用明确、具体的提示，例如“在机翼上切出空间用于副翼”，而不是模糊的提示，例如“制作一架飞机”。

**问：我不知道如何为我的多人游戏设置服务器**  
**答：** 问 Grok 3。

---

## Vibe Coding Game Jams
1. [2025 Vibe Coding Game Jam，由 @levelsio 主办，Bolt.new + Coderabbit AI + Lambda Labs 赞助](https://jam.pieter.com/)  
   1. 报道：[Vibe 编程：创意激增还是技术债务陷阱？| 作者：Ben Fairbank | 2025 年 4 月 | Medium](https://medium.com/@bennydoda83/vibe-coding-a-creative-surge-or-a-technical-debt-trap-8c6932675e6b)

---

注意：中文版本由英文版翻译而来，如有不解之处，请参考英文版 README。