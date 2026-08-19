# Learn with Codex · 私人学习搭子

一个面向"学习任何知识"的通用导师型 skill。

## 这是什么

一个可移植的 `SKILL.md` 工作流包，让 AI 成为你的私人学习搭子（Codex）。
默认扮演 **导师 + 项目教练**：中文主讲，温柔鼓励，专业幽默；不只解释概念，还会诊断起点、制定计划、组织项目化练习、检查掌握度，并在你没给资料时主动补官方文档与权威材料，把关键学习产出落盘到 Markdown 文件。

> 把 AI 从"会回答问题"推进成"能带你真的学会"的学习搭子。

## 核心特性

- 默认角色：`导师 + 项目教练`（Codex）
- 默认方法：`项目驱动学习 + Mastery Learning`
- 默认产出：学习计划、学习笔记、课后复盘、项目任务书、掌握度检查、错题/卡点记录
- 默认行为：把关键学习产出写入当前工作目录下的 Markdown 文件
- 默认来源策略：优先官方文档、原始资料、经典教材、权威机构材料，并区分事实依据与建议判断
- 默认项目化方式：
  - 编程主题：最小 demo、微项目、调试任务、小型任务书
  - 非编程主题：研究短报告、演讲提纲、案例分析、知识地图、读书笔记、复盘文档

## 目录结构

```text
Learn_with_codex/
├── SKILL.md                  # 主工作流
├── README.md                 # 本说明
├── LICENSE                   # MIT
├── agents/
│   └── openai.yaml           # Codex / OpenAI Skills 接口
├── references/
│   ├── mastery-rubric.md     # 掌握度 5 级评估标准
│   ├── project-patterns.md   # 项目化学习模式
│   ├── source-strategy.md    # 资料来源策略
│   └── teaching-playbook.md  # 导师式教学动作手册
└── assets/
    ├── learning-plan-template.md       # 学习计划模板
    ├── study-notes-template.md         # 学习笔记模板
    ├── session-review-template.md      # 单次复盘模板
    ├── project-brief-template.md       # 项目任务书模板
    ├── mastery-check-template.md       # 掌握度检查模板
    └── mistakes-log-template.md        # 错题/卡点记录模板
```

## 怎么用

推荐在一个干净的学习目录里调用，产出会自动落盘到 `study/` 子目录：

```bash
mkdir -p learn-rust && cd learn-rust
```

然后在对话里：

```text
用 $Learn_with_codex 帮我学 Rust 的所有权。
我有 Python 基础，没碰过内存管理。
请给我一个 2 周学习计划，并设计一个小项目任务书。
```

## 适用主题

不限于编程。适用于：

- 编程与软件工程
- 数学与统计
- 经济学与金融基础
- 英语和其他语言学习
- 历史、社会科学、人文阅读
- 写作、演讲、表达训练
- AI / LLM / 数据相关主题

## 想再改

最常见的个人化修改点：

- 改默认语气与输出语言 → `SKILL.md` 的 `Tone And Style`
- 改项目风格 → `references/project-patterns.md`
- 改资料策略 → `references/source-strategy.md`
- 改掌握度检查方式 → `references/mastery-rubric.md`

## 兼容性

- **OpenAI / Codex / ChatGPT Skills**：原生目标形态
- **Claude Code**：可直接作为 Skill 使用
- **WorkBuddy**：放在 `~/.workbuddy/skills/` 下即可被识别为用户级 skill
- **OpenCode**：建议作为 command 适配

## License

MIT — 见 [LICENSE](./LICENSE)。
