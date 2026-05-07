# NovelWeaver - 全能网文写作助手

> 整合业界优秀网文写作工具理念，通过简洁指令+自然语言，帮你从零创作高质量长篇小说。

[![Version](https://img.shields.io/badge/version-1.5.0-blue.svg)](SKILL.md)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Trae](https://img.shields.io/badge/Trae-Skill-purple.svg)](https://trae.com)
[![Claude](https://img.shields.io/badge/Claude-Skill-orange.svg)](https://claude.ai)

---

## 一句话介绍

网文创作全流程技能：初始化 → 大纲 → 幕规划 → 章节写作 → 审查 → 记忆更新 → 阶段总结。

---

## 核心能力

| 能力 | 说明 |
|------|------|
| 智能创作引导 | AI引导完成6问：情绪标签→题材→简介→主角+反差点→核心冲突→章节数 |
| 22位作者文风库 | 覆盖搞笑、热血、文青、严谨等7大流派，智能推荐+场景切换 |
| 幕系统 | 卷内剧情弧，6条分支走向（A主线/B危机/C支线/D缓冲/E回环/F颠覆），偏离检查 |
| 33维度质量审计 | 角色、世界观、情节、叙事、文字全覆盖，AI味检测 |
| 三重记忆系统 | 真相文件 + 长程上下文 + 实体关系，长篇写作不忘事 |
| 情绪曲线 + 节奏控制 | 每3章"压-小扬-压-爆"循环，S1-S5五级评级 |
| 阶段总结 | 每10章/50章/卷末自动生成总结 |
| Python预处理脚本 | chapter_info.py / volume_batch.py / hook_report.py 节省 ~90% token |

---

## 快速上手

### 第一步：初始化项目

```
/nw init 开始写小说
```

### 第二步：生成大纲

```
/nw plan 帮我生成总大纲
```

### 第三步：开始写作

```
/nw write 写第一章
```

AI自动完成：写作 → 审查 → 字数检查 → 更新大纲 → 更新记忆 → 摘要 → 进度提示

### 日常循环

```
/nw write 继续写 → 看结果 → 满意继续 / 不满意 /nw review fix
/nw act 下一幕怎么走 → 选择分支 → 继续写作
```

---

## 核心指令

| 指令 | 说明 | 示例 |
|------|------|------|
| `/nw init` | 开始写小说 | `/nw init 开始写一本修仙小说` |
| `/nw write` | 写/续写章节 | `/nw write 写第一章` |
| `/nw review` | 审查（一致性+AI味+节奏+约束） | `/nw review` |
| `/nw memory` | 查看/管理设定 | `/nw memory 主角什么等级` |
| `/nw plan` | 生成大纲/卷计划 | `/nw plan 规划第一卷` |
| `/nw act` | 下一幕剧情规划 | `/nw act 下一幕怎么走` |
| `/nw help` | 帮助信息 | `/nw help` |

扩展指令：`/nw style`（文风） `/nw expand`（扩写） `/nw stats`（字数） `/nw inspire`（灵感） `/nw summary`（总结）

---

## 内置资源

- **22位作者文风库** - styles/ 目录，7大流派
- **17个参考文档** - references/ 目录，含37种题材规则、黄金开篇、情绪曲线等
- **14个模板** - templates/ 目录，大纲、章节、角色、场景、伏笔等
- **6个Python脚本** - scripts/ 目录，字数检查、章节提取、卷级汇总、钩子报告、一致性扫描、AI味检测

---

## 多 IDE 兼容

本技能兼容以下 AI IDE（完整安装指南见仓库 [INSTALL.md](../INSTALL.md)）：

| IDE | 安装路径 |
|-----|----------|
| Trae | `.trae/skills/novel-weaver/` |
| Claude Code | `.claude/skills/novel-weaver/` |
| Cline / Roo Code | `.clinerules/novel-weaver/` |
| OpenCode | `.opencode/skills/novel-weaver/` |
| Cursor | `.cursor/rules/` |
| GitHub Copilot | `.github/copilot-instructions.md` |
| Continue | `.continue/rules/` |

---

*NovelWeaver v1.5.0 - 指令 `/nw` + 语义，用说话的方式写小说*
