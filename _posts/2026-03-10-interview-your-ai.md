---
layout: post
title: "Start Building an Interview Kit for Your AI — Today"
date: 2026-03-10
---

The model your team is using right now — was it chosen through rigorous evaluation? Or because it's the newest? Or simply because… it's what you've always used?

This is not a trivial question. AI is no longer just a "tool" — it's your **digital employee**. Writing code, running analyses, processing documents, handling customer responses — it does all of that. It has capability boundaries, domain strengths, and varying cost profiles. You wouldn't hire a human without an interview, and you wouldn't assign one person to every task regardless of fit.

Yet that's exactly how most teams treat their AI.

## You're Making One of Two Mistakes

In late 2025, four companies released their most powerful models within just 25 days: xAI's Grok 4.1 (Nov 17), Google's Gemini 3 (Nov 18), Anthropic's Claude Opus 4.5 (Nov 24), and OpenAI's GPT-5.2 (Dec 11) [1]. Entering 2026, the pace accelerated further — Claude Sonnet 5, DeepSeek V4, and Gemini 3.1 Pro all appeared in February, nearly simultaneously [2]. A year ago, we measured release cycles in quarters. Now it's months, sometimes weeks.

Facing this pace, teams tend to fall into one of two symmetrical errors:

**Error one: Chasing the new.** Every time a new model drops, the team switches over, spends a week or two re-tuning prompts, only to discover — maybe some tasks improved, but others regressed. Time wasted, workflows disrupted, and the only "evaluation" was a few people's vague feelings.

**Error two: Standing still.** The team defaults to one model and forgets the world has moved on. Simple tasks like summarization and formatting burn through a flagship model at $15 per million output tokens [3], when a $0.08 lightweight model would perform just as well. Meanwhile, critical tasks requiring strong reasoning are being dragged down by an underpowered legacy model.

These two errors look opposite, but they share the same root cause: **you have no evaluation standard of your own.**

## Why Current Evaluation Methods Fall Short

**Official benchmarks weren't built for you.** MMLU, HumanEval, MATH — these leaderboards measure general capability, not your specific use case. And the benchmarks themselves are breaking down: research shows that of 445 mainstream LLM benchmarks, only 16% use rigorous scientific methods to compare model performance; roughly half claim to measure abstract concepts like "reasoning" or "harmlessness" without providing clear definitions or measurement criteria [4]. The sharper problem is Goodhart's Law: when a measure becomes a target, it ceases to be a good measure. OpenAI's own research confirms this [5]. The Chatbot Arena leaderboard controversy is a case in point — companies like Meta, OpenAI, and Google privately tested numerous model variants and only published the best results, turning the leaderboard into a target to be gamed [6].

The #1 model on the leaderboard might rank last in your domain.

**"Using it for a while and going by feel" costs too much.** When hiring humans, we used to rely on this approach too — bring someone on, wait six months, form a vague impression. But AI's iteration cycle has compressed to weeks. By the time you've developed a "feel" for the current model, the next version has already arrived. Teams don't have time for six-month probation-style slow evaluation.

And in the AI era, efficiency gaps are dramatically amplified. A wrong model decision isn't just "not ideal" — it means your team spends more time blindly tuning prompts. The same work that another team finishes in an hour takes yours a day. Model capabilities are growing exponentially. That gap only gets wider.

## Interview Your AI: Not a New Idea

When hiring humans, we long ago evolved from "going by feel" to structured processes. Research shows that structured interviews achieve a predictive validity correlation of 0.43, nearly double that of unstructured interviews at 0.24 [7]. Put another way, **one structured interview predicts job performance as accurately as three to four unstructured interviews**.

This logic transfers directly to AI evaluation. You don't need to rely on someone else's leaderboard (equivalent to hiring based solely on a resume's GPA), nor do you need six months of slow "feeling it out" — you need a standardized set of your own test questions.

And AI is far easier to interview than humans. No nerves, no off days, fully repeatable, results directly quantifiable.

### Four Dimensions to Build Your Evaluation Matrix

The core of interviewing isn't "find the smartest person" — it's "find the best fit for this role." Evaluating AI works the same way. I recommend designing your test suite across four dimensions:

**Dimension 1: Difficulty Gradient.** Cheaper models may perform just as well on simple tasks — no need to use a sledgehammer to crack a nut. But you also need to know where the ceiling is. Build a ladder from summary generation to multi-document comparative analysis to system architecture design from ambiguous requirements, and see where each model starts to fall apart.

**Dimension 2: Prompt Ambiguity.** Take the same task and test it twice: once with precise instructions, once with vague ones. Precise: "Write a Python function that takes a list and returns a deduplicated, sorted result." Ambiguous: "Help me clean up this data, there are duplicates." In real work, requirements are rarely spelled out. A model that handles ambiguity is worth far more in practice. Good candidates don't need hand-holding — good models shouldn't either.

**Dimension 3: Domain Coverage.** Don't test one domain and call it a day. Model capabilities are unevenly distributed — even top models achieve only a 26.2% success rate on real freelance coding tasks (SWE-Lancer benchmark) [8], far below what benchmarks suggest. Code, writing, data analysis, reasoning, translation — pick your team's top three to five.

**Dimension 4: Collaboration Mode.** Strong single-shot answers don't guarantee context consistency across multi-turn conversations, let alone autonomous task completion as an agent. Try this: have the model explain a bug in one shot, then debug iteratively across multiple turns, then run tests, locate the issue, and submit a fix as an autonomous agent. Three modes, three very different capabilities.

The cross-product of these four dimensions reveals true capability distribution. You don't need to cover every combination — start with your team's three to five most frequent scenarios, cover all four dimensions for each, and you're already an order of magnitude better than "going by feel."

![Four-dimensional evaluation matrix: Capability distribution comparison of two models across difficulty gradient, prompt ambiguity, domain coverage, and collaboration mode](/assets/images/interview-your-ai-matrix.png)

## After the Interview, Assign People to the Right Roles

Evaluation isn't about crowning "one best model" for everything. The real value lies in figuring out **who belongs in which seat** — just as you wouldn't assign everyone to the same job after interviews.

Simple formatting tasks → Fast, cheap model (Gemini Flash Lite, $0.08/M tokens). Critical reasoning tasks → Most capable flagship model. Creative tasks → Whichever performs best under ambiguous instructions. Multi-step autonomous tasks → Highest scorer in collaboration mode.

Your test suite is your assignment guide. This isn't a novel concept — enterprises already have open-source tools like Yourbench for creating custom benchmarks against their own data [9], and evaluation platforms are maturing rapidly. But tools are just means; what matters is whether you have the **awareness and habit of evaluating**.

## Start Today

You don't need a perfect evaluation framework from day one.

Start with your team's three most common tasks. Write one "interview question" for each — a precise version and an ambiguous version. Next time a new model launches, run your questions first, then decide whether to switch.

The key isn't perfection in your questions — it's that you've started.

Your team already has digital employees. The only question is — have you actually interviewed them, and have you put them in the right seats?

In the AI era, making decisions without evaluation is as dangerous as hiring without interviews.

---

## References

[1] [The AI Model Race Reaches Singularity Speed - Vertu](https://vertu.com/lifestyle/the-ai-model-race-reaches-singularity-speed/) — Four major models released within 25 days in late 2025

[2] [AI Updates Today (March 2026) - LLM Stats](https://llm-stats.com/llm-updates) — Five frontier models launched near-simultaneously in early 2026

[3] [LLM API Pricing Comparison - IntuitionLabs](https://intuitionlabs.ai/articles/ai-api-pricing-comparison-grok-gemini-openai-claude) — Claude Sonnet 4.6 output at $15/M tokens vs. Gemini Flash Lite at $0.08/M tokens

[4] [AI Benchmarks Hampered by Bad Science - The Register](https://www.theregister.com/2025/11/07/measuring_ai_models_hampered_by/) — Only 16% of 445 LLM benchmarks use rigorous scientific methods

[5] [Measuring Goodhart's Law - OpenAI](https://openai.com/index/measuring-goodharts-law/) — OpenAI's research on Goodhart's Law in AI optimization

[6] [Gaming the System: Goodhart's Law in AI Leaderboard Controversy - Collinear AI](https://blog.collinear.ai/p/gaming-the-system-goodharts-law-exemplified-in-ai-leaderboard-controversy) — How major companies gamed the Chatbot Arena leaderboard

[7] [Structured vs. Unstructured Interviews - McGill University](https://www.mcgill.ca/psychology/files/psychology/structuredinterviews.pdf) — Structured interview validity 0.43 vs. unstructured 0.24

[8] [Measuring the Performance of Our Models on Real-World Tasks - OpenAI](https://openai.com/index/gdpval/) — SWE-Lancer: Top models achieve only 26.2% on real coding tasks

[9] [Beyond Generic Benchmarks: How Yourbench Lets Enterprises Evaluate AI Models - VentureBeat](https://venturebeat.com/ai/beyond-generic-benchmarks-how-yourbench-lets-enterprises-evaluate-ai-models-against-actual-data) — Hugging Face's open-source Yourbench for custom enterprise benchmarks
