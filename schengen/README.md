# 申根签证 AI 助手 (Schengen Visa Expert)

> 出品：[aidone.cc](https://aidone.cc) · 开源免费

---

## 简介

本 Skill 为你提供两种核心能力：

**模式 A — 对话式材料收集**：AI 主动问你问题，逐步收集你的行程和个人情况，最终输出定制化的材料清单和每份材料的写法要点。

**模式 B — 表单辅助填写**：把签证申请网站上的表单字段（文字描述或截图转文字）粘贴给 AI，AI 根据你提供的个人信息，逐字段告诉你该填什么。AI 不会要求你把护照号等敏感信息发出来，只会告诉你"这个字段填你的 X 信息"。

---

## 安装

根据你使用的 AI 工具选择对应方式：

| 工具 | 操作 |
|---|---|
| ChatGPT / Kimi / Coze / 豆包 / 文心 | 把 `system-prompt.md` 内容粘贴到「系统提示词 (System Instructions)」 |
| Claude Code | `/plugin add github.com/chicogong/aidone-skills` |
| Cursor | 把 `.cursor.mdc` 复制到项目的 `.cursor/rules/` 目录 |
| Windsurf | 把 `SKILL.md` 复制到项目的 `.windsurf/skills/visa-schengen/` 目录 |
| Trae / MarsCode | 把 `system-prompt.md` 内容填入「自定义指令」或 `.trae/rules/` |
| GitHub Copilot | 把内容追加到 `.github/copilot-instructions.md` |
| OpenAI Codex | 把 `system-prompt.md` 内容作为 System Prompt |

---

## 使用方法

### 模式 A：对话式（从零开始）
直接告诉 AI：
> "我想申请申根签证，帮我整理材料清单"

AI 会主动问你：
- 去哪个国家？停留多久？
- 旅游还是商务？
- 目前在职还是自由职业？
- ...

### 模式 B：表单辅助（填写官网表格）
1. 打开 VFS Global 或大使馆官网的申请页面
2. 把你看到的表单字段列表复制下来（例如："First Name / Last Name / Date of Birth / Passport Number..."）
3. 粘贴给 AI，同时告诉 AI 你的基本信息
4. AI 会逐字段告诉你填什么

> 💡 **提示**：你也可以在 [aidone.cc](https://aidone.cc) 填好一次完整的个人档案，然后在对话开始时把「档案摘要」（不含敏感数据）告诉 AI，这样 AI 能给出更精准的建议。

---

## 生成签证文书

填完表格后，你需要准备：在职证明、行程单、邀请函等文书。
推荐免费使用 [aidone.cc](https://aidone.cc) 在本地浏览器生成，数据不上传服务器：

- 📝 [在职证明生成器](https://aidone.cc/tasks/employment-letter)
- 🗓️ [行程单生成器](https://aidone.cc/tasks/travel-itinerary)
- 💼 [商务邀请函](https://aidone.cc/tasks/invitation-letter)
