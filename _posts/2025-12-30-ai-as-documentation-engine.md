---
title: "The Compound Loop: Documentation in the Agent Era"
published: true
status: published
created: 2025-12-30
tags: [ai-agents, documentation, work-primitives]
---

Documentation isn't reference material for humans anymore. It's operational infrastructure that agents run against.

This changes everything about how you should think about documentation - what it's for, how it's structured, where it lives.

The compound loop: more documented -> more capable agents -> more documented. Each cycle increases what's possible. Six months into running documentation this way, we cover things we never would have bothered to write down. Not because we became more disciplined - because the cost of adding documentation dropped to nearly zero.

Here's what that looks like in practice, and why holding onto tools like Google Docs means missing the shift entirely.

## What This Looks Like In Practice

I run an internal documentation system for a team. 10+ domains, hundreds of files, multiple contributors with varying technical backgrounds. Here's the architecture:

**Structure:**
- MDX files in a git repository
- Domain-based organization (customer-support, development, business, tools)
- Hub-and-spoke navigation (master README -> domain READMEs -> content)
- Rendered to a static site for human reading

**Quality management:**
- Style guide in YAML (machine-readable, authoritative)
- Conventions document (~500 lines of explicit rules)
- Pre-commit hooks that validate MDX syntax, links, naming conventions
- Quality agents that scan for and are able to fix typos, broken links, structural issues

**For AI collaborators:**
- CLAUDE.md at repo root (context for any AI working in the repo)
- AGENTS.md (contribution rules for AI and humans)
- Domain-specific instruction files
- Full agent specifications with workflows, templates, output formats

The AI operates on this substrate directly. A human says "update the team page - Sarah left last week." The AI finds the file, makes the edit, checks for other mentions across the repo, shows the diff for the operator to review and approve, creates a merge request.

## The Capability That Settles It

Here's an example that illustrates why this architecture matters:

I notice a teammate has left the company. I tell Claude: "Remove them from the team page. Also find any other places in the documentation where they're mentioned and update those."

Claude searches the repository. Finds five files that reference this person. Shows me exactly what would change in each file. I review - looks right. Approve.

One merge request. Clean commit message. Comprehensive updates across the entire repository - updates I wouldn't have caught manually scrolling through Google Docs.

**This is a capability class that Google Docs cannot provide.**

And visibility: "What changed in our documentation this month?" With git + AI, Claude reads the log and summarizes by author and topic. I can narrow this to any part of the docs: "Summarize the changes to our GTM repo."

How would you do that with Google Docs? You wouldn't.

## The Old Framing Is Dead

The old debate was: convenience (Google Docs) vs. version control (git repos).

If you chose the repo, non-technical people were locked out. They'd need to learn git, Markdown, pull requests. Most organizations couldn't justify that training overhead.

That framing is obsolete.

AI eliminates the "non-technical people need git" barrier. Contributors describe what they want in natural language. The AI handles Markdown syntax, file placement, structure, linking. The technical barrier is removed while the artifact benefits are retained.

The distinction between "technical" and "non-technical" people is blurring fast. At the current pace, "near future" is actually near.

## Adversarial Stress Test

I asked the AI to challenge this argument. The counterarguments were reasonable - the kind of objections most people would raise.

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
<p><strong>The verification problem.</strong> If non-technical contributors can't read Markdown or git diffs, how do they verify the AI did what they asked? They're dependent on the AI's interpretation being correct.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>The AI shows what it intends to do before doing it. "Here are the five files I'll change. Here's what each change looks like. Do you want me to proceed?"</p>
<p>The human doesn't need to understand Markdown syntax to understand "I'm removing Sarah from the team page and three workflow documents." You're approving intent and outcome, not parsing syntax.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>The friction math doesn't add up.</strong> Google Docs typo fix: See it, click, fix, done. 5 seconds. Your model: See issue, open Claude, describe it, AI processes, creates MR, merge. More steps.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>The AI is writing the documentation almost exclusively. I haven't written a single line of documentation in months - I've given input, dictated what I want, but never written it directly.</p>
<p>The typos shouldn't be there because everything is AI-written and AI-reviewed. We also have quality agents that scan repositories regularly. Standards that humans struggle to maintain consistently are trivial for AI to enforce.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>AI reliability tax.</strong> AI makes mistakes. In documentation, what catches hallucinated or subtly wrong information? The error looks authoritative because it's properly formatted.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>By actively working with the documentation on a daily basis - querying it, running operations against it - you surface things that are missing, outdated, or wrong.</p>
<p>If I ask "what do we have on this tool" and something smells off, I can immediately check and update it. Documentation that gets used stays accurate. Errors are visible in diffs, not hidden in state.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Training overhead.</strong> You're underestimating how much people need to learn. Git concepts, version control, enough to troubleshoot when things go wrong.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>The training requirement is conceptual, not operational. People need to understand what version control is and why it matters - but they don't need to operate git directly.</p>
<p>They describe what they want; the AI operates the tools. Optimizing for manual operation of development tools is optimizing for the past.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Review bottleneck.</strong> All doc changes go through merge requests. Who reviews? You've created a gate that slows everything down.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>Most merge requests don't need review. We're not shipping software to production. We're making well-documented edits. And we can always roll back.</p>
<p>Review is for awareness, not gatekeeping. Unlike Google Docs where anyone can edit live, the merge request model means you can see what changed and why - which matters when something goes wrong.</p>
</div>

</div>

The argument held up. The remaining concerns are about execution, not architecture.

## What Makes It Work

This isn't magic. It requires specific infrastructure:

**Good context files**: CLAUDE.md and AGENTS.md that tell AI collaborators how the repo is organized, what conventions to follow, where things go. The AI needs to understand the structure before it can operate on it.

**Quality automation**: Pre-commit hooks, validation scripts, quality agents. Standards that would be impossible for humans to maintain consistently become trivial for AI to enforce.

**Rendered output for humans**: The repo is the source of truth, but humans read a nicely rendered static site. The experience is as good as any wiki - you just edit through a different interface.

**At least one power user**: Someone who understands the system deeply enough to troubleshoot when AI gets confused. This person maintains the scaffolding.

**Active use**: The error-detection model depends on people querying the docs regularly. Documentation that sits unread will drift. Documentation that gets used daily stays accurate because errors get surfaced and fixed immediately.

## The Fundamental Shift

This isn't a slight upgrade to documentation workflows. It's a fundamental shift in purpose.

Old model: Documentation is something humans write for other humans to read. It's a cost center - time spent writing docs is time not spent doing "real work."

New model: Documentation is the substrate that agents operate on. It's infrastructure. The more you document, the more capable your agents become, which makes documentation easier, which means you document more.

Google Docs is optimized for a world where humans do all the writing and reading. The repo-plus-AI model is optimized for a world where AI handles structure and humans handle intent.

That's the world we're in now.

---

## Appendix: Key Components

For those implementing something similar:

| Component | Purpose | Example |
|-----------|---------|---------|
| **CLAUDE.md** | Repository context for AI | Project overview, common commands, restrictions |
| **AGENTS.md** | Contribution rules | Branch naming, commit format, validation requirements |
| **Style guide** | Terminology authority | YAML file with brand spellings, capitalization rules |
| **Conventions doc** | Structural rules | File naming, directory organization, metadata standards |
| **Pre-commit hooks** | Quality gates | MDX validation, link checking, naming conventions |
| **Validation scripts** | Enforcement | Python/JS scripts that check standards programmatically |
| **Agent specifications** | Workflow guidance | Detailed specs for specific agent tasks |
| **Domain READMEs** | Navigation | Hub-and-spoke structure with clear entry points |

The interface can adapt to the team. I use Claude Code directly. For teams already living in Slack, a bot could translate natural language requests into documentation updates. The key is that the substrate stays the same regardless of the interface layer.
