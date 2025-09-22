---
layout: post
title: "Back to Basics: Documentation"
date: 2025-09-22
categories: blog
tags: []
source_url: ""
karakeep_id: "back-to-basics-documentation"
---


LLM models have gotten better. And I am intentional to say better, not “more intelligent.” 
We need different and more specific terminology to describe what LLMs are good for. For one, we have to get away from anthropomorphizing them, because it just reinforces all sorts of misunderstandings and misconceptions which in turn lead to frustrations and disappointments. But yes, they have improved in many ways, while still suffering from most of the fundamental problems. Better to know about them, and how to deal with them or mitigate, than to assume those will ever be solved (think hallucinations, prompt injection, etc.)
What hasn’t changed: No state. 
We are still operating in conversations that are limited in length (context window). While some dream of context windows getting larger and larger, it doesn’t really solve the problem of having the right context. You want the most relevant context in the most narrow but sufficient way. Complete information with no distractions. 
“
So while models have gone “agentic”, that just intensifies the problem. I am warming up to the term agent, agreeing with [Simon Willison](https://simonwillison.net/2025/Sep/18/agents/):
> An LLM agent runs tools in a loop to achieve a goal.
Now, instead of going prompt, response, prompt, response, …, we go prompt, which then sends the agent off in a loop using tools. 
Guess what? With this, your context engineering and your instructions, tests, specs, requirements, workflows, … you name it, have to be so much more precise. 
You no longer fix the prompt, that is just the trigger. You have to fully “system architect” all the rest. Try it. You’ll see. If you don’t provide structure and chop up the work into appropriate chunks, keep an eye on each agent’s context and context window, and all that, you are just waiting longer than you did with the past prompt-response game in the chatbot UI to see that your agent(s) went off the rails.
So what’s the point? I am trying to make an argument for documentation. Excellent documentation is required. The models can help you create, update and maintain it. And I think this is a key step – maybe the best thing to get started with. But the LLMs are lost without it. Hence, this is where you need to start. Build a foundation. It’s not difficult, but kinda hard to do well. And it takes some time. 
