# ai-audience-sim

> Stop guessing your audience. Let AI role-play them.

**ai-audience-sim** is a reusable [WorkBuddy](https://www.workbuddy.cn) skill that turns "brainstorming your users" into a low-cost **pre-flight test** for content. Instead of imagining what people want at your desk, you hand an LLM five persona questions and let it simulate many real viewers in the exact scenario where they meet your content — then read out **who swipes away and who stays**, *before you ever publish*.

## The core idea

> Give the AI five questions — **Who / Where they scroll / When / How they scroll / What they subconsciously want** — then have it simulate many people browsing your content in its real scenario, and read out who swipes away and who stays.

Most content fails not because it is made badly, but because the creator "brainstorms the user" — adding filters to themselves and ignoring that the real user is on a subway, muted, thumb-scrolling, deciding in 0.5 seconds. This skill replaces that guesswork with a repeatable method distilled from product-management practice.

Plenty of advice online says "think about your user." Almost none teaches *how to actually test the assumption instead of guessing*. This skill is that missing step.

## Install

This skill runs inside WorkBuddy. Place the folder under your user-level skills directory:

```
~/.workbuddy/skills/ai-audience-sim/
```

Or install it via the WorkBuddy skill marketplace / `skill-creator`.

## Workflow (6 steps)

1. **Name the product and the user** — product = one piece of content; user = the person who scrolls past it (not the fan you imagine).
2. **Build 1–3 concrete personas** — reject "everyone".
3. **Run the 5W scene analysis** (Who / Where / When / How / What they subconsciously want).
4. **Simulate with AI** — at 4 contact moments (cover / first 3s / core claim / CTA), role-play the inner monologue and decide stay-or-swipe.
5. **Synthesize gaps → fix content** — who stays, who leaves, which unspoken thought you missed, and per-segment phrasing direction.
6. **Calibration loop** — after publishing, feed backend analytics (completion rate, drop-off curve, follower source, audience profile) back in; the next simulation gets sharper.

## Structure

| File | Purpose |
|---|---|
| `SKILL.md` | Core workflow and trigger conditions |
| `references/framework.md` | Full 5W framework, persona template, edge-case catalog, calibration loop |
| `references/prompts.md` | Copy-paste P1–P4 prompt library (topic / edge / cover / data review) |
| `assets/simulation_report.md` | Output template for the simulation report |

## Red lines (creator trust)

- **Don't mythologize AI** — it's a simulation tool, not a virality machine. Never promise "guaranteed hit".
- **Simulation ≠ reality** — every conclusion must be re-checked against platform backend data before decisions.
- **No clickbait, no anxiety-manufacturing** — respect the author's voice; suggest directions, don't rewrite.

## License

MIT

---

## 中文说明

# ai-audience-sim

> 用 5W 场景分析 + AI 模拟，把"脑补用户"换成"演给用户看"——发布前低成本试错。

大多数内容失败，不是因为做得差，而是创作者在书桌前"脑补"了用户：自动给自己加滤镜，忽略了真实用户正躺在地铁上、静音、拇指快滑、0.5 秒就划走。本技能把产品经理的"发布前用户模拟"纪律蒸馏成可复用工作流：

**给 AI 五个问题（谁 / 在哪刷 / 什么时候 / 怎么刷 / 他潜意识要什么）→ 让 AI 模拟很多人在你内容的真实场景里刷 → 读出谁划走、谁停留。**

网上教"做用户思维"的到处都是，但几乎没人教你怎么真的去**试**——本技能就是这一步。

## 安装

把本目录放到 WorkBuddy 的用户级 skills 目录后即可被自动识别：

```
~/.workbuddy/skills/ai-audience-sim/
```

或直接用 WorkBuddy 的 `skill-creator` / 市场安装。

## 工作流（6 步）

1. **认产品认用户** —— 产品 = 单条内容；用户 = 刷到你内容的人（不是你以为的粉丝）。
2. **建 1–3 个具体 Persona** —— 拒绝"所有人"。
3. **跑 5W 场景还原** —— Who / Where / When / How / What（潜意识要什么）。
4. **用 AI 模拟** —— 在 4 个接触点（封面 / 前 3 秒 / 核心观点 / CTA）演内心独白，判定停留或划走。
5. **汇总缺口 → 改内容** —— 谁留谁走、没接住哪个念头、按段给话术方向。
6. **校准闭环** —— 发布后用后台数据（完播率 / 逐秒流失 / 转粉来源 / 粉丝画像）回灌，下一轮更准。

## 结构

| 文件 | 作用 |
|---|---|
| `SKILL.md` | 核心工作流与触发条件 |
| `references/framework.md` | 完整 5W 框架、Persona 模板、边缘场景清单、校准闭环 |
| `references/prompts.md` | 可抄的 P1–P4 提示词库（选题 / 边界 / 封面 / 数据回看） |
| `assets/simulation_report.md` | 观众模拟报告输出模板 |

## 红线（守住创作者信任）

- 不神话 AI：AI 是模拟工具，不是爆款机器，绝不承诺"必火"。
- 模拟 ≠ 真实：任何结论都需用平台后台数据回看校准后再决策。
- 不标题党、不制造焦虑；尊重作者原有文风，只给方向不替写。

## License

MIT
