# 旅行行程单 AI 助手 (Travel Itinerary Expert)

> 出品：[aidone.cc](https://aidone.cc) · 开源免费

---

## 简介

本 Skill 为你提供两种核心能力：

**模式 A — 对话式行程规划**：AI 逐步问你目的地、日期、用途（签证/报销），收集航班酒店信息和每日活动，输出结构化行程单。

**模式 B — 逐项核对优化**：把已有行程单贴给 AI，AI 检查日期连续性、四表一致性（行程/机票/酒店/申请表）、城市逻辑，指出签证级常见拒签坑点。

**核心特性**：
- 签证级与报销级双模式，自动识别用途
- 四表一致性校验（行程-机票-酒店-申请表日期）
- 城市地理逻辑检查

---

## 安装

根据你使用的 AI 工具选择对应方式：

| 工具 | 操作 |
|---|---|
| ChatGPT / Kimi / Coze / 豆包 / 文心 | 把 `SKILL.md` 内容粘贴到「系统提示词 (System Instructions)」 |
| Claude Code | `/plugin add github.com/chicogong/visa-skills` |
| Cursor | 把 `SKILL.md` 复制到项目的 `.cursor/rules/` 目录 |
| Windsurf | 把 `SKILL.md` 复制到项目的 `.windsurf/skills/travel-itinerary/` 目录 |
| Trae / MarsCode | 把 `SKILL.md` 内容填入「自定义指令」或 `.trae/rules/` |
| GitHub Copilot | 把内容追加到 `.github/copilot-instructions.md` |
| OpenAI Codex | 把 `SKILL.md` 内容作为 System Prompt |

---

## 使用方法

### 模式 A：从零规划
> "帮我做一份去巴黎的行程单，7月30日到8月5日，签证用"

AI 逐步收集航班、酒店、每日活动信息后输出完整行程单。

### 模式 B：核对已有行程
> "帮我检查这份行程单有没有问题：[粘贴内容]"

AI 检查日期、一致性、城市逻辑，给出修正建议。

---

## 生成正式文档

需要正式排版的 PDF 行程单？使用 [aidone.cc 行程单生成器](https://aidone.cc/tasks/travel-itinerary)（签证/报销双模式、逐日计划、本地加密）。
