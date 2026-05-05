# 脚本工具使用说明

## 概述

NovelWeaver 提供多种脚本工具，帮助作者进行数据统计、分析和质量控制。

## 工具列表

| 工具 | 功能 | 触发方式 |
|------|------|---------|
| 字数统计 | 统计章节/卷/书字数 | `/nw stats` |
| 章节分析 | 全面分析章节质量 | `/nw review` |
| 自动扩写 | 字数不达标时扩写 | `/nw expand` |
| 灵感助手 | 剧情走向建议、冲突设计 | `/nw inspire` |

## 使用场景

### 写作完成后

```
/nw write 写第一章
    ↓
[AI自动执行]
- 字数检查
- 33维度审计
- AI味检测
- 一致性检查
- 追读力分析
    ↓
[自动回顾]
- 审查报告
- 前情摘要
- 后续建议
```

### 手动检查

```
/nw stats                   # 查看字数
/nw review                  # 分析章节
/nw review                  # 全面审查
/nw review consistency      # 检查一致性
```

### 批量统计

```
/nw stats volume            # 统计整卷字数
/nw stats all               # 统计全书字数
```

## 字数配置

### 初始化时设置

```
/nw init 写一本小说，每章2500-3500字
```

### 修改配置

```
/nw memory 更新字数要求，每章3000-5000字
```

### 配置位置

`.novel-weaver/memory/constitution.md` 中：

```markdown
## 字数要求
- 最低字数：2500字
- 最高字数：3500字
- 理想字数：2800-3200字
```

## 指令汇总

| 指令 | 说明 |
|------|------|
| `/nw stats` | 统计字数 |
| `/nw stats volume` | 统计整卷 |
| `/nw stats all` | 统计全书 |
| `/nw review` | 分析章节 |
| `/nw review` | 全面审查 |
| `/nw review consistency` | 检查一致性/AI味 |
| `/nw expand` | 扩写当前章 |
| `/nw expand 增加500字` | 指定扩写量 |
