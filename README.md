# visa-skills 🌍

> **Open-source AI Skill library for visa applications** — Install into Claude, Cursor, Trae, Codex, ChatGPT and more.
>
> 开源签证 AI Skill 库 — 一键安装到主流 AI 工具，获得专业签证咨询与表单辅助能力

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-3b82f6.svg)](CONTRIBUTING.md)
[![Skills](https://img.shields.io/badge/Skills-7%20countries-8b5cf6.svg)](#-skills-list)

**由 [aidone.cc](https://aidone.cc) 出品 · 免费开源 · 欢迎贡献 PR**

---

## ✨ 能做什么

每个 Skill 内置两种工作模式，**自动识别**，无需手动切换：

### 🗣️ 模式 A：对话式材料收集
AI 扮演签证顾问，主动向你提问（目的地、职业、停留时间等），逐步收集信息，最终输出：
- ✅ 针对你情况的**定制材料清单**（必须 / 建议 / 加分项 三档）
- ⚠️ 你情况下的**高频拒签坑点**（精准 2-3 条）
- 📝 每份关键材料的**写法要点**

### 📋 模式 B：表单字段辅助填写
把签证官网的表单字段（文字或截图转文字）复制给 AI，AI 告诉你每个字段该填什么。

> **隐私设计**：护照号、身份证号、银行卡号等敏感字段，AI 只告诉你"这里填你的护照号"，绝不要求你把敏感信息发给它。

---

## 📦 Skills 列表

| 签证 | 目录 | 状态 | 适用人群 |
|------|------|------|---------|
| 🇪🇺 **申根签证**（29国）| [`schengen/`](schengen/) | ✅ 完整版 | 去法/德/意/西等欧洲国家 |
| 🇺🇸 **美国 B1/B2 签证** | [`usa-b1b2/`](usa-b1b2/) | ✅ 完整版 | 旅游/商务赴美，含面签辅导 |
| 🇯🇵 **日本旅游签**（单/三/五年）| [`japan/`](japan/) | ✅ 完整版 | 日本旅游，含年薪/领区判断 |
| 🇬🇧 **英国访客签证** | [`uk/`](uk/) | ✅ 完整版 | 赴英旅游/探亲/商务 |
| 🇨🇦 **加拿大访客签（TRV）** | [`canada/`](canada/) | ✅ 完整版 | 赴加旅游/探亲 |
| 🇦🇺 **澳大利亚访客签（600类）**| [`australia/`](australia/) | ✅ 完整版 | 赴澳旅游/探亲，含 GTE 辅导 |
| 🇳🇿 **新西兰访客签证** | [`new-zealand/`](new-zealand/) | ✅ 完整版 | 赴新西兰旅游/探亲 |

---

## 🚀 安装方式

> **选择你在用的 AI 工具，按对应方式安装即可。**

### 💬 ChatGPT / Kimi / Coze / 豆包 / 文心一言（最简单）

1. 打开对应国家目录，复制 `SKILL.md` 中的全部内容
2. 粘贴到你的 AI 工具的「系统提示词（System Instructions）」设置中
3. 开始对话，说"帮我整理申根签证材料"即可

或者直接访问 **[aidone.cc/skills](https://aidone.cc/skills)** — 在线浏览、一键复制 Prompt，无需手动找文件。

---

### 🤖 Claude Code（一键安装）

```bash
/plugin add github.com/chicogong/visa-skills
```

安装后直接对话：
```
"帮我整理英国签证材料清单"
"我想去法国，申根签证怎么准备"
"把这些表单字段帮我填一下：[粘贴字段]"
```

---

### ⚡ Cursor

```bash
# 安装单个国家（以申根为例）
mkdir -p .cursor/rules
curl -o .cursor/rules/visa-schengen.mdc \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/.cursor.mdc
```

或者在 Cursor 设置 → **Rules** 面板中，手动粘贴 `SKILL.md` 的内容。

---

### 🌊 Windsurf

```bash
mkdir -p .windsurf/skills/visa-schengen
curl -o .windsurf/skills/visa-schengen/SKILL.md \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/SKILL.md
```

---

### 🟡 Trae（字节跳动）

```bash
mkdir -p .trae/rules
curl -o .trae/rules/project_rules.md \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/trae-rule.md
```

或在 Trae 设置 → **Rules & Skills** 中，粘贴 `trae-rule.md` 的内容。

---

### 🟢 通义灵码（阿里云）

```bash
mkdir -p .lingma/rules
curl -o .lingma/rules/visa-schengen.md \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/lingma-rules.md
```

---

### 🧑‍💻 OpenAI Codex CLI / AGENTS.md 标准

```bash
curl -o AGENTS.md \
  https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/AGENTS.md
```

---

### 👾 GitHub Copilot

```bash
mkdir -p .github
cat >> .github/copilot-instructions.md << 'EOF'

$(curl -s https://raw.githubusercontent.com/chicogong/visa-skills/main/schengen/SKILL.md)
EOF
```

---

## 🛡️ 隐私与安全

| 设计原则 | 说明 |
|---------|------|
| ❌ 绝不收集敏感数据 | 所有 Skill 均禁止在对话中索要护照号、身份证号、银行卡号 |
| ✅ 本地文书生成 | 生成正式文书时，引导用户至 aidone.cc 在**本地浏览器**完成（AES-GCM 加密，不上传服务器）|
| ✅ 纯静态 Markdown | 本仓库为纯文本，无服务端，无数据收集，任何人可审计 |
| ⚠️ 仅供参考 | 所有内容为参考建议，不构成法律意见，最终以各国官方签证机构规定为准 |

---

## 🤝 如何贡献

欢迎贡献更多国家/地区的签证 Skill！详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

```bash
# 快速开始
git clone https://github.com/chicogong/visa-skills.git
cd visa-skills
cp templates/SKILL-TEMPLATE.md korea/SKILL.md  # 以韩国为例
# 按模板填写内容，提交 PR
```

**目前最需要的贡献**：🇰🇷 韩国 / 🇹🇭 泰国 / 🇦🇪 迪拜（UAE）/ 🇸🇬 新加坡

---

## 📚 参考资料

值得参考的开源项目：[torlyai/Schengen-master](https://github.com/torlyai/Schengen-master) · [PatrickJS/awesome-cursorrules](https://github.com/PatrickJS/awesome-cursorrules) · [browser-use/browser-use](https://github.com/browser-use/browser-use)

完整列表见 [REFERENCES.md](REFERENCES.md)

---

## 📄 License

[MIT](LICENSE) © [aidone.cc](https://aidone.cc)
