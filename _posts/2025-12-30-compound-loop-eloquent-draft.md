---
title: "The Compound Loop"
published: false
status: draft-eloquent
created: 2025-12-30
tags: [ai-agents, documentation, work-primitives]
---

Documentation used to be something you wrote for people to read. Now it's infrastructure that agents run against. This distinction matters more than it appears to.

When you structure knowledge so that AI can operate on it directly, something unexpected happens: a compound loop emerges. Better documentation makes agents more capable. More capable agents make documentation easier to maintain. Easier maintenance means more gets documented. The cycle accelerates.

Six months into this approach, we document things we would never have bothered writing down before. Not through discipline. Through economics. The cost collapsed to nearly zero.

## The Architecture

I maintain documentation across ten domains, hundreds of files, contributors with varied technical backgrounds. The system runs on a few key principles:

Text files in version control. Domain-based organization. A style guide encoded in YAML that machines can read and enforce. Five hundred lines of explicit conventions. Pre-commit hooks that catch problems before they propagate. Quality agents that find what humans miss.

For the AI itself: context files at the repository root explaining structure and conventions. Contribution rules that apply equally to human and machine collaborators. Workflow specifications detailed enough that an agent can execute them without improvisation.

The result: a human says "Sarah left - update the team page and anywhere else she's mentioned." The AI searches, finds five files, shows the proposed changes, waits for approval. One merge request. Complete coverage. Version history intact.

## What This Makes Possible

A colleague departs. Rather than hunting through folders hoping to catch every reference, I state the intent. The AI handles the search, the edits, the verification. Comprehensive updates that I would have missed doing manually.

"What changed in our documentation this month?" The AI reads the commit history and summarizes by author, by topic, by domain. Try that with Google Docs - clicking through revision histories one document at a time, hoping you don't overlook something.

This isn't incremental improvement. It's a different class of capability.

## The Obsolete Debate

The old argument was convenience versus control. Google Docs for accessibility. Git repositories for rigor. Choose your tradeoff.

That framing assumed humans would always be the ones typing. AI dissolves the assumption. Contributors describe intent in natural language. The AI handles syntax, placement, structure, linking. The technical barrier vanishes. The benefits of version control remain.

The distinction between "technical" and "non-technical" people is eroding faster than most realize.

## Pressure Testing

I asked the AI to argue against this approach. The objections were reasonable - exactly what a thoughtful skeptic would raise.

<style>
.chat-container { max-width: 100%; margin: 2rem 0; }
.chat-bubble { padding: 1rem 1.25rem; margin: 1rem 0; border-radius: 1rem; max-width: 85%; }
.challenge { background: #f1f1f1; border-left: 3px solid #666; margin-right: auto; }
.response { background: #e8f4e8; border-left: 3px solid #2a7d2a; margin-right: auto; }
.chat-label { font-size: 0.75rem; text-transform: uppercase; letter-spacing: 0.05em; color: #666; margin-bottom: 0.5rem; font-weight: 600; }
.chat-bubble p { margin: 0; }
.chat-bubble p + p { margin-top: 0.75rem; }
</style>

<div class="chat-container">

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Verification.</strong> If contributors can't read the diffs, how do they know the AI did what they asked?</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>The AI presents its intentions before acting. "Here are the five files I'll modify. Here's each change. Proceed?" You don't parse syntax. You approve intent and outcome.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Friction.</strong> Google Docs: see typo, click, fix. Five seconds. Your model adds steps.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>I haven't written documentation directly in months. I describe what I want. The AI writes. Typos don't exist because nothing is typed by hand. Quality agents scan continuously. Standards that humans struggle to maintain become trivial to enforce.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Reliability.</strong> AI hallucinates. Errors look authoritative when well-formatted.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>Active use surfaces problems. Query the documentation daily, run operations against it, and inconsistencies reveal themselves. Errors live in diffs, not hidden in opaque state. What gets used stays accurate.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Training.</strong> People still need to understand git, version control, how to troubleshoot.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>Conceptual understanding, not operational skill. Know what version control accomplishes and why it matters. The AI operates the tools. Optimizing for manual operation is optimizing for the past.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Bottleneck.</strong> Every change goes through merge requests. Who reviews?</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>Most changes need no review. This isn't production code. Edits are documented. Rollback is trivial. Review exists for awareness, not gatekeeping. Unlike live-edit systems, you can see what changed and why - which matters when something breaks.</p>
</div>

</div>

The architecture held. What remains are questions of execution, not design.

## Prerequisites

This requires scaffolding:

Context files that explain repository structure and conventions to AI collaborators. Quality automation that enforces what humans cannot consistently maintain. A rendered interface for human readers - the repository is truth, but people browse a website. At least one person who understands the system deeply enough to intervene when the AI gets confused. And active use - documentation that sits unread will drift regardless of architecture.

## The Shift

The old model treated documentation as a cost center. Time writing was time not working. The new model treats it as infrastructure that compounds. More documented means more capable agents means easier documentation means more documented.

Google Docs optimizes for a world where humans do all the reading and writing. This approach optimizes for a world where AI handles structure and humans handle intent.

That world arrived.
