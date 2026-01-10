---
layout: "post"
title: "Boris Cherny's Claude Code Setup: What I Learned Running 5 Parallel Sessions"
published: true
date: "2026-01-10T22:42:00.603079+01:00"
tags: []
---

# Boris Cherny's Claude Code Setup: What I Learned Running 5 Parallel Sessions

I've been experimenting with Claude Code for months, but when Boris Cherny—the creator of Claude Code himself—dropped a 23-tweet thread about his personal workflow, I stopped what I was doing to take notes.

The insight that hit hardest: he runs 5+ parallel Claude sessions simultaneously. Not sequentially. Not one at a time. Five or more, all at once.

## Why Parallel Sessions Change Everything

Most of us approach AI coding assistants like we approach a single developer: give them a task, wait for completion, review, repeat. Boris treats Claude more like a team.

While one session handles backend refactoring, another explores a UI approach, a third writes tests, and a fourth researches an integration pattern. The context for each stays fresh because each session maintains its own conversation history.

This maps to how I've been using Claude Code for content creation. One session handles research synthesis while another drafts sections. The mental model shift is significant: you're orchestrating, not waiting.

## The Shared CLAUDE.md Pattern

Boris keeps a team-wide CLAUDE.md file that all sessions reference. This is engineering wisdom applied to AI: shared configuration that compounds over time.

Every time someone on the team discovers a better prompt pattern or a gotcha to avoid, it goes into CLAUDE.md. New sessions inherit months of accumulated knowledge without anyone needing to remember to share it.

I've started doing this for my solo work too. My CLAUDE.md contains my writing voice preferences, common mistakes to avoid, and standard workflows. Each new session starts smarter than the last.

## Plan Mode Before Auto-Accept

One practice I hadn't fully adopted: starting every significant task in Plan mode. Boris doesn't let Claude auto-accept changes on complex work until he's reviewed the proposed approach.

This feels slower initially but prevents the frustrating cycle of watching Claude confidently implement the wrong solution. Better to catch misunderstandings before code gets written than after.

## The Verification Investment

Perhaps the most counterintuitive lesson: Boris invests heavily in verification loops, even when it feels redundant. Have Claude check its own work. Have it write tests before implementation. Have it critique its own approach.

These loops feel like they slow you down. They don't. They catch issues before they compound into bigger problems.

## What I'm Changing

Based on Boris's thread, I'm making three changes:

1. **Running at least 3 parallel sessions** for any substantial work
2. **Maintaining a living CLAUDE.md** that captures what works
3. **Starting in Plan mode** for anything beyond simple fixes

The meta-lesson: the person who built the tool uses it as a force multiplier, not a replacement for thinking. He's orchestrating Claude instances like a conductor, not dictating to a typist.

That's the mindset shift worth internalizing.