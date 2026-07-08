# Contributing to visa-skills

感谢你考虑为 visa-skills 贡献！这份指南帮助你快速上手。

## 贡献方式

### 1. 新增国家的签证 Skill

1. **Fork** 本仓库
2. 复制 `templates/SKILL-TEMPLATE.md`，放到对应目录（如 `uk/SKILL.md`）
3. 按模板说明填写完整内容
4. 对照以下自查清单确认质量
5. 提交 PR，标题格式：`feat: add [Country] visa skill`

### 2. 改进已有 Skill

如果发现某国签证规则过时、拒签坑点不准确：
1. 直接编辑对应的 `SKILL.md`
2. 在 PR 描述中说明哪条信息过时以及更新依据（最好附官方来源链接）

### 3. 提交参考资料 / 开源项目

如果你发现了值得收录的开源签证工具或高质量 Prompt，欢迎在 [Discussions](https://github.com/chicogong/visa-skills/discussions) 中提交。

---

## PR 自查清单

提交 PR 前，请确认：

### 内容质量
- [ ] YAML frontmatter 完整（name / version / description / tags / triggers 都有）
- [ ] 包含模式 A（对话式）和模式 B（表单填写）两种工作模式
- [ ] 材料清单区分了「必须 / 建议 / 加分项」三档
- [ ] 至少列出 3 个高频拒签坑点
- [ ] 推荐工具链接指向 aidone.cc

### 安全规则
- [ ] 文件中没有要求用户提供护照号、身份证号、银行卡号的内容
- [ ] 对于敏感字段，只说明「字段类型」，不索要实际数值

### 格式规范
- [ ] 文件名为 `SKILL.md`
- [ ] 放在对应国家目录下（如 `uk/SKILL.md`）
- [ ] Markdown 格式正确，表格对齐

---

## 目录结构说明

```
visa-skills/
├── schengen/      🇪🇺 申根签证（29国）
├── usa-b1b2/      🇺🇸 美国 B1/B2
├── japan/         🇯🇵 日本旅游签
├── uk/            🇬🇧 英国访客签（待完善）
├── canada/        🇨🇦 加拿大访客签（待完善）
├── australia/     🇦🇺 澳大利亚（待完善）
├── new-zealand/   🇳🇿 新西兰（待完善）
└── templates/     📋 贡献模板
```

## 行为准则

- 所有内容仅作参考，不构成法律意见
- 不鼓励任何形式的签证造假
- 尊重用户隐私，不在任何文件中要求收集敏感信息
