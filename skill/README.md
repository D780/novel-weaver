# NovelWeaver - 全能网文写作助手

> 整合业界优秀网文写作工具理念，通过简洁指令+自然语言，帮你从零创作高质量长篇小说。

[![Version](https://img.shields.io/badge/version-1.2.0-blue.svg)](https://github.com/novel-weaver)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Trae IDE](https://img.shields.io/badge/Trae%20IDE-Skill-purple.svg)](https://trae.com)

---

## ✨ 核心能力

| 能力 | 说明 |
|------|------|
| 🎯 智能创作引导 | AI引导填写书名、题材、主角、文风，自动生成大纲 |
| 🎨 22位作者文风库 | 覆盖搞笑、热血、文青、严谨等6大流派，智能推荐+场景切换 |
| 🔍 33维度质量审计 | 角色、世界观、情节、叙事、文字全覆盖，AI味检测 |
| 🧠 三重记忆系统 | 真相文件 + 长程上下文 + 实体关系，长篇写作不忘事 |
| 📊 节奏控制 | S1-S5五级节奏评级，卷级节奏曲线分析 |
| 📝 阶段总结 | 每10章/50章/卷末自动生成总结，记录剧情和伏笔状态 |
| 💡 灵感助手 | 基于当前剧情，给出短期/长期走向建议、冲突设计、爽点建议 |
| 🔢 字数统计 | 自动检查字数，不达标时精细扩写 |
| 🎭 创意约束 | 三轴混搭、反套路触发器、镜像对抗、约束继承 |

---

## 🚀 快速开始

### 第一步：初始化项目

```
/nw init 开始写小说
```

AI会引导你完成：书名、题材、主角设定、文风选择、故事基调。

### 第二步：生成大纲

```
/nw plan 帮我生成总大纲
```

### 第三步：开始写作

```
/nw write 写第一章
```

AI会自动：生成内容 → 质量审查 → 更新记忆 → 生成前情摘要 → 提供后续建议

### 日常循环

```
/nw write 写第X章 → 看结果 → 满意继续 / 不满意 /nw review fix
```

---

## 📋 核心指令

> 指令分三级：**核心**（5个）→ **扩展**（6个）→ **高级**（子指令，极少用）

### 一级：核心指令（仅需记 5 个）

| 指令 | 说明 | 示例 |
|------|------|------|
| `/nw init` | 开始写小说 | `/nw init 开始写一本小说` |
| `/nw write` | 写/续写章节 | `/nw write 写第一章` |
| `/nw review` | 审查（含一致性、AI味、节奏、约束） | `/nw review` |
| `/nw memory` | 查看/管理设定 | `/nw memory 主角什么等级` |
| `/nw help` | 帮助信息 | `/nw help` |

### 二级：扩展指令（经常用）

| 指令 | 说明 | 示例 |
|------|------|------|
| `/nw plan` | 生成大纲/规划 | `/nw plan 规划第一卷` |
| `/nw style` | 切换文风 | `/nw style 换辰东风格` |
| `/nw expand` | 扩写章节 | `/nw expand` |
| `/nw stats` | 字数统计 | `/nw stats` |
| `/nw inspire` | 灵感建议 | `/nw inspire` |
| `/nw summary` | 阶段总结 | `/nw summary` |

---

## 📚 内置资源

### 22位作者文风库

| 流派 | 作者 |
|------|------|
| 搞笑幽默 | 弈青峰、会说话的肘子、三天两觉、卖报小郎君 |
| 热血升级 | 天蚕土豆、唐家三少、我吃西红柿、辰东、滚开 |
| 细腻文青 | 猫腻、烽火戏诸侯、愤怒的香蕉、耳根 |
| 严谨设定 | 爱潜水的乌贼、忘语、言归正传 |
| 特色领域 | 蝴蝶蓝、天下霸唱、月关、萧鼎 |
| 多神话热血 | 三九音域 |
| 悬疑推理 | 杀虫队队员 |

### 13个创作模板

创作宪法、总大纲、卷计划、章节、角色档案、场景、伏笔管理、审查报告、世界观设定、力量体系、10章小总结、50章大总结、卷总结

### 11个参考文档

37种题材规则、33维度审计、反AI味指南、文风模仿、记忆系统、写作方法、创意约束、一致性检查、实体管理、节奏分析、使用指南

---

## 🏗️ 项目结构

```
.trae/skills/novel-weaver/
├── SKILL.md                    # 主技能文件
├── references/                 # 参考文档（11个）
│   ├── genre-rules.md
│   ├── audit-dimensions.md
│   ├── anti-ai-patterns.md
│   ├── style-imitation.md
│   ├── memory-system.md
│   ├── writing-methods.md
│   ├── usage-guide.md
│   ├── creative-constraints.md
│   ├── consistency-checker.md
│   ├── data-agent.md
│   └── pacing-analysis.md
├── styles/                     # 文风库（22位作者）
│   ├── author-styles.md
│   └── authors/
├── templates/                  # 模板（13个）
│   ├── chapter.md
│   ├── constitution.md
│   ├── outline.md
│   ├── volume-plan.md
│   ├── character-profile.md
│   ├── scene-template.md
│   ├── hook-template.md
│   ├── review-report.md
│   ├── world-setting.md
│   ├── power-system.md
│   ├── summary-10chapters.md
│   ├── summary-50chapters.md
│   └── summary-volume.md
└── scripts/                    # 脚本工具（5个）
    ├── README.md
    ├── word-count.md
    ├── chapter-analyzer.md
    ├── word-check-expand.md
    └── inspiration.md
```

---

## 📖 详细文档

- [使用指南](references/usage-guide.md) - 快速开始、进阶用法、问题排查
- [文风模仿指南](references/style-imitation.md) - 内置文风使用、自定义文风
- [记忆系统](references/memory-system.md) - 三重记忆架构说明
- [脚本工具](scripts/README.md) - 字数统计、章节分析、灵感助手

---

## 🔧 工作流程

### 写作完成后自动执行

```
/nw write 继续写，主角发现了敌人
    ↓
[1] 质量审查（33维度 + AI味 + 一致性 + 追读力 + 字数）
    ↓
[2] 更新记忆（世界状态 + 角色状态 + 伏笔追踪）
    ↓
[3] 阶段总结（每10章/50章/卷末自动触发）
    ↓
[4] 前情摘要（概括前3章 + 当前状态 + 未回收伏笔）
    ↓
[5] 后续建议 + 灵感（A/B/C走向 + /nw inspire）
```

---

## 📄 License

MIT License

---

*NovelWeaver v1.2 - 指令 `/nw` + 语义，用说话的方式写小说*
