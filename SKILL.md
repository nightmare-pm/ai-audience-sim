---
name: 'ai-audience-sim'
display_name: 'AI 观众模拟'
display_name_en: 'AI Audience Simulation'
description: 'This skill should be used when a user wants to test or validate content (short video, article, product page, ad, landing page) BEFORE publishing by simulating how real audience members behave. It applies a 5W scene-analysis framework (Who / Where / When / How / What) plus AI role-play simulation to predict who swipes away vs who stays, replacing meeting-room guesswork with low-cost pre-flight testing. Trigger when users mention "simulate my audience", "test this content before launch", "演/模拟用户", "5W 场景分析", "发布前测试内容", "观众/读者画像", "谁会划走", or want to move beyond generic "user empathy" advice into concrete, testable simulations.'
description_zh: '用 5W 场景分析 + AI 模拟，发布前低成本试错：让 AI 把你的观众演出来，看谁划走、谁停留。'
description_en: 'Pre-flight test your content: let AI role-play your audience with a 5W scene framework and predict who swipes away vs stays.'
category: 'writing'
version: '1.0.0'
author: '队友噩梦'
agent_created: true
---

# AI Audience Simulation (5W + 场景模拟)

## Overview

Most content fails not because it is badly made, but because its creator "brainstormed the user" — sitting at a desk imagining what people want, while the real user is on a subway, muted, thumb scrolling, deciding in 0.5 seconds. This skill replaces that guesswork with a repeatable method: hand an AI five persona questions, let it role-play many concrete viewers in the *real* scenario where they meet your content, and read out who swipes away and who stays — before you ever publish.

The differentiator this skill encodes: the internet is full of "think about your user" advice, but almost none teaches *how to actually test the assumption instead of guessing*. This skill is the "test it with AI" step. It is the product-manager's pre-flight discipline (5W scene analysis + AI simulation), distilled for any creator or PM.

## When To Use

- The user has a draft video script, article, product page, or ad and wants to know "will this land?" before publishing.
- The user says "simulate my readers / viewers", "演出来给用户看", "帮我测一下这条内容", "谁会划走谁会停留".
- The user wants an audience persona / reader profile built from a real scenario, not an abstract avatar.
- The user is iterating on hook, cover, or opening and wants to know which persona it loses.

## Core Principle (read first)

**Simulation is a hypothesis, not truth.** AI simulation estimates behavior; backend analytics (完播率 / 逐秒流失曲线 / 转粉来源 / 粉丝画像) is the calibration reality. Always close the loop: simulate → publish → read backend data → recalibrate the next simulation. Never present simulation as a guarantee.

**Distinguish metric types before concluding.** On Douyin/public platforms, ▶ = 播放量 (views), ❤ = 点赞 (likes), 💬 = 评论. Mixing them up inverts every diagnosis. State which metric any cited number is before reasoning.

## Workflow

### Step 1 — Identify the "product" and the "user"

Clarify two substitutions before anything else:
- **Product** = the single piece of content being tested (one video / one article / one page), or the whole account if testing positioning.
- **User** = the person who *scrolls past* this content — NOT the follower the creator imagines. The imagined fan is the bias this skill exists to defeat.

If the user has not specified a target work, ask which draft/script to test, or request them to paste it.

### Step 2 — Build 1–3 concrete personas (never "everyone")

Reject the "target everyone" trap. Generate 1–3 specific personas, each with: age / role / state-of-mind / the specific pain that brings them to this topic. Personas must be *situated* (in a constrained environment), not abstract avatars. Use `references/framework.md` §Persona for the template and examples.

### Step 3 — Run the 5W scene还原 (Who / Where / When / How / What)

For each persona, answer the five questions that define the *real* encounter with the content:
- **Who** — concrete persona (from Step 2).
- **Where** — physical place (subway, bed, office toilet break).
- **When** — moment (commute, pre-sleep, between meetings).
- **How** — device state: muted? single-hand scroll? small screen? weak network? 0.5s swipe?
- **What** — what they subconsciously want in that moment (reassurance / a shortcut / to not feel stupid / entertainment).

This is the "How" dimension that justifies design choices like big-type covers and high-contrast text: the user is muted + fast-scrolling + small-screen, so the conclusion must be readable in 0.5s.

### Step 4 — Simulate with AI (the differentiator)

Do NOT just "think about the user". Run the simulation prompts from `references/prompts.md` (P1 persona + scenario, P2 edge-case穷举, P3 cover/hook校验, P4 data回看). For each persona, have the AI role-play the internal monologue at 4 moments of contact: **(a) sees cover, (b) first 3 seconds, (c) hears the core claim, (d) reaches the CTA** — and declare at each: stays or swipes, and why. Generate enough simulated individuals (the method's signature is "simulate 100", but 5–10 well-chosen is sufficient for a draft; scale up for high-stakes launches).

### Step 5 — Synthesize gaps → concrete fixes

Aggregate the monologues into:
- **Who stays / who swipes** (by persona and by contact moment).
- **What the script did NOT catch** — the unspoken thought each persona had that the content failed to answer.
- **Per-segment fix**: which paragraph to change, based on which persona's psychology, with a phrasing direction (do NOT auto-rewrite the author's voice unless asked).

Output the report using `assets/simulation_report.md` as the template.

### Step 6 — Calibrate loop (post-publish)

After the content is live, ask the user for backend data (完播率, 3秒留存, 转粉来源, 粉丝画像). Re-run P4 to reverse-engineer where real users actually dropped, explicitly separating views from interactions, and feed the correction into the next simulation. This is what makes the simulation get sharper over time.

## Persona Psychology Triggers To Watch

When simulating, these three archetypes cover most content audiences — adapt, do not invent blindly:
- **Anxious beginner** — tried, failed, suspects "user empathy" is mysticism; wants a low-threshold, copyable method.
- **Method hoarder** — has consumed 5 "viral" courses; filters "another user-thinking lesson" as "old news"; what they actually lack is *how to actually test*, not more theory.
- **Casual passerby** — not a creator at all;刷到 by cover only; bounces the instant they hear "make a video". Decides the first-3-seconds生死.

## Red Lines (preserve creator trust)

- **Do not mythologize AI.** AI is a simulation tool, not a viral-machine. Never claim "guaranteed hit / 爆款".
- **Simulation ≠ reality.** Always pair output with "verify via backend data after publishing".
- **No clickbait / anxiety-manufacturing.** The method挖 needs is fine; the copy that lands must be truthful and compliant with the creator's house style.
- **Respect the author's voice.** Suggest phrasing directions; do not silently rewrite their script into a different persona.

## Resources

- `references/framework.md` — full 5W framework, persona template, worked examples, edge-case catalog.
- `references/prompts.md` — the reusable P1–P4 prompt library (copy-paste into any LLM).
- `assets/simulation_report.md` — output template for the simulation report.
