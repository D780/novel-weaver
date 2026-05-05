# NovelWeaver 变更日志

所有重要变更将记录在此文件中。

格式参考 [Keep a Changelog](https://keepachangelog.com/)。

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
