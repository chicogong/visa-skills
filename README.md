# aidone-skills

> 开源签证 AI Skill 库 — 安装到你的 AI 编程助手，获得专业签证咨询能力

[aidone.cc](https://aidone.cc) 出品 · 免费开源 · 欢迎贡献

---

## 这是什么？

这个仓库收录了针对全球各国签证申请场景的 AI Skill Prompt，你可以将它们安装到你正在使用的 AI 编程/助手工具里，快速获得：

- 📋 **各国签证材料清单与避坑指南**
- 🤖 **对话式材料收集**：AI 主动提问，你回答，AI 汇总成完整清单
- 📝 **表单辅助填写**：把网页表单内容复制给 AI，AI 用你的档案数据帮你填好每个字段

## 支持的 AI 工具

| 工具 | 安装方式 | Skill 文件 |
|---|---|---|
| **Claude Code** | `/plugin add github.com/chicogong/aidone-skills` | `.claude/skills/` |
| **Cursor** | 复制 `.mdc` 文件到 `.cursor/rules/` | `.cursor/rules/` |
| **Windsurf** | 复制 `SKILL.md` 到 `.windsurf/skills/` | `.windsurf/skills/` |
| **Trae / MarsCode** | 复制到 `.trae/rules/` 或项目根目录 | `RULES.md` |
| **GitHub Copilot** | 复制到 `.github/copilot-instructions.md` | `.github/` |
| **OpenAI Codex** | System Prompt 直接粘贴 | `system-prompt.md` |
| **ChatGPT / Kimi / Coze** | 粘贴到「系统提示词」 | `system-prompt.md` |
| **通义灵码 / 豆包** | 粘贴到「自定义指令」 | `system-prompt.md` |

## 两种使用模式

### 模式 A：对话式材料收集（推荐新手）
AI 会像一位签证顾问一样，主动问你问题：出发日期？目的地？职业？然后汇总成你需要准备的材料清单，并给出每份材料的写法要点。

### 模式 B：表单字段辅助填写
1. 打开签证申请网站
2. 把你看到的表单字段（或截图转文字）复制给 AI
3. AI 会根据你的个人档案逐字段回答应填什么内容
4. 你对照 AI 的答案，手动填入官网

> ⚠️ **安全提示**：永远不要把护照号、银行卡号发给你不信任的 AI 服务。
> 我们建议你只告诉 AI 你需要填什么字段，然后自己输入敏感数据。

## 包含的签证 Skill

```
visa/
├── schengen/      🇪🇺 申根签证（29个国家）
├── usa/           🇺🇸 美国 B1/B2 签证 + 面签辅导
├── japan/         🇯🇵 日本旅游签（单次/三年/五年）
├── uk/            🇬🇧 英国访客签证
├── canada/        🇨🇦 加拿大访客签证（TRV）
├── australia/     🇦🇺 澳大利亚访客签证（600类）
└── new-zealand/   🇳🇿 新西兰访客签证
```

## 如何贡献

欢迎提交 PR 添加更多国家的签证 Skill！请参考 `visa/schengen/` 的目录结构。

每个 Skill 需要包含：
- `system-prompt.md`：通用系统提示词（兼容所有 AI 工具）
- `SKILL.md`：Claude/Windsurf 格式（含 YAML frontmatter）
- `.cursor.mdc`：Cursor Rules 格式
