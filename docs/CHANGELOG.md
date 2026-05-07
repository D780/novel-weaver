# NovelWeaver 变更日志

所有重要变更将记录在此文件中。

格式参考 [Keep a Changelog](https://keepachangelog.com/)。

## [Unreleased]

### 新增
- 3个新Python脚本：hook_report.py（钩子密度报告）、consistency_scan.py（一致性扫描）、style_check.py（AI味检测）
- nw_utils.py 公共工具模块，消除脚本间重复代码
- INSTALL.md 多IDE安装指南（9种AI IDE）
- 多IDE兼容支持（Trae/Claude/Cursor/Cline/Roo/Copilot/Continue/OpenCode/Windsurf）

### 修复
- SKILL.md 指令层级统一：核心指令7个（含plan/act），扩展指令5个，消除重复
- usage-guide.md 分支示例从4条更新为6条（A-F）
- constitution.md 和 memory-system.md 中 `.trae/` 路径泛化为相对路径
- .gitignore 增加各IDE规则目录排除

### 优化
- 脚本代码去重：`extract_characters`、`detect_hook`、`chapter_sort_key`、`clean_markdown` 等重复函数统一提取到 nw_utils.py
- 脚本体积缩减：`chapter_info.py` 从167行→61行，`check_wordcount.py` 从219行→98行
- skill/README.md 重写为技能级快速参考
- 根 README.md 全面更新到 v1.5.0
- scripts/README.md 增加公共模块说明和6个脚本的完整说明

---

## [1.5.0] - 2026-05

### 新增
- 幕系统完善：6条分支走向（A主线/B危机/C支线/D缓冲/E回环/F颠覆）
- 偏离影响分析（🟢🟡🟠🔴四级）
- 大幕分段机制、幕大纲、AI推荐、可调章节数
- Python 预处理脚本：chapter_info.py（单章结构化提取）、volume_batch.py（卷级批量汇总）
- 每次写入后强制更新链：写作→审查→字数检查→更新大纲→更新记忆→摘要→进度
- 多 IDE 兼容支持（Trae/Claude/Cursor/Cline/Roo/Copilot/Continue/OpenCode/Windsurf）
- INSTALL.md 多 IDE 安装指南
- 3个新脚本：hook_report.py、consistency_scan.py、style_check.py

### 修复
- 字符提取过滤：修复代词+动词模式导致的噪音识别
- 工作流程整合：脚本在 /nw write 和 /nw act 时自动运行
- SKILL.md 指令层级统一（核心7个，扩展5个）
- .gitignore 增加各 IDE 规则目录排除

---

## [1.4.0] - 2026-05

### 新增
- 情绪标签系统：6大情绪标签对应不同节奏模板
- 黄金开篇锻造术：写第一章时自动生成3版开篇+避雷针检查
- 情绪曲线"压-小扬-压-爆"3章循环
- content-expansion.md：7种内容扩充技巧
- dialogue-writing.md：对话写作规范
- plot-structures.md：情节结构模板
- emotion-curve.md：情绪曲线系统
- golden-opening.md：黄金开篇参考文档
- Python字数检查脚本（check_wordcount.py）

### 优化
- 情绪曲线与节奏分析连接
- 统一init流程6问顺序
- 修正黄金开篇触发时机
- 去除重复内容

---

## [1.3.0] - 2026-05

### 重构
- 消除 SKILL.md 中的重复内容（指令速查表、工作流描述）
- 将详细工作流程移到 references/usage-guide.md，SKILL.md 中保留引用
- 将完整文风库内容移到 styles/author-styles.md，SKILL.md 中保留精简版

### 优化
- 文风库按 7 大流派分类组织（原 22 个文件平铺）
- SKILL.md 从 718 行精简至 363 行（约 50% 缩减）
- 更新 styles/author-styles.md 中文风文件的链接路径

### 新增
- 独立开源项目结构（skill/ 目录 + docs/ 文档）
- README.md（面向 GitHub 访问者）
- CONTRIBUTING.md（贡献指南）
- LICENSE（MIT 许可证）
- .gitignore（排除运行时数据）

---

## [1.2.0] - 2026-04

### 重构
- 三级指令体系：核心（5个）→ 扩展（6个）→ 高级（7个子指令）
- 合并 `/nw check`、`/nw analyze`、`/nw pacing`、`/nw constraint`、`/nw consistency`、`/nw fix` 到 `/nw review`
- 合并 `/nw entity`、`/nw outline` 到 `/nw memory`
- `/nw stats wordcount` → `/nw stats`

### 优化
- 核心指令从 19 个精简到 5 个
- 用户只需记住 `/nw init`、`/nw write`、`/nw review`、`/nw memory`、`/nw help`
- 其余功能用自然语言或二级扩展指令调用

## [1.1.0] - 2026-04

### 新增
- RAG 检索增强：AI 自动检索规则、指令驱动检索矩阵、语义检索指引
- `/nw consistency` 指令：实时一致性校验
- `/nw fix` 指令：AI 自动修复审查发现的问题

### 优化
- 简化指令系统：合并冗余子命令，用户只需记住核心指令
- 统一 `/nw review`、`/nw check`、`/nw analyze` 的使用方式
- 移除 `/nw check wordcount` 等重叠指令
- 优化指令速查表，减少用户记忆负担

### 修复
- 模板计数不一致（SKILL.md 说 10 个，实际 13 个）
- 脚本计数不一致（SKILL.md 说 4 个，实际 5 个）
- 描述文案错误（"46 个参考文档"）
- 指令速查表缺少 `/nw summary`、`/nw inspire`、`/nw consistency`、`/nw fix`

---

## [1.0.0] - 2026-04

### 新增
- 完整创作流程：初始化 → 大纲 → 写作 → 审查 → 记忆更新
- 22 位作者文风库：搞笑、热血、文青、严谨等 6 大流派
- 33 维度质量审计：角色、世界观、情节、叙事、文字全覆盖
- 三重记忆系统：真相文件 + 长程上下文 + 实体关系
- S1-S5 五级节奏评级
- 三轴混搭创意约束系统
- 阶段总结：每 10 章/50 章/卷末自动生成
- 灵感助手：剧情走向建议、冲突设计、爽点建议
- 字数统计与自动扩写
- 11 个参考文档、13 个创作模板、5 个脚本工具
