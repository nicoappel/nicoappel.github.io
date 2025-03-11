---
layout: post
title: "Personal Knowledge Management"
tags: PKM, Zettelkasten
---
The nerdy version. Because I have a draft for another article [over there](https://nicoappel.substack.com/) in which I’m making an effort to keep it all very simple.

But this here… we can talk shop.

## Tool

Let’s start with the core tool right away: I am typing this in [SilverBullet](https://silverbullet.md/),

> … a note-taking application optimized for people with a [hacker mindset](https://en.wikipedia.org/wiki/Hacker). […] Where your notes essentially become a _database_ that you can query; that you can build custom knowledge applications on top of? A _hackable notebook_, if you will?

SilverBullet reminds me of Roam Research, which I used for a while. Compared to Roam Research, or Notion, SilverBullet is nothing but plain text files, formatted in Markdown, stored locally on my device.

Running Silverbullet in a Docker container locally on my Mac is a bit of a stretch for me, tech skills and such. I’ve done things like that, but I only understand a very small part of what’s actually going on. However, this is 2025 and I have a few very knowledgeable friends that never sleep. I can ask for help and get some pretty solid advice whenever I am lost.

You’ll be reading this on a blog that is built with Jekyll and hosted on Github pages. I set this up just the other day. I had some one-digit percentage of the necessary knowledge/experience. Again, I had some help. Apparently, we got it done. Amazing. Still blows my mind 🤯.

## Personal Knowledge Management

At its core, I think, **personal knowledge management** based on [Zettelkasten](https://en.wikipedia.org/wiki/Zettelkasten) (I also like [Andy Matuschak’s Evergreen Notes](https://notes.andymatuschak.org/z5E5QawiXCMbtNtupvxeoEX), or more modern and digital take) has three components:

1. Creating notes
2. Making connections
3. Refining notes

There are _many ways_ to **create notes** in the first place. That’s probably the easiest part. Mostly, I suppose, it should be low friction. You can always edit your notes progressively.

As for **making connections**, this seems a cognitive and manual, or technical, process. You could get assistance from AI, but you probably want to stay in the loop. Otherwise, you miss out on the benefits, meaning:

> If we push ourselves to add lots of links between our notes, that makes us think expansively about what other concepts might be related to what we’re thinking about. It creates pressure to think carefully about how ideas relate to each other. – [Matuschak](https://notes.andymatuschak.org/zF8xCU4BwXwbmSyp7tmff9i)


**Refining notes** requires significant cognitive effort. It is active learning.

❗Don’t miss this: it’s _personal_ knowledge management. You “write notes for yourself by default, disregarding audience” ([Matuschak](https://notes.andymatuschak.org/zXDPrYcxUSZbF5M8vM5Y1U9)).

## More Tool 

Back to the tool: SilverBullet automatically creates bi-directional links. Something that Notion’s missing.

What’s cool about this, is that I can even instruct an AI system to assist in creating Zettelkasten-style notes _and_ have it use the formatting to create internal links.

So I tell the AI about the format, like this:

```
I am using SilverBullet for my notes.

This means, we use the following format. 

Instructions in the formatting example are set in single curly brackets like `{this}`:

<format>
---
title: {same as note title}
tags: {suggest tags, comma-separated, as you see fit}
ID: {leave empty}
type: {could be 'note', 'concept', 'structure', 'principle' etc.}
---

{Content of the note goes here.  Markdown format. Silverbullet uses double square brackets for internal links, so you can link notes/pages, existing or not by simply writing [[note/page title]]}

{Incoming links, so called linked mentions, are added by the software automatically.}

</format>
```

With these instructions I can use the AI assistant to suggest and creat notes that are _already connected_. 

```
---
title: Cognitive Elevation Model
tags: cognition, models, AI augmentation, knowledge work
ID: 
type: concept
---

The Cognitive Elevation Model provides a framework for understanding how knowledge workers interact with tasks at different cognitive levels, helping determine appropriate AI integration strategies.

Three primary domains:
1. [[Eye-Level Domain]]: Zone of optimal professional performance
2. [[Above-Level Domain]]: Cognitive challenges requiring scaffolding
3. [[Below-Level Domain]]: Tasks not requiring full cognitive capacity

This model serves as a decision framework for determining what tasks should be:
- Directly performed by the knowledge worker
- Augmented through AI collaboration
- Delegated to AI systems

The model maintains human agency while optimizing cognitive resource allocation across different types of professional activities.
```

As you may realize, I apply this approach to structure my own output, not to a topic I am trying to learn or study. The example is based on a simple framework I am using in some of my presentations.