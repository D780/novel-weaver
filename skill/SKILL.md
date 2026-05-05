---
name: novel-weaver
description: 全能网文写作辅助技能
license: MIT
metadata:
  version: "1.3.0"
  author: NovelWeaver Contributors
  tags: [writing, novel, webnovel, creative, chinese]
---

# NovelWeaver - 全能网文写作助手

## 一句话介绍

整合业界优秀网文写作工具理念，通过简洁指令+自然语言，帮你从零创作高质量长篇小说。

---

## 核心能力

### 1. 智能创作引导

| 能力 | 说明 | 指令 |
|------|------|------|
| 项目初始化 | AI引导填写书名、题材、主角、文风等 | `/nw init` |
| 大纲生成 | 基于设定自动生成三幕结构大纲 | `/nw plan` |
| 卷计划 | 分卷规划章节安排 | `/nw plan 规划第一卷` |
| 章节写作 | 自动读取上下文，应用文风 | `/nw write` |

### 2. 文风系统

| 能力 | 说明 |
|------|------|
| 22位作者文风库 | 覆盖搞笑、热血、文青、严谨等7大流派 |
| 智能推荐 | 根据题材自动推荐合适文风 |
| 场景切换 | 不同场景使用不同文风 |
| 自定义文风 | 支持学习用户个人写作风格 |

> 文风库详见 [styles/author-styles.md](styles/author-styles.md)

### 3. 质量保障

| 能力 | 说明 |
|------|------|
| 33维度审计 | 角色、世界观、情节、叙事、文字全覆盖 |
| AI味检测 | 识别套话、情感空洞、描写模式化 |
| 一致性检查 | 角色OOC、设定冲突、时间线验证 |
| 追读力分析 | Hook质量、爽点、弃读风险评估 |

### 4. 记忆与实体（RAG 检索增强）

| 能力 | 说明 |
|------|------|
| 三重记忆 | 真相文件 + 长程上下文 + 实体关系 |
| 智能检索 | 写作前自动检索相关设定、前文、角色档案 |
| 实体管理 | 角色/物品/地点/势力的自动提取与管理 |
| 伏笔追踪 | 自动记录埋设/回收状态 |
| 状态同步 | 每章后自动更新世界状态 |

#### 检索规则（AI 自动执行，用户无感知）

| 用户指令 | AI 自动检索范围 | 检索目标 |
|---------|----------------|---------|
| `/nw write` | truth-files/、novels/、.novel-weaver/summaries/ | 角色设定、世界观、力量体系、前文相关章节、大纲 |
| `/nw memory` | truth-files/、.novel-weaver/chapters/ | 角色档案、世界状态、伏笔表、相关章节 |
| `/nw review` | 被审查章节、truth-files/、前3章 | 角色设定、前文情节、审查规则、一致性验证所需全部设定 |
| `/nw plan` | outline.md、truth-files/、已写卷 | 总大纲、当前设定、已有内容 |
| `/nw stats` | novels/volume-XX/chapters/ | 章节文件统计字数 |

### 5. 节奏控制

| 能力 | 说明 |
|------|------|
| 章节节奏 | S1-S5五级节奏评级 |
| 卷级节奏 | 整卷节奏曲线分析 |
| 节奏建议 | 自动建议节奏调整 |

### 6. 创意约束

| 能力 | 说明 |
|------|------|
| 三轴混搭 | 风格轴+冲突轴+节奏轴组合防重复 |
| 反套路触发器 | 检测常见套路并自动改写 |
| 镜像对抗 | 确保冲突双方有对等合理性 |
| 约束继承 | 新章节继承前文约束，禁止随意发明设定 |

### 7. 脚本工具

| 能力 | 说明 |
|------|------|
| 字数统计 | 统计章节/卷/书字数，支持范围检查 |
| 章节分析 | 多维度分析章节质量（节奏、爽点、Hook等） |
| 自动扩写 | 字数不达标时自动精细扩写 |
| 数据分析 | 卷级/全书级数据统计和趋势分析 |

### 8. 总结与回顾

| 能力 | 说明 |
|------|------|
| 小总结 | 每10章自动生成，记录剧情进展和伏笔状态 |
| 大总结 | 每50章全面回顾，包含角色成长和世界观展开 |
| 卷总结 | 每卷结束总结，包含下一卷衔接建议 |
| 剧情回顾 | 随时查看已写内容的剧情概要 |

### 9. 灵感助手

| 能力 | 说明 |
|------|------|
| 剧情建议 | 基于当前剧情，给出短期/长期走向建议 |
| 冲突设计 | 设计人际/内在/外部冲突 |
| 爽点建议 | 设计多样化爽点（打脸、逆袭、突破等） |
| 角色建议 | 新角色出场建议和角色关系设计 |

---

## 快速上手

### 第一步：初始化项目

```
/nw init 开始写小说
```

AI会引导你完成以下配置：
- **基础信息**：书名、题材、一句话简介、目标平台、目标字数
- **主角设定**：姓名、身份、性格、核心目标
- **文风选择**：根据题材自动推荐，也可手动选择
- **故事基调**：轻松/严肃/热血/悲壮等

### 第二步：生成大纲

```
/nw plan 帮我生成总大纲
```

AI会根据你的设定生成：
- 完整故事大纲（三幕结构）
- 角色详细设定
- 世界观框架
- 分卷大纲

### 第三步：开始写作

```
/nw write 写第一章
```

AI会自动完成：
- 读取创作宪法和大纲，应用目标文风
- 生成章节内容
- **自动审查质量**（AI味检测、一致性检查、追读力分析）
- **更新记忆文件**（世界状态、角色状态、伏笔追踪）
- **生成前情摘要**和**后续建议**（3个剧情走向）

---

## 推荐工作流

### 从零到一（新书启动）

```
/nw init 开始写一本修仙小说
    ↓ AI引导填写：书名、题材、主角、文风
/nw plan 帮我生成总大纲
    ↓ AI生成：三幕结构大纲 + 角色设定 + 世界观 + 分卷大纲
/nw write 写第一章
    ↓ 进入日常循环
```

### 日常写作循环（核心）

```
/nw write 继续写，主角发现了敌人
    ↓ AI自动完成：写作 → 审查 → 更新记忆 → 前情摘要 → 后续建议
[看结果] → 满意 → /nw write 继续
            → 不满意 → /nw review fix 帮我改一下
```

> 详细工作流程请查阅 [references/usage-guide.md](references/usage-guide.md)

---

## 指令参考

> 指令分三级：**核心**（每天用）→ **扩展**（经常用）→ **高级**（极少用，作为子指令）

### 一级：核心指令（必须用，仅需记 5 个）

| 指令 | 一句话说明 | 使用示例 |
|------|-----------|---------|
| `/nw init` | 开始写小说 | `/nw init 开始写一本修仙小说` |
| `/nw write` | 写/续写章节 | `/nw write 写第一章` |
| `/nw review` | 审查（含一致性、AI味、节奏、约束等全部检查） | `/nw review` 或 `/nw review 第三章` |
| `/nw memory` | 查看/管理一切设定 | `/nw memory 主角什么等级` |
| `/nw help` | 帮助信息 | `/nw help` |

### 二级：扩展指令（经常用）

| 指令 | 一句话说明 | 使用示例 |
|------|-----------|---------|
| `/nw plan` | 生成大纲/卷计划 | `/nw plan 规划第一卷` |
| `/nw style` | 切换/推荐文风 | `/nw style 换辰东风格` |
| `/nw expand` | 扩写章节 | `/nw expand` 或 `/nw expand 增加500字` |
| `/nw inspire` | 灵感建议 | `/nw inspire` |
| `/nw stats` | 字数统计 | `/nw stats` 或 `/nw stats volume` |
| `/nw summary` | 阶段总结 | `/nw summary` |

### 三级：高级指令（极少用，作为子指令存在）

| 子指令 | 归属 | 说明 | 等效说法 |
|--------|------|------|---------|
| `/nw review consistency` | `/nw review` | 一致性检查 | `/nw review 有没有矛盾` |
| `/nw review pacing` | `/nw review` | 节奏分析 | `/nw review 节奏怎么样` |
| `/nw review constraint` | `/nw review` | 约束检查 | `/nw review 有没有套路重复` |
| `/nw review fix` | `/nw review` | AI 自动修复 | `/nw review 帮我改一下` |
| `/nw memory entity` | `/nw memory` | 实体管理 | `/nw memory 列出所有角色` |
| `/nw memory outline` | `/nw memory` | 查看大纲 | `/nw memory 大纲是什么` |
| `/nw analyze` | `/nw review` | 追读力分析 | `/nw review 这章好看吗` |

---

## 文风推荐系统

在创建项目时，AI会根据题材自动推荐合适的文风：

| 题材 | 推荐文风 | 理由 |
|------|---------|------|
| 玄幻修仙 | 天蚕土豆、辰东 | 热血升级，宏大世界观 |
| 都市搞笑 | 弈青峰、会说话的肘子 | 幽默接地气 |
| 仙侠探案 | 卖报小郎君 | 探案+仙侠+搞笑 |
| 悬疑诡秘 | 爱潜水的乌贼 | 设定严谨，逻辑严密 |
| 历史权谋 | 猫腻、愤怒的香蕉 | 文笔细腻，深度思考 |
| 凡人流 | 忘语、言归正传 | 严谨稳健 |
| 电竞网游 | 蝴蝶蓝 | 群像精彩，热血 |
| 无限流 | 三天两觉、杀虫队队员 | 吐槽玩梗/烧脑轮回 |
| 盗墓探险 | 天下霸唱 | 江湖气，民俗悬疑 |
| 极道诡异 | 滚开 | 黑暗杀伐，加点升级 |
| 稳健搞笑 | 言归正传 | 反套路，苟道 |
| 多神话热血 | 三九音域 | 多神话融合，守夜人家国 |
| 悬疑推理 | 杀虫队队员 | 反爽文，智商博弈 |

> 完整22位作者文风库详见 [styles/author-styles.md](styles/author-styles.md)

---

## 项目结构

### 技能静态内容

```
.
├── SKILL.md                    # 主技能文件
├── references/                 # 参考文档（11个）
│   ├── genre-rules.md          # 37种题材写作规则
│   ├── audit-dimensions.md     # 33维度审计系统
│   ├── anti-ai-patterns.md     # 反AI味指南
│   ├── style-imitation.md      # 文风模仿指南
│   ├── memory-system.md        # 记忆系统说明
│   ├── writing-methods.md      # 写作方法
│   ├── usage-guide.md          # 使用指南
│   ├── creative-constraints.md # 创意约束系统
│   ├── consistency-checker.md  # 一致性检查器
│   ├── data-agent.md           # 实体管理代理
│   └── pacing-analysis.md      # 节奏分析系统
├── styles/                     # 文风库
│   ├── author-styles.md        # 文风汇总
│   └── authors/                # 22位作者文风（按流派分类）
├── templates/                  # 模板文件（13个）
│   ├── chapter.md              # 章节模板
│   ├── constitution.md         # 创作宪法模板
│   ├── outline.md              # 大纲模板
│   └── ...
└── scripts/                    # 脚本工具（5个）
    ├── README.md               # 脚本使用说明
    ├── word-count.md           # 字数统计脚本
    ├── chapter-analyzer.md     # 章节分析工具
    ├── word-check-expand.md    # 字数检查与扩写
    └── inspiration.md          # 灵感助手脚本
```

### 项目运行时数据（用户项目生成）

```
.novel-weaver/
├── memory/               # 创作记忆
│   ├── constitution.md   # 创作宪法
│   └── personal-voice.md # 个人语料
├── truth-files/          # 真相文件
│   ├── current-state.md  # 世界状态
│   ├── characters.md     # 角色档案
│   ├── world-setting.md  # 世界观
│   ├── pending-hooks.md  # 伏笔表
│   └── power-system.md   # 力量体系
├── chapters/             # 章节正文
├── reviews/              # 审查报告
└── analysis/             # 分析数据

novels/                   # 小说正文
├── outline.md            # 总大纲
└── volume-01/            # 第一卷
    ├── plan.md           # 卷计划
    └── chapters/         # 章节正文
```

---

## 参考文档

| 文档 | 说明 |
|------|------|
| [genre-rules.md](references/genre-rules.md) | 37种题材写作规则 |
| [audit-dimensions.md](references/audit-dimensions.md) | 33维度审计系统 |
| [anti-ai-patterns.md](references/anti-ai-patterns.md) | 反AI味指南 |
| [style-imitation.md](references/style-imitation.md) | 文风模仿指南 |
| [memory-system.md](references/memory-system.md) | 记忆系统 |
| [writing-methods.md](references/writing-methods.md) | 写作方法 |
| [usage-guide.md](references/usage-guide.md) | 使用指南 |
| [creative-constraints.md](references/creative-constraints.md) | 创意约束系统 |
| [consistency-checker.md](references/consistency-checker.md) | 一致性检查器 |
| [data-agent.md](references/data-agent.md) | 实体管理代理 |
| [pacing-analysis.md](references/pacing-analysis.md) | 节奏分析系统 |

## 脚本工具

| 脚本 | 说明 |
|------|------|
| [word-count.md](scripts/word-count.md) | 字数统计 |
| [chapter-analyzer.md](scripts/chapter-analyzer.md) | 章节分析 |
| [word-check-expand.md](scripts/word-check-expand.md) | 字数检查扩写 |

### 模板清单

| 模板 | 用途 |
|------|------|
| `constitution.md` | 创作宪法 |
| `outline.md` | 总大纲 |
| `volume-plan.md` | 卷计划 |
| `chapter.md` | 章节模板 |
| `character-profile.md` | 角色档案 |
| `scene-template.md` | 场景规划 |
| `hook-template.md` | 伏笔管理 |
| `review-report.md` | 审查报告 |
| `world-setting.md` | 世界观设定 |
| `power-system.md` | 力量体系 |
| `summary-10chapters.md` | 10章小总结 |
| `summary-50chapters.md` | 50章大总结 |
| `summary-volume.md` | 卷总结 |

---

## 版本历史

| 版本 | 日期 | 更新内容 |
|------|------|---------|
| 1.0.0 | 2026-04 | 初始版本 - 完整创作流程、文风系统、质量保障、阶段总结、灵感助手 |
| 1.1.0 | 2026-04 | RAG 检索增强 - AI 自动检索规则、指令驱动检索矩阵、语义检索指引 |
| 1.2.0 | 2026-04 | 指令精简 - 三级指令体系（5核心+6扩展+7子指令）、合并审查/节奏/约束/一致性到 /nw review |
| 1.3.0 | 2026-05 | 结构优化 - 消除SKILL.md重复内容、文风库按流派分类、精简至350行 |

---

*NovelWeaver v1.3.0 - 指令 `/nw` + 语义，用说话的方式写小说*
