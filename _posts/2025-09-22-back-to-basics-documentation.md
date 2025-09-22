---
layout: post
title: "Back to Basics: Documentation"
date: 2025-09-22
categories: blog
tags: []
source_url: ""
karakeep_id: "back-to-basics-documentation"
---

LLM models have gotten better — and I'm intentional about saying "better," not "more intelligent." We need different and more specific terminology to describe what LLMs excel at. For one, we must move away from anthropomorphizing them, because this reinforces misunderstandings and misconceptions that inevitably lead to frustration and disappointment. 

Yes, models have improved in many ways while still suffering from most of their fundamental problems. It's better to understand these limitations and learn how to mitigate them than to assume they'll ever be fully solved. Think hallucinations, prompt injection vulnerabilities, and the rest.

## What Hasn't Changed: The State Problem

We're still operating within conversations limited by context windows. While some dream of infinitely expanding context windows, this doesn't actually solve the problem of having the *right* context. You want the most relevant information delivered in the narrowest but sufficient way—complete information with no distractions.

## Agentic Intensification

Now that models have gone "agentic," this problem intensifies. I'm warming up to the term "agent," agreeing with [Simon Willison](https://simonwillison.net/2025/Sep/18/agents/):

> An LLM agent runs tools in a loop to achieve a goal.

Instead of the familiar prompt-response-prompt-response pattern, we now have a single prompt that sends the agent into a tool-using loop. 

And guess what? This makes your context engineering, instructions, tests, specifications, requirements, and workflows exponentially more critical. You're no longer just fixing prompts—those are merely triggers now. You have to fully architect the entire system.

Try it. You'll see. Without proper structure, without breaking work into appropriate chunks, without monitoring each agent's context and context window constraints, you're simply waiting longer than you did with basic chatbot interactions to discover that your agents have gone completely off the rails.

## Documentation Foundation

So what's the point? I'm making an argument for documentation—excellent documentation as a prerequisite. The models can help you create, update, and maintain it, which I think represents a crucial first step and perhaps the best place to start. But LLMs are fundamentally lost without this foundation.

This is where you need to begin: build a solid foundation. It's not difficult conceptually, but it's surprisingly hard to execute well. And it takes time. 