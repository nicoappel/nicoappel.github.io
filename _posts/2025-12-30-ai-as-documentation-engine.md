---
title: "Why Your Docs Should Live in a Repo Now"
published: true
status: published
created: 2025-12-30
tags: [ai-agents, documentation, work-primitives]
---

Should your internal documentation live in Google Docs or a git repository?

Most teams stopped asking this question years ago. Google Docs won. Non-technical people can't use git. End of debate.

Except it's not the end. The reasoning made sense when it was humans doing all the typing, formatting, placing files in folders. That assumption is dissolving faster than most people realize.

I want to examine this question again – not to relitigate old arguments, but because the ground shifted underneath us. We're going to stress test both approaches. I'll make the case for repositories, then surface the strongest objections and address them directly.

The answer, IMO, is clear. But there's something else most teams overlook entirely. And that might matter more than the tooling decision itself.

## The Direct Comparison

A teammate leaves the company. Their name appears on the team page, in project documentation, in onboarding guides – you're not sure where else. In Google Docs, you start searching. Document by document. Hoping you don't miss one. Hoping someone else didn't create a doc you don't know about.

In a repository with AI as your interface, you say: "This person is no longer working for us. Remove them from the team page, and find any other places in the documentation where they're mentioned."

The AI searches. Comes back: "I found five files affected by this. Here are the proposed changes." You review. You approve. One merge request. Complete coverage. Version history intact.

This is a class of capability Google Docs simply doesn't have.

Here's another: "What changed in our documentation this month?"

With a repository, the AI reads the commit history and summarizes – by author, by topic, by domain. With Google Docs, you're clicking through revision histories one document at a time. If you even remember which documents to check.

And then there's quality. Documentation I produce through AI doesn't have typos. Not because I'm careful – because nothing is typed by hand. Quality agents scan the repository continuously. They check for broken links, inconsistent terminology, naming conventions. Standards that humans struggle to maintain consistently become trivial to enforce.

Google Docs has version history. It has commenting. It has suggesting mode. For many teams, it's genuinely sufficient.

But it can't do comprehensive cross-repository updates. It can't answer "what changed this month" across all your documentation. It can't enforce quality standards automatically. The repository approach doesn't just match Google Docs on convenience – it exceeds the capability ceiling.

There's another dimension most people miss. When you put documentation in a repository, you're putting it in the AI's native habitat.

These tools were trained on code repositories. That's their breeding ground – where they learned to navigate file structures, parse markdown, understand diffs, follow conventions. They know the ins and outs. When you ask an AI to operate on a repo, you're asking it to work in the environment it knows best.

Which means your documentation isn't just for your human team anymore. It's for your AI team too. Every file you structure well, every convention you follow, every piece of context you make explicit – it serves both audiences. The humans who need to understand what's happening, and the AI agents who need to operate reliably.

Google Docs is parseable. But the repo is where the AI lives.

## Stress Test

I told the AI to argue against this approach – to surface the strongest objections a thoughtful skeptic would raise. Not because I wanted to lose the argument, but because I wanted to find the holes I might be sensing but hadn't articulated yet. The challenges it came back with were reasonable. Here's how I'd address them.

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
<p>I don't write documentation by hand anymore. I describe what I want. The AI writes. Typos don't get introduced because nothing is typed manually. Quality agents catch what slips through. The "fix a typo" scenario barely exists in this model.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Reliability.</strong> AI hallucinates. Errors look authoritative when well-formatted.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>Active use surfaces problems. Query the documentation daily, run operations against it, and inconsistencies reveal themselves. What gets used stays accurate. What sits unread drifts – regardless of what tool produced it.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Training.</strong> People still need to understand git, version control, how to troubleshoot.</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>Conceptual understanding, not operational skill. Know what version control accomplishes and why it matters. The AI operates the tools. Training people on manual git operations is optimizing for the past.</p>
</div>

<div class="chat-bubble challenge">
<div class="chat-label">Challenge</div>
<p><strong>Bottleneck.</strong> Every change goes through merge requests. Who reviews?</p>
</div>

<div class="chat-bubble response">
<div class="chat-label">Response</div>
<p>Most changes need no review. This isn't production code. Edits are documented. Rollback is trivial. Review exists for awareness when needed, not gatekeeping. And unlike live-edit systems, you can see exactly what changed and why.</p>
</div>

</div>

The objections are reasonable. In my experience, they don't hold.

But there's a deeper question underneath all of this.

## The Dissolution

The distinction between "technical" and "non-technical" people is eroding faster than most realize.

Most teams never considered putting documentation in a git repository because git is for code. Documentation is just something people write into documents – Word, then Google Docs. Different worlds entirely.

There have been attempts to bridge them. Wikis promised structured, linked documentation – most failed to stick. Notion blends the document model with wiki-like features, and it's genuinely good at what it does. Arguing against Notion is a different piece. But my taste runs toward keeping things as close as you can to the bare metal: text files, version control, minimal abstraction.

The suggestion that docs should live in version-controlled text files, structured like a codebase, surprises most people. Add "and you'll interact with it through command lines and merge requests" and you've lost them completely.

But AI changes the equation. The interface layer shifted.

If you're not seeing this yet, consider it a wake-up call. AI can be the documentation interface. Not someday – now. I'm telling you from the trenches: it works.

What does onboarding look like in this model? You teach people the concepts. What is version control? Why does it matter? What's a commit, a branch, a merge request? You walk them through it once – write some markdown, see what it looks like, understand what a diff shows you.

Then you hand them to the AI.

From that point on, they describe what they want in natural language. The AI handles the markdown, the file placement, the structure, the formatting. Contributors don't need to remember syntax. They need to understand what they're trying to accomplish.

The barrier that kept documentation in Google Docs – "git is for code, not for us" – is dissolving. If you're still making decisions based on that assumption, you might be solving a problem that's disappearing.

## What You Might Be Overlooking

Even if you're still unsure which way to go on the tooling question, there's something you might be overlooking.

This isn't just a decision about where your docs live. It's a directional choice – about what you're developing your team, your organization, and yourself toward.

If you solve the "non-technical people can't use git" problem by adding abstraction layers – a CMS on top, a friendly UI that hides the machinery – you might win convenience. But you also prevent people from developing primitive fluency[^1]: the intuition for how these building blocks work together and compound into capability over time.

From my point of view, you have to actually buy into this direction. Performatively doing a little bit of AI – "we also use AI, we have a chatbot" – won't cut it. That's not going to put you or your team in step with what's happening.

I acknowledge it's difficult to keep up. But this is already happening. And unlike betting on future model capabilities, there's little downside to moving this way. We're talking about what works right now. Putting yourself and your organization into a state where you're leveraging what's already possible – which is already a multiplier – and ready to leverage what's coming.

Jack Clark put it sharply:

> "By the summer I expect that many people who work with frontier AI systems will feel as though they live in a parallel world to people who don't. And I expect this will be more than just a feeling."

The Google Docs question might feel like a tooling decision. It's actually a question about which world you're positioning yourself for.

More on this to come.

[^1]: Primitive fluency: the intuition for how simple building blocks – text files, version control, AI interaction patterns – work together and compound into capability. Term from Nate B. Jones.
