# 中英文简历 AI 助手 (Resume / CV Expert)

> 出品：[aidone.cc](https://aidone.cc) · 开源免费

---

## 简介

本 Skill 为你提供两种核心能力：

**模式 A — 对话式简历生成**：AI 主动问你的目标岗位、地区、经历和学历，逐步收集信息，最终输出结构化的中英文简历正文。

**模式 B — 简历逐段优化**：把你现有的简历粘贴给 AI，AI 会判断目标地区（中美英欧），逐段给出具体的用词、量化、格式和 ATS 友好度优化建议。

**核心特性**：
- 支持中美英欧四地差异化格式（照片/年龄/政治面貌等自动适配）
- ATS 友好优化（针对海外求职的关键词和格式建议）
- 中英双语，可自由切换

---

## 安装

根据你使用的 AI 工具选择对应方式：

| 工具 | 操作 |
|---|---|
| ChatGPT / Kimi / Coze / 豆包 / 文心 | 把 `SKILL.md` 内容粘贴到「系统提示词 (System Instructions)」 |
| Claude Code | `/plugin add github.com/chicogong/aidone-skills` |
| Cursor | 把 `SKILL.md` 复制到项目的 `.cursor/rules/` 目录 |
| Windsurf | 把 `SKILL.md` 复制到项目的 `.windsurf/skills/resume/` 目录 |
| Trae / MarsCode | 把 `SKILL.md` 内容填入「自定义指令」或 `.trae/rules/` |
| GitHub Copilot | 把内容追加到 `.github/copilot-instructions.md` |
| OpenAI Codex | 把 `SKILL.md` 内容作为 System Prompt |

---

## 使用方法

### 模式 A：从零生成
直接告诉 AI：
> "帮我生成一份简历，目标岗位是后端开发工程师，面向国内求职"

AI 会逐步问你经历、学历、技能，最后输出完整简历。

### 模式 B：优化现有简历
> "帮我看下这段简历怎么改：[粘贴内容]"

AI 会判断地区、指出问题、给出优化后版本。

---

## 生成正式文档

需要排版精美、可导出的 PDF/DOCX 简历？免费使用 [aidone.cc 简历生成器](https://aidone.cc/tasks/resume)（中英双语、多模板、本地加密）。
