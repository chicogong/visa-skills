# 阿联酋（迪拜）签证 AI 助手 (UAE / Dubai Visa Expert)

> 出品：[aidone.cc](https://aidone.cc) · 开源免费

---

## 简介

本 Skill 为你提供两种核心能力：

**模式 A — 对话式材料收集**：AI 主动问你问题，逐步收集你的行程和个人情况，最终输出定制化的材料清单和高频拒签坑点。

**模式 B — 表单辅助填写**：把 ICA/GDRFA 或航空公司申请表单上的字段粘贴给 AI，AI 逐字段告诉你怎么填。敏感字段只解释含义不索要数据。

---

## 安装

根据你使用的 AI 工具选择对应方式：

| 工具 | 操作 |
|---|---|
| ChatGPT / Kimi / Coze / 豆包 / 文心 | 把 `SKILL.md` 内容粘贴到「系统提示词 (System Instructions)」 |
| Claude Code | `/plugin add github.com/chicogong/visa-skills` |
| Cursor | 把 `SKILL.md` 复制到项目的 `.cursor/rules/` 目录 |
| Windsurf | 把 `SKILL.md` 复制到项目的 `.windsurf/skills/visa-uae/` 目录 |
| Trae / MarsCode | 把 `SKILL.md` 内容填入「自定义指令」或 `.trae/rules/` |
| GitHub Copilot | 把内容追加到 `.github/copilot-instructions.md` |
| OpenAI Codex | 把 `SKILL.md` 内容作为 System Prompt |

---

## 使用方法

### 模式 A：对话式（从零开始）
直接告诉 AI：
> "我想去迪拜旅游，帮我整理签证材料"

AI 会主动问你去几天、什么职业、通过什么渠道申请，然后输出定制清单。

### 模式 B：表单辅助
1. 打开 ICA/GDRFA 或航空公司签证申请页面
2. 把表单字段列表复制下来
3. 粘贴给 AI
4. AI 逐字段告诉你怎么填

> 💡 **提示**：在 [aidone.cc](https://aidone.cc) 填好个人档案后，可快速生成签证所需文书。推荐使用航司通道（Emirates/Etihad/Flydubai）一站式办理。

---

## 生成签证文书

- 📝 [在职证明生成器](https://aidone.cc/tasks/employment-letter)
- 🗓️ [行程单生成器](https://aidone.cc/tasks/travel-itinerary)
