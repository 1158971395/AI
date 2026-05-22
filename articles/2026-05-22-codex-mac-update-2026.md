---
title: "Codex 这波大更新后，Mac 的含金量再次提升"
date: 2026-05-22
tags: AI, OpenAI, Codex, macOS, 产品分析
excerpt: "Codex 迎来大更新：Appshots 应用快照、Locked Computer Use 锁屏远程操控、/goal 命令正式上线。macOS 独占功能让 Mac 的 AI PC 含金量再次提升。"
cover: https://jonathanxu.xyz/codex-mac-update-2026.png
source: APPSO（爱范儿）
---

## 核心观点

OpenAI Codex 本周迎来重大功能更新，新增 Appshots 应用快照、Locked Computer Use 锁屏远程操控、/goal 正式发布等多项能力。**但所有新功能均为 macOS 独占**，Windows 用户暂不可用。

## 关键洞察

| 维度 | 要点 |
|------|------|
| 🏢 商业表现 | OpenAI Q1 营收 57 亿美元，Codex 是主要增长引擎 |
| 🍎 平台策略 | 三大新功能全为 macOS 独占，Mac mini 的 AI PC 含金量持续上升 |
| 🔒 安全设计 | Locked Computer Use 采用 Apple 授权认证插件，多层次安全约束 |
| 🎯 产品架构 | /goal 让 Codex 从对话工具转向任务驱动的持久 Agent 架构 |

## 深度解读

### 1. Appshots：从截屏到应用级的上下文理解

同时按下两个 Command 键，Codex 自动捕获当前应用窗口的截图和文本（包括屏幕不可见内容），作为对话上下文。与普通截图不同，Codex 会结合 **Computer Use** 和 **Chrome 自动化**，读取整个窗口而非仅一张图。

**实际效果：** 在飞书文档开头按 Command+Command，Codex 会自动打开 Chrome 浏览全文。在微信阅读公众号时同样可用，但存在 Bug——Computer Use 操作微信时可能误登出账号。

> "就是这种应用多做了一步的感觉，我们就减少了很多 AI 的使用负担，让 Codex 的体验也变得更加丝滑。"

### 2. Locked Computer Use：迈向持久 Agent 的关键一步

这是本次更新最具突破性的功能——Mac 锁屏后，Codex 仍能在后台操控桌面应用完成任务。

**安全机制（4 层防护）：**
- 解锁窗口极短，仅限当前 Computer Use 操作期间
- 覆盖所有显示器，临时解锁期间屏幕对旁观者不可见
- 检测到键盘/鼠标输入立即重锁
- 仅 Codex 可调用，其他进程无法借道

> "如果 Codex 能够在没有活跃用户会话的情况下运行 Mac 应用，这或许是迈向持久 Agent 基础架构的第一步。"

### 3. /goal：从对话到项目管理

/goal 命令从实验室正式推出，将任务当作独立项目进行管理。Codex 会反复判断"还该做什么"和"是否完成"，自动迭代直到任务完成。

**关键原则：目标必须具体可验证。**
- ✅ 好目标："把首页交互时间压到 1 秒以内"
- ✅ 好目标："将 JavaScript 项目迁移到 TypeScript，strict 模式编译通过"
- ❌ 坏目标："优化一下"、"完善一下"

### 4. ChatGPT + PowerPoint 集成

ChatGPT 新增可直接在 PowerPoint 中创建和编辑演示文稿的能力，支持 GPT Image 2 生成 PPT 内图片。

### 5. 实用贴士

**解决绑定手机号问题：** 先在浏览器打开 https://auth.openai.com/log-in 登录，再回 Codex 授权即可跳过。

> "如果这篇文章获得了一个赞，你的 Codex 有可能重置额度限制 😄"

## 文章金句

> "Mac 用户总是能享受到好东西，而 Windows 用户只能眼巴巴地看着，哈哈。不得不说，Mac mini 作为 AI PC 的含金量还在增加。"
