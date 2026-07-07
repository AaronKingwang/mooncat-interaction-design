# mooncat-interaction-design

> 让 B端交互设计从「感觉不对」变成「知道哪里不对、知道怎么改」。
>
> Author: **MoonCat**

设计管理后台、SaaS、工作台这类 B端系统时，最常见的困境不是画不出界面，而是：

- 方案做完了，总觉得哪里别扭，却说不上来；
- 评审时大家只说「这里不好用」「用户可能会迷」，给不出具体改法；
- 改来改去，最后变成「再加个字段、再加个按钮」，页面越来越重。

这个 skill 把 B端交互设计的方法论拆成一套可对照、可打分、可落地的流程。不改模型，只给你一套「设计时能跟着走、评审时能照着打」的外部大脑。

---

## 它解决什么问题

### 「B端页面越画越复杂，用户反而找不到主功能」

后台系统功能多、角色多、字段多，设计时很容易把「后台能展示的」全堆到界面上。结果用户进来满眼都是按钮和表格，却不知道第一步该做什么。这个 skill 用**目标导向四步法**帮你先定角色和主任务，再决定什么该露、什么该藏。

### 「表单/列表/详情页做得中规中矩，但用起来就是不顺」

控件选得没问题，布局也整齐，但用户填表单时反复切换、列表里找一行要翻很久、详情页想看关联信息要跳三四次。这个 skill 提供 B端常见场景的**模式库和自查清单**，帮你发现那些「看起来对、用起来卡」的 excise（操作杂物）。

### 「评审原型时只会说『感觉不对』，给不出改法」

产品经理、设计师、开发围在一起看原型，大家都能挑出毛病，但说完「这里不好用」「用户可能会迷」就卡住了。这个 skill 用**七维度评审框架**把「好不好用」拆成可打分的检查项，并针对问题输出 2–3 个可落地的原型优化方案。

### 「照搬 C端习惯做 B端，效率反而更低」

在 B端做渐进披露、动效引导、精简流程，结果专家用户每天要重复操作几十次，反而嫌慢。这个 skill 从前提上就区分 B端与 C端：B端用户是**高频专家用户**，效率优先于新颖，默认要的是直达、批量、记忆、少思考。

### 「不同角色看到的界面完全一样，权限问题靠报错」

操作员、审核员、管理员共用一套界面，没权限的功能点了才提示「无权限」。这个 skill 按角色梳理目标与视图，把权限差异前置到设计里，而不是靠后端拦截。

### 它不擅长这些

- **纯视觉/UI 风格**：配色、字体、插画、动效能评，但只评是否影响可用性，不输出视觉规范。
- **前端代码实现**：只到交互设计/原型建议层面，不生成 HTML/Vue/React/JS 代码。
- **C端/消费端产品**：如果明确是 C端且与 B端效率无关，只给通用可用性建议，不强行套用 B端模式。

---

## 安装

mooncat-interaction-design 基于开放的 [Agent Skills](https://agentskills.io) 协议，可在任何 skills-compatible 的 AI agent runtime 中运行。

### 方式一：一句话安装（推荐，跨 runtime）

打开你正在用的 agent（Claude Code、Codex、Cursor、OpenClaw、Hermes、CodeBuddy、Workbuddy、Gemini CLI、kimi CLI、OpenCode 等），告诉它：

```
帮我安装这个 skill：https://github.com/AaronKingwang/mooncat-interaction-design
```

或者用通用 CLI 安装器 [`vercel-labs/skills`](https://github.com/vercel-labs/skills)（支持 55+ runtime）：

```bash
npx skills add AaronKingwang/mooncat-interaction-design
```

### 方式二：手动安装

<details>
<summary>展开查看各 runtime 的 skills 目录</summary>

| Runtime | 安装路径 |
|---|---|
| Claude Code | `~/.claude/skills/mooncat-interaction-design/` |
| Codex CLI | `~/.codex/skills/mooncat-interaction-design/` |
| Cursor | `~/.cursor/skills/mooncat-interaction-design/` |
| OpenClaw | `~/.openclaw/workspace/skills/mooncat-interaction-design/` |
| 其他 runtime | clone 到对应 runtime 的 `skills/` 目录 |

</details>

```bash
git clone https://github.com/AaronKingwang/mooncat-interaction-design.git <上面对应的路径>
```

### 方式三：作为参考资料直接使用

把 `SKILL.md` 和 `references/` 的内容作为提示词喂给当前 agent，让它按流程执行即可。适合临时试用或不方便安装的场景。

---

## 两种用法

### 模式 A · 设计模式（边设计边对照）

适合：从 0 到 1 设计一个 B端页面或交互流程。

你可以这样说：

```
帮我设计一个 B端工单列表页
这个表单怎么减少填写步骤
详情页上怎么摆放操作按钮更合理
```

它会：先确认角色和主任务 → 跑四步法 → 查 `bend-scenarios.md` 对应场景 → 给出 2–3 个候选方案 + 推荐项 → 用通用原则清单自查一遍 → 输出流程描述、页面结构、交互规则（不写代码）。

### 模式 B · 评审模式（给已有方案打分）

适合：手里已有原型、设计稿、HTML 或交互说明，想知道问题在哪、先改什么。

你可以这样说：

```
评审一下这个交互
帮我看看这个原型有哪些交互问题
这个列表页为什么用户会卡住
```

它会：先确认业务上下文 → 读 `review-checklist.md` 七维度 → 逐条检查目标物 → 输出分级问题清单 + 总分 + Top 3 必改 → 针对 Top 问题给出 2–3 个可落地的原型优化方案 → 用流程/线框/决策表表达，不写代码。

---

## 输出规范：为什么你不会拿到一堆废话

这个 skill 对输出做了硬性约束，避免两种常见失败：

| 约束              | 含义                                          |
| --------------- | ------------------------------------------- |
| **上下文先于判断**     | 评审前先确认业务角色、频率、目标、约束；不臆断                     |
| **给方案，不给清单**    | 最终交付物是可选择的**具体原型/交互方案**，含优劣与推荐，不是抽象问题列表     |
| **面向产品经理，不写代码** | 用流程描述、线框说明、决策表、交互规则表达；不输出 HTML/Vue/React/JS |
| **少而准**         | 评审聚焦 Top 必改项，不用长清单淹没用户                      |

---

## 借鉴的思想

这个 skill 参考了四本交互设计经典的核心思想方向，并把它们落到 B端实践里：

| 书目 | 核心思想 | 在这个 skill 里的落点 |
|---|---|---|
| 《About Face 4：交互设计精髓》Alan Cooper | 为用户的目标而设计，消灭操作杂物(excise) | 四步法、目标契合维度、去杂物检查 |
| 《Web界面设计》Jenifer Tidwell | 不要发明轮子，复用成熟界面模式 | 模式库引用、模式一致维度 |
| 《简约至上：交互式设计四策略》Giles Colborne | 简单来自合理分配复杂度（删除/组织/隐藏/转移） | 四策略、复杂度分配维度 |
| 《点石成金》Steve Krug | 别让我思考（Don't Make Me Think） | 清晰维度、通用原则清单、少而准 |

> 注：本 skill 为 MoonCat 原创整理，方法论框架、B端场景落地、评审打分体系与模板均为原创；提及书名/作者只表示「思想参考方向」，不代表做法逐条出自书中原文，需严格溯源请回到原书核对。

---

## 目录结构

```
mooncat-interaction-design/
├── SKILL.md                          主文档：方法论、四步法、四策略、通用原则、两种姿势
├── README.md                         本文件（给人看）
└── references/
    ├── about-face.md                 目标导向/姿态/去杂物/心理模型/撤销/流
    ├── designing-interfaces.md       导航/表格/表单/复杂数据 模式库
    ├── simple-and-usable.md          删除·组织·隐藏·转移 四策略
    ├── dont-make-me-think.md         可用性法则/扫读/文案/可用性自测
    ├── bend-scenarios.md             B端场景速查：列表/表单/详情/仪表盘/批量/权限/边界态
    └── review-checklist.md           评审七维度打分 + 问题清单模板
```

---

## 环境要求

- 任意支持 Agent Skills 协议的 AI agent runtime。
- 不需要 Python、Node 或其他依赖。

---

## 一句话哲学

> **面向目标 → 复用模式 → 分配复杂度 → 让它无需思考。**

B端的复杂没法删掉，只能被放到对的地方。

---

*© Author: **MoonCat** · mooncat-interaction-design v1.0.0*
