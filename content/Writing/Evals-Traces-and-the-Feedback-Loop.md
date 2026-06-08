---
title: Evals, Traces, and the Feedback Loop
type: essay
author: Nihit Nirmal
---

The feedback loop beats the one-shot — build the loose version, instrument it, and let it get better over time.

![[evals-traces-loop.jpg]]

## Why people stop

A friend messaged me last week. He'd been wiring a few skills and prompts into his work, got excited — and then, within a couple of weeks, when they didn't quite work, he quietly stopped. They weren't doing what he wanted, and fixing them felt like more work than just doing the task himself. It's not really an exception; it happens a lot.

The reflex, when a skill or prompt underperforms, is to fix it right then. So you patch it — it works a couple of times, and then it breaks again. Under that reflex is a question that never really stops: do you fix it now, or later?

## What to do instead

As a product manager this felt obvious to me — but I rarely see anyone actually do it. The fix isn't to keep patching. It's to maintain three things:

1. **Versions** of your prompts and skills.
2. A **golden set** — the runs that came out right, with the answer you actually wanted.
3. A **traces file** — when a run slips, the exact input and what went wrong.

A slip doesn't earn a place in the golden set until I've fixed it. For the skills that matter, I keep all three together.

To make it concrete: my pre-flight skill runs at the start of every work session. Its job is to read my project file, work out where I've actually gotten to, find the gap to the goal, and turn that into a launch card — a GTD-style read on what to do in the next block. One morning it took the single line I'd typed and ran with it, without reading the state it's built to read. The skill I made to give me clarity had skipped the input that clarity comes from.

> **Before — what it handed me** *(echoed my line, never read the project)*
>
> Task — "publish the post." *(my own words, handed back)*\
> Goal — post is live.\
> Done — post is live.

> **After — the fixed run** *(read the draft, found the gap, bounded the work)*
>
> Route — the post's own draft file.\
> Current → Goal — draft at v8 → published.\
> Delta — three edits stand between v8 and live.\
> Task (this session) — (1) the voice pass; (2) the real dashboard numbers; (3) the last edit.\
> Done — those three edits committed *(not "published" — that's a session or two out)*.\
> Friction — clear; the take is locked, this is finishing.\
> If–then — if I start reopening the structure, I hold v8 and ship the three edits.

The move is small: fix it in the moment so you keep going, but capture the trace so the fix isn't lost. In a product team, the instinct to **instrument** — to check whether the thing actually works — is everywhere. Building your own skills, alone, I see almost none of it.

None of this takes more than five minutes in the moment. But do it for a week or two on a skill you lean on, and you end up with twenty or thirty real cases — where it went wrong, and what right looked like. When I finally sit down to fix it, I'm not guessing at what's broken. **I have the list** — what to run it on, and what the ideal output should look like.

I've built skills that saved me real time, and skills that quietly did the wrong thing for days before I caught it.

## Feedback loop and compounding

Two things started to matter to me early on. The first is the **feedback loop** — building with LLMs gives you a very fast one, so every run either makes the skill better or leaves behind the thing that will: the trace of what went wrong, the corrected case once I've fixed it. The second is **compounding** — once you're capturing all of it, you can watch it move: how fast you're fixing things, how many skills are graduating, how often they come out right.

I keep a weekly scorecard for this — not per skill, but counts: how many have **graduated** (graduated means it holds **96% correct or better**), how many are **in progress**, and how many are still **in view**. For the graduated ones, I also track the average number of turns it took to get them there.

---

**Weekly skill scorecard** *(illustrative)*

| Status | Count | Avg turns to graduate |
|--------|-------|----------------------|
| Graduated (≥96%) | 4 | ~3 |
| In progress | 5 | — |
| In view | 6 | — |

---

The five-minute fix is the micro move — it gets me through the session. The scorecard is the macro one: how I know, over weeks, whether I'm actually moving forward or just changing things.

There's a third thing I'm still working out — whether all of this actually saves me time, or makes me money. For a knowledge worker that's what finally counts, but it's harder to measure honestly, so I'll leave it for another post.

If you're building your own skills this way — keeping the traces, watching whether they actually get better — I'd be glad to compare notes.
