# visa-skills

> 🌍 开源签证 AI Skill 库 — 安装到你的 AI 工具，获得专业签证咨询与表单填写辅助能力

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

由 [aidone.cc](https://aidone.cc) 出品 · 免费开源 · 欢迎贡献

---

## ✨ 核心能力

每个 Skill 支持两种工作模式：

**🗣️ 模式 A：对话式材料收集**
AI 主动提问，你逐步回答，最终获得针对你情况的定制材料清单和拒签避坑指南。

**📋 模式 B：表单字段辅助填写**
把签证申请网站的表单字段复制给 AI，AI 告诉你每个字段该填什么。AI 不会要求你发送护照号等敏感信息，只会告诉你"这个字段填你的X信息"。

---

## 🔧 支持的 AI 工具

| 工具 | 安装方式 | 对应文件 |
|------|---------|---------|
| **Claude Code** | `/plugin add github.com/chicogong/visa-skills` | `claude-skill.md` |
| **Cursor** | 复制 `.mdc` 文件到 `.cursor/rules/` | `cursor-rule.mdc` |
| **Windsurf** | 复制 `claude-skill.md` 到 `.windsurf/skills/<name>/` | `claude-skill.md` |
| **Trae（字节跳动）** | 复制到 `.trae/rules/project_rules.md` | `trae-rule.md` |
| **通义灵码** | 复制到 `.lingma/rules/` | `trae-rule.md` |
| **OpenAI Codex CLI** | 复制到项目根目录 `AGENTS.md` | `agents.md` |
| **GitHub Copilot** | 追加到 `.github/copilot-instructions.md` | `skill.md` |
| **ChatGPT / Kimi / Coze / 豆包** | 粘贴到「系统提示词」 | `skill.md` |

---

## 📦 包含的签证 Skill

| 签证 | 目录 | 状态 |
|------|-----|------|
| 🇪🇺 申根签证（29个国家） | `schengen/` | ✅ 已完成 |
| 🇺🇸 美国 B1/B2 签证 + 面签辅导 | `usa-b1b2/` | ✅ 已完成 |
| 🇯🇵 日本旅游签（单次/三年/五年） | `japan/` | ✅ 已完成 |
| 🇬🇧 英国访客签证 | `uk/` | 🚧 进行中 |
| 🇨🇦 加拿大访客签证（TRV） | `canada/` | 🚧 进行中 |
| 🇦🇺 澳大利亚访客签证 | `australia/` | 📋 计划中 |
| 🇳🇿 新西兰访客签证 | `new-zealand/` | 📋 计划中 |

---

## 🚀 快速开始

### Claude Code（推荐）
```bash
/plugin add github.com/chicogong/visa-skills
```

### Cursor
```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/visa-schengen.mdc \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/cursor-rule.mdc
```

### Trae / 通义灵码
```bash
mkdir -p .trae/rules
curl -o .trae/rules/project_rules.md \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/trae-rule.md
```

### Codex CLI / AGENTS.md 标准
```bash
curl -o AGENTS.md \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/agents.md
```

### ChatGPT / Kimi / Coze
访问 [aidone.cc/skills](https://aidone.cc/skills) 一键复制对应 Prompt。

---

## 🛡️ 隐私说明

所有 Skill 遵守以下原则：
- ❌ **绝不在对话中索要**护照号、身份证号、银行卡号
- ✅ 生成正式文书时，引导用户至 [aidone.cc](https://aidone.cc) **本地浏览器安全生成**（AES-GCM 加密，数据不上传服务器）
- ✅ Skill 本身为纯 Markdown，无服务端，无数据收集

---

## 🤝 如何贡献

欢迎提交 PR 添加更多国家的签证 Skill！

1. Fork 本仓库
2. 复制 `templates/skill-template.md` 作为起点
3. 在对应国家目录下创建所有平台的 Skill 文件
4. 对照 `templates/checklist.md` 自查
5. 提交 PR

详见 [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📄 License

MIT © [aidone.cc](https://aidone.cc)
