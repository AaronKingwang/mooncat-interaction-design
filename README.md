# mooncat-interaction-design

> **B端产品交互设计通用 Skill** —— 参考四本交互设计经典的思想方向，结合 B端实践整理成一套可对照、可执行、可评分的 B端（管理后台 / SaaS / 工作台）交互设计工作法。
>
> **作者**：MoonCat · **版本**：v1.0

---

## Skill 能解决什么问题

这个 skill 帮助产品经理、交互设计师或任何正在设计 / 评审 B端界面的人，把「好不好用」从主观感觉变成可执行的判断和可落地的方案。

### 适用场景

- **设计新页面/交互**：列表页、表单页、详情页、仪表盘、工作流、筛选、批量操作、权限、引导、空状态、反馈。
- **索要设计输入**：交互原则、模式参考、命名与布局建议、组件选型。
- **评审已有方案**：对原型/设计稿/HTML/交互说明做「交互质量评审」，输出问题清单与改进建议。
- **讨论可用性问题**：「这个交互合不合理」「怎么设计更好用」「为什么用户会卡住」「这里该怎么引导」。

### 核心解决的三类问题

| 问题 | Skill 提供的帮助 |
|---|---|
| 设计时没有头绪 | 用「四步法」定角色、主线、模式、复杂度分配 |
| 评审时只会说「感觉不对」 | 用「七维度打分清单」结构化找问题、分严重度 |
| 方案难以落地 | 输出流程描述、线框说明、决策表、交互规则，而不是抽象建议 |

### 不解决什么

- **纯视觉/UI 风格**（配色、字体、插画、动效）：只判断它是否影响交互可用性，不输出视觉规范。
- **前端代码实现**：只到交互设计/原型建议层面，不生成 HTML/Vue/React/JS 代码。
- **C端/消费端产品**：若明确是 C端且与 B端效率无关，仅提供通用可用性建议，不强行套用 B端模式。

---

## 安装

本 skill 基于开放的 [Agent Skills](https://agentskills.io) 协议，可在任何 skills-compatible 的 AI agent runtime 中运行。

### 方式一：一句话安装（推荐）

打开你正在用的 agent（Claude Code、Codex、Cursor、OpenClaw 等），告诉它：

```
帮我安装这个 skill：https://github.com/AaronKingwang/mooncat-interaction-design
```

或使用通用 CLI 安装器 [`vercel-labs/skills`](https://github.com/vercel-labs/skills)：

```bash
npx skills add AaronKingwang/mooncat-interaction-design
```

### 方式二：手动安装

| Runtime | 安装路径 |
|---|---|
| Claude Code | `~/.claude/skills/mooncat-interaction-design/` |
| Codex CLI | `~/.codex/skills/mooncat-interaction-design/` |
| Cursor | `~/.cursor/skills/mooncat-interaction-design/` |
| OpenClaw | `~/.openclaw/workspace/skills/mooncat-interaction-design/` |
| 其他 runtime | 对应 runtime 的 `skills/` 目录 |

```bash
git clone https://github.com/AaronKingwang/mooncat-interaction-design.git <上面对应路径>
```

---

## 用法

### 姿势 A：设计模式

1. 跑 `SKILL.md` 中的「四步法」：定角色与目标 → 理清主线场景 → 选模式排布局 → 分配复杂度去杂物。
2. 针对当前页面类型，查 `references/bend-scenarios.md` 对应场景要点。
3. 输出设计建议时，**给方案 + 给依据**，列出至少 2 个候选 + 推荐项。
4. 交付前用 `SKILL.md` 第四节「通用原则清单」自查一遍。

### 姿势 B：评审模式

1. 先确认业务上下文：谁用、什么岗位、什么频率、要达成什么、有什么约束。
2. 读 `references/review-checklist.md` 的七维度评分框架。
3. 逐维度检查目标物（原型 HTML / 设计稿 / 交互说明）。
4. 输出分级问题清单 + 总分 + Top3 必改项。

### 高频激活语

- 「帮我设计一个 B端……」
- 「评审一下这个交互」
- 「这个表单/列表/详情页怎么设计」
- 「为什么用户在这里会迷路/卡住」
- 「怎么减少操作步骤」

---

## 结构

```
mooncat-interaction-design/
├── SKILL.md                          # 主文档：方法论、四步法、四策略、通用原则、两种姿势
└── references/
    ├── about-face.md                 # 目标导向/姿态/去杂物/心理模型/撤销/流（参考 About Face）
    ├── designing-interfaces.md       # 导航/表格/表单/复杂数据 模式库（参考 Web界面设计）
    ├── simple-and-usable.md          # 删除·组织·隐藏·转移 四策略（参考 简约至上）
    ├── dont-make-me-think.md         # 可用性法则/扫读/文案/可用性自测（参考 点石成金）
    ├── bend-scenarios.md             # B端场景速查：列表/表单/详情/仪表盘/批量/权限/边界态
    └── review-checklist.md           # 评审七维度打分 + 问题清单模板
```

---

## 参数资料 / 参考书目

本 skill 的方法论框架、B端场景落地、评审打分体系与模板由 MoonCat 原创整理；所参考的交互设计思想方向归各原书作者所有。

> **来源声明**：本 skill 内容是参考下列经典中广为人知的核心思想、并结合 B端实践推演整理而成，**非对原书逐页精读后的原文提炼**。提及书名/作者处均表「参考方向」，需严格溯源请回到原书核对。

| 参考来源 | 参考的核心思想方向（概括，非原文） |
|---|---|
| 《About Face 4：交互设计精髓》Alan Cooper | 为用户的**目标**而设计，消灭操作杂物(excise) |
| 《Web界面设计》Jenifer Tidwell | 不要发明轮子，**复用成熟界面模式** |
| 《简约至上：交互式设计四策略》Giles Colborne | 简单来自**合理分配复杂度**（删除/组织/隐藏/转移） |
| 《点石成金》Steve Krug | **别让我思考**（Don't Make Me Think） |

---

> © MoonCat · 本 skill 为原创整理，转载或二次分发请保留署名。
