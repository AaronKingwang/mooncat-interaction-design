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

### 「感觉不对，但说不上来」

B端页面一旦复杂起来，很难判断某个设计到底好不好。这个 skill 提供一张**七维度评审清单**（目标契合、效率、清晰、模式一致、复杂度分配、反馈容错、边界状态），让你能逐条检查、打分，把主观感受变成可讨论的问题清单。

### 「只提问题，不给方案」

很多评审停在「这里不合理」就结束了。这个 skill 要求：每个问题必须跟一条**具体可落地的原型/交互优化方案**，并且优先给出 2–3 个候选，说明适用条件和推荐项，供你选完再细化。

### 「设计时没方向，只会堆功能」

拿到一个新页面，不知道从哪开始。这个 skill 用**四步法**带你走：先定角色和目标 → 再理主线场景 → 然后选成熟模式 → 最后把复杂度藏到该在的地方。避免一上来就画界面、堆字段。

### 「评审不看业务上下文，瞎给建议」

同一个交互，卖给小商家的 SaaS 和给大型机构用的调解平台，结论可能完全不同。这个 skill 要求：评审或设计方案前，先确认**谁用、什么岗位、什么频率、要达成什么、有什么约束**，信息不足时主动追问，不凭假设下结论。

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

| 约束 | 含义 |
|---|---|
| **上下文先于判断** | 评审前先确认业务角色、频率、目标、约束；不臆断 |
| **给方案，不给清单** | 最终交付物是可选择的**具体原型/交互方案**，含优劣与推荐，不是抽象问题列表 |
| **面向产品经理，不写代码** | 用流程描述、线框说明、决策表、交互规则表达；不输出 HTML/Vue/React/JS |
| **少而准** | 评审聚焦 Top 必改项，不用长清单淹没用户 |

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
