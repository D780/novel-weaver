# NovelWeaver - 全能网文写作助手

> 整合业界优秀网文写作工具理念，通过简洁指令+自然语言，帮你从零创作高质量长篇小说。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.3.0-blue.svg)](skill/SKILL.md)

## 核心能力

- **智能创作引导** - 从书名、题材到角色设定，AI 引导你完成创作准备
- **22位作者文风库** - 覆盖搞笑、热血、文青、严谨等 7 大流派，支持智能推荐
- **33维度质量审计** - AI味检测、一致性检查、追读力分析全覆盖
- **RAG 记忆增强** - 三重记忆架构，自动检索设定、追踪伏笔、更新世界状态
- **创意约束系统** - 三轴混搭、反套路触发器、镜像对抗防重复
- **自动节奏控制** - S1-S5五级节奏评级，卷级节奏曲线分析
- **阶段总结** - 每10章/50章/每卷自动总结，记录剧情进展和伏笔状态

## 快速开始

### 前置条件

- 使用 Trae IDE 或支持 Skills 的 AI 编程助手

### 安装方式

#### 方式1：直接复制（推荐）

将 `skill/` 目录复制到你项目的 `.trae/skills/` 目录下：

```bash
cp -r skill/* /path/to/your/project/.trae/skills/novel-weaver/
```

Windows PowerShell：

```powershell
Copy-Item -Path "skill\*" -Destination ".trae\skills\novel-weaver\" -Recurse
```

#### 方式2：符号链接（开发模式）

创建符号链接，方便开发调试：

```bash
ln -s $(pwd)/skill /path/to/your/project/.trae/skills/novel-weaver
```

### 使用

在你的小说项目中，直接使用以下指令开始创作：

```
/nw init 开始写小说
```

AI 会引导你完成：
1. 基础信息：书名、题材、一句话简介
2. 主角设定：姓名、身份、性格、核心目标
3. 文风选择：根据题材自动推荐
4. 故事基调：轻松/严肃/热血/悲壮

## 指令速查

| 指令 | 说明 |
|------|------|
| `/nw init` | 开始写小说 |
| `/nw write` | 写/续写章节 |
| `/nw review` | 审查质量 |
| `/nw memory` | 查看/管理设定 |
| `/nw plan` | 生成大纲 |
| `/nw style` | 切换文风 |
| `/nw help` | 帮助信息 |

完整指令体系详见 [SKILL.md](skill/SKILL.md)

## 项目结构

```
.
├── skill/                  # 技能核心（安装到 .trae/skills/）
│   ├── SKILL.md            # 主技能文件
│   ├── references/         # 参考文档（11个）
│   ├── styles/             # 文风库（22位作者）
│   ├── templates/          # 模板文件（13个）
│   └── scripts/            # 脚本工具（5个）
├── docs/                   # 项目文档
│   ├── CHANGELOG.md        # 版本历史
│   └── CONTRIBUTING.md     # 贡献指南
├── LICENSE                 # MIT 许可证
└── README.md               # 项目说明
```

## 文风库

内置 22 位知名网文作者文风，按流派分类：

| 流派 | 代表作者 |
|------|---------|
| 搞笑幽默流 | 弈青峰、会说话的肘子、三天两觉、卖报小郎君 |
| 热血升级流 | 天蚕土豆、唐家三少、我吃西红柿、辰东、滚开 |
| 细腻文青流 | 猫腻、烽火戏诸侯、愤怒的香蕉、耳根 |
| 严谨设定流 | 爱潜水的乌贼、忘语、言归正传 |
| 特色领域流 | 蝴蝶蓝、天下霸唱、月关、萧鼎 |
| 多神话热血流 | 三九音域 |
| 悬疑推理流 | 杀虫队队员 |

详细文风库见 [skill/styles/author-styles.md](skill/styles/author-styles.md)

## 版本历史

| 版本 | 日期 | 更新内容 |
|------|------|---------|
| 1.0.0 | 2026-04 | 初始版本 |
| 1.1.0 | 2026-04 | RAG 检索增强 |
| 1.2.0 | 2026-04 | 指令精简 - 三级指令体系 |
| 1.3.0 | 2026-05 | 结构优化 - 消除重复、文风库分类 |

完整更新记录见 [CHANGELOG](docs/CHANGELOG.md)

## 贡献指南

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/amazing-feature`)
3. 提交变更 (`git commit -m 'Add amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 创建 Pull Request

详细贡献指南请参阅 [CONTRIBUTING.md](docs/CONTRIBUTING.md)

## 许可证

本项目基于 [MIT License](LICENSE) 开源。

## Star History

如果你觉得这个项目有帮助，请给一个 Star！
