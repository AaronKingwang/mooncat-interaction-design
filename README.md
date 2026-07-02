# mooncat-interaction-design

给 B端产品做交互设计时，经常会有这种感觉：方案画出来了，但说不上哪里别扭；评审时只会说「这里不太好用」，却给不出具体改法。

这个 skill 就是用来解决这个问题的。它把 B端交互设计里那些「说不清道不明」的东西，整理成一套可以直接对照、可以打分、可以落地的方法论。

适合设计管理后台、SaaS、工作台、复杂业务系统的人用。

---

## 它能解决什么问题

### 设计时没方向
拿到一个新页面需求，不知道从哪开始。这个 skill 会按「四步法」带你走：先定角色和目标，再理主线场景，然后选成熟模式，最后把复杂度藏到该在的地方。

### 评审时只会凭感觉
「这里有点怪」「用户可能会迷」这种话说了等于没说。它提供一张「七维度评审清单」，照着打过分、标过严重度，就能输出一份开发能看懂、产品能排期的改动清单。

### 方案落不了地
很多交互建议停在「要更好用」这种层面。这个 skill 要求输出的是：**流程描述、页面结构、决策表、交互规则**——产品经理拿起来就能跟研发和设计师沟通。

### 它不擅长这些

- **纯视觉/UI 风格**：配色、字体、插画、动效能评，但只评是否影响可用性，不输出视觉规范。
- **前端代码实现**：只到交互设计/原型建议，不写 HTML/Vue/React/JS。
- **C端产品**：如果明确是 C端消费产品，只给通用可用性建议，不硬套 B端效率模式。

---

## 安装

基于 [Agent Skills](https://agentskills.io) 协议，主流 agent runtime 都能装。

### 最快的方式

对你正在用的 agent 说：

```
帮我安装这个 skill：https://github.com/AaronKingwang/mooncat-interaction-design
```

或者用安装器：

```bash
npx skills add AaronKingwang/mooncat-interaction-design
```

### 手动安装

| Runtime | 放到这个目录 |
|---|---|
| Claude Code | `~/.claude/skills/mooncat-interaction-design/` |
| Codex CLI | `~/.codex/skills/mooncat-interaction-design/` |
| Cursor | `~/.cursor/skills/mooncat-interaction-design/` |
| OpenClaw | `~/.openclaw/workspace/skills/mooncat-interaction-design/` |
| 其他 | 对应 runtime 的 `skills/` 目录 |

```bash
git clone https://github.com/AaronKingwang/mooncat-interaction-design.git <上面选的路径>
```

---

## 用法

一句话：设计时打开 `SKILL.md` 跟四步法走；评审时打开 `references/review-checklist.md` 逐条打分。

### 设计新页面

1. 跑 `SKILL.md` 里的「四步法」。
2. 查 `references/bend-scenarios.md` 里对应页面类型的要点（列表/表单/详情/仪表盘…）。
3. 给出至少两个候选方案，标明推荐项，并说明依据。
4. 最后用 `SKILL.md` 的「通用原则清单」自查一遍。

### 评审已有方案

1. 先确认业务上下文：谁用、什么岗位、什么频率、要达成什么、有什么约束。
2. 读 `references/review-checklist.md`，按七维度打分。
3. 输出问题清单：每条含严重度、位置、问题、参考原则、改法。
4. 给总分和 Top 3 必改项，避免一次抛出几十条让人无从下手。

### 你可以这样激活它

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
    ├── about-face.md                 # 目标导向/姿态/去杂物/心理模型/撤销/流
    ├── designing-interfaces.md       # 导航/表格/表单/复杂数据 模式库
    ├── simple-and-usable.md          # 删除·组织·隐藏·转移 四策略
    ├── dont-make-me-think.md         # 可用性法则/扫读/文案/可用性自测
    ├── bend-scenarios.md             # B端场景速查：列表/表单/详情/仪表盘/批量/权限/边界态
    └── review-checklist.md           # 评审七维度打分 + 问题清单模板
```

---

## 参考资料

这个 skill 里的方法论框架、B端场景落地、评审打分体系和模板由 MoonCat 原创整理。下面的书目是思想参考方向，不是原文摘录。

> 需要严格溯源的话，请回到原书核对。提及书名/作者只表示「参考方向」，不代表做法逐条出自书中。

| 书目 | 参考的核心思想 |
|---|---|
| 《About Face 4：交互设计精髓》Alan Cooper | 为用户的目标而设计，消灭操作杂物(excise) |
| 《Web界面设计》Jenifer Tidwell | 不要发明轮子，复用成熟界面模式 |
| 《简约至上：交互式设计四策略》Giles Colborne | 简单来自合理分配复杂度：删除/组织/隐藏/转移 |
| 《点石成金》Steve Krug | 别让我思考（Don't Make Me Think） |

---

> © MoonCat · 原创整理，转载或二次分发请保留署名。
