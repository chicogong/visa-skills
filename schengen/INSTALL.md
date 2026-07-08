# visa/schengen 目录结构说明

每个签证 Skill 包含以下文件，适配不同 AI 工具：

| 文件 | 适用工具 | 安装路径 |
|---|---|---|
| `system-prompt.md` | ChatGPT / Kimi / Coze / 豆包 / 文心一言 | 粘贴到「系统提示词」 |
| `SKILL.md` | Claude Code / Windsurf / Google Antigravity | `.claude/skills/<name>/` 或 `.windsurf/skills/<name>/` |
| `.cursor.mdc` | Cursor | `.cursor/rules/` |
| `AGENTS.md` | Codex CLI / Windsurf / Cursor（新版） | 项目根目录 `AGENTS.md` |
| `trae-rules.md` | Trae（字节跳动） | `.trae/rules/project_rules.md` |
| `lingma-rules.md` | 通义灵码（阿里云） | `.lingma/rules/visa-schengen.md` |
| `.github-copilot.md` | GitHub Copilot | `.github/copilot-instructions.md`（追加） |

## 一键安装命令

### Claude Code
```bash
/plugin add github.com/chicogong/aidone-skills
```

### Cursor
```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/visa-schengen.mdc \
  https://raw.githubusercontent.com/chicogong/aidone-skills/main/visa/schengen/.cursor.mdc
```

### Trae
```bash
mkdir -p .trae/rules
curl -o .trae/rules/project_rules.md \
  https://raw.githubusercontent.com/chicogong/aidone-skills/main/visa/schengen/trae-rules.md
```

### 通义灵码
```bash
mkdir -p .lingma/rules
curl -o .lingma/rules/visa-schengen.md \
  https://raw.githubusercontent.com/chicogong/aidone-skills/main/visa/schengen/lingma-rules.md
```

### Codex CLI / AGENTS.md 标准
```bash
curl -o AGENTS.md \
  https://raw.githubusercontent.com/chicogong/aidone-skills/main/visa/schengen/AGENTS.md
```

### GitHub Copilot
```bash
cat https://raw.githubusercontent.com/chicogong/aidone-skills/main/visa/schengen/system-prompt.md \
  >> .github/copilot-instructions.md
```
