---
title: The Work Your AI Can't See
date: 2025-12-29
published: true
tags: [ai-agents, workflows, documentation, operations]
---


There's an overlooked benefit to working with agents: in order to make working with agents work, **you're going to make work work.**

The gap that most organizations stumble over isn't technical per se. It won't be solved by more capable models, a better UI, or the next release. It's the same gap that's plagued knowledge work for decades: work that exists only in people's heads, processes that depend on the right person being in the room, documentation that's either outdated or unfindable or both.

Whether the AI models improve next month or next year, the work before us is the same. But there's some good news.

## The Six Primitives

[Nate B. Jones](https://www.youtube.com/watch?v=4Bg0Q1enwS4) frames it as six questions that every workflow needs to answer explicitly:

1. **State**  – What are the current conditions? What changed?
2. **Artifacts**  – What tangible outputs are we working with?
3. **Change Records**  – What modifications were made, and when?
4. **Checks**  – How do we validate it worked?
5. **Rollback**  – How do we revert when it doesn't?
6. **Traceability**  – Who did what, and why?

This framing resonates with my work at TightOps. A decade of work in and with (distributed team) operations, across different companies and cultures, and always finding the same fundamental failure is not the technology. It is a **legibility** issue – work that isn't readable, findable, or actionable by anyone who wasn't in the room when it happened.

James C. Scott developed this into a framework in _Seeing Like a State_ – legibility as what institutions need to function: standardized forms that make complex realities readable and governable. The surname. The cadastral map. The grid city. But that legibility is often crude and extractive, erasing local variation to facilitate state control.

What we are dealing with now is different.

The "magic" of working with AI is that you don't have to standardize _how_ people work. You can provide the AI with fairly unstructured braindumps, going back and forth between topics, closing some loops and opening others. You can let your conversations be messy. The AI reads through the full transcript and restructures it. It finds the threads, identifies the decisions, surfaces what changed (with some caveats, but that is for another post).

The legibility happens at the output, not the process. People stay human. The AI handles the translation.

Is some nuance lost? Of course. Summarization means emphasis, means choices about what matters. But the cost is negligible, the result is useful, and you end up with a system of record that's transparent and fair rather than extractive.

## Outsource boring work

For years, the answer to all of this was "better documentation." And for years, the response was a collective shrug. Documentation felt like a technical nice-to-have. So called non-technical people found it even more tedious (good luck getting your sales team to write and maintain documentation). Busy executives had revenue to chase and fires to put out. The cost was upfront – someone has to write it, maintain it, keep it current – and the benefit was abstract, later, somewhere down the line.

So it didn't happen. Or it happened once, grew stale, and became another artifact nobody trusted.

Two things changed.

First, documentation became more important. It's no longer just operational hygiene. It is now the key that, excuse my hyperbole, "unlocks an army of agents." A different vector of scale entirely. The organizations that have their work documented in legible, structured form can tap into capabilities that others simply cannot access. Documentation got promoted from nice-to-have to strategic lever.

Second, the burden shifted. AI can take messy context – a Slack thread, a voice note, a rambling meeting transcript – and turn it into structured, legible documentation. It can figure out where that information belongs in your existing system. It can update what's already there rather than creating yet another conflicting source.

The skill and discipline that documentation always required? The AI handles that now. You don't write documentation from scratch – you capture what's already happening and let AI structure it. What's left is curation: deciding what matters, what to feed in, what to keep current. A human still steers. But the documentation becomes much more convenient to create _and_ maintain, plus proves its value in such an obvious way every day, that you'll go there voluntarily.

## Compounding

The more you document, the more capable your AI becomes. Not in some abstract "training" sense – you're _not_ fine-tuning a model. You're building context.

This is the broader picture: context engineering matters more than prompt engineering. When I tell the AI to process an input and update our team's documentation accordingly, I don't fix the prompt when I'm not satisfied with the execution. I fix the context – a readme file, a missing link to a related file, a formatting convention.

The full picture of how your business works, captured in plain text that any AI (or human) can read.

Ask a question about your pricing strategy, and the AI can reference what you've already decided. Ask how to solve a problem with your current tool stack, and it knows what tools you're using. New hires onboard from the same source that agents use. Decisions don't have to be re-explained every time someone new joins the conversation – human or otherwise.

This is what it means to scale without losing coherence. **The documentation isn't overhead. It's the substrate.**

## Entry Point

Pick one workflow, one project, one team. Audit it against the six primitives:

- What's the current state, and can you see what changed?
- What artifacts are you working with?
- Where are the change records?
- What checks validate success?
- Can you roll back when it doesn't work?
- Can you trace who did what?

The gaps you find will tell you exactly where the friction lives – why things aren't shipping, why execution feels harder than it should, why scaling keeps breaking what used to work.

And then: start documenting. Not by writing from scratch, but by capturing what's already happening and letting AI structure it. Talk. Record. Transcribe. Let the machine make it legible. (I'll likely publish some templates or guiding ideas for this. But really, the AIs are plenty capable of getting you started. Also: "Can you roll back when it doesn't work?" Sure you can. You can ask AI to restructure your docs, to replace terminology that you want updated, to break up one file gone too large and unwieldy into smaller ones. Let 'em work. Review. Approve. Correct direction. It's inexpensive.)

Bottom line: The primitives that make work agent-legible are the same ones that make work work. Solve for one, you solve for both.
