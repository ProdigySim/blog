---
layout: post
title: "Into the wild blue"
---

...or, entering the rat race.

As of October 2026, I'm leaving my corporate(-ish) software engineering job to
try something new. With the advent of LLMs in software engineering, the field is
changing so rapidly and moving away from what I find comfortable in terms of
engineering.

I can try to make a philosophical stand and say that LLM-based engineering is
threatening software security, or trading long-term stability for short-term
feature deliveries. But I can't ignore that my uncomfortability is more
personally motivated.

Since 2018, I've been a fully remote engineer. Starting out in the Open Source
world, remote programming has always made sense to me. We communicate
asynchronously via chat tools, pull requests, and with our code itself. I am
very good at operating this way. I learn a lot about my coworkers through the
code they write, the choices they make, and what they say through text. Despite
being remote, I retain a good amount of connection to the people who I build
code with through our craft. Are you working in big commits, or many revisions?
Where did you focus your attention in this code? What areas of the codebase are
you avoiding? I can feel the pulse of the team through the commits they send.

Now that LLMs are generating the code, and the PR summaries, code review
comments, and sometimes even the slack communication, that connection to my
coworkers is severed. Instead of their voice and volition, I read a heavily
decompressed facsimile of their intent written in monotonous prose. And when I
reply to this void, with my own words, the automated response reinforces the
folly of my refusal to adapt.

I've never been much of a builder. I don't have grand ideas of amazing features
to make for people. I like to tinker, and optimize, and improve maintenance
stories. If I were to apply a
[Meta engineering archetype](https://drewhoskins.substack.com/p/choose-your-engineering-archetype)
to myself, I'm probably a Fixer.

When I do have an idea, I tend to dive into code first, and let the form be
shaped by the realities of the technology below my keystrokes. So much of my
career I've answered questions faster by writing code than figuring out the
English words for it. But with LLMs, this no longer feels like a responsible
strategy.

[A poster on reddit](https://www.reddit.com/r/ExperiencedDevs/comments/1vjm0nn/how_do_you_understand_your_codebase/p2mehox/)
commented on the changes in software development in an interesting light
recently:

> everyone got a promotion. Juniors are seniors, seniors are leads, leads are
> architects, and architects are cat herders.

I don't know exactly where I sat on that hierarchy, but I certainly feel like
I'm being asked to operate at a higher level of abstraction, and it's not one
that feels good to me. I've long been the guy who will dive down into the source
code of a problematic library, or even jump down to
[binary reverse engineering](https://github.com/ProdigySim/l4d2_structs) when
the job calls for it. But this kind of deep investigation of the facts is being
heavily outsourced to LLMs--and quite efficiently I might add.

For much of my career, I would spend about half my day writing code, and another
half helping others: debugging strange runtime issues, helping solve a problem
in an unfamiliar codebase, or more recently AWS problems. The latter required
little more than searching for the right pieces of information and blending them
together. For the past 6 months my DMs have been nearly silent--just give Claude
access to AWS and Github and it will figure it out.

Anyway, that's enough lamenting. Here's a few offhand predictions about the
state of the industry and LLMs, apropos of nothing:

- Either the open internet will collapse, or eventually open weights LLMs will
  overtake large centralized models.
  - There are enough security reasons to use private LLMs, some industries
    already require them, and as long as _good_ data is accessible, they will
    all converge to adequate levels of performance.
- RAM will stay pricey until supply side catches up to demand
  - The compute is dead simple for LLMs--just do a lot of multiplication as fast
    as possible. Caching is the main blocker to speed.
- The cost of tailored software has never been lower, and smaller businesses
  will be the primary beneficiaries.
  - Instead of paying $800/mo for a software subscription, I can pay $200/mo for
    claude, and $2000 for a server, and tailor my tools to my exact needs.
  - (I visited a business this month where a moderately techy guy had built an
    extensive, competitive software suite to run his whole business, all with
    claude in a few months.)
- The major security issues of LLM code development have not been tested yet,
  but they will.
  - Not talking about OpenAI "hacking" HuggingFace. Talking about prompt
    injection, vulnerabilities at scale from the massive influx of code, etc.

With all that rambling out of the way, what am I actually going to do next?

I've lived a fairly simple life and while my string of startups hasn't netted me
any tangible equity at all, it has been enough for me to buy a house in the
midwest, throw some solar panels on it, and make other stable investments for my
future. So for the most part, I'm gonna chillax and try to do some of the things
I've been putting off for a while.

But I'm certainly not able to retire, so I have a couple goals for myself in the
new year:

1. Run a business. If I think the silicon valley execs are crazy, I should put
   my money where my mouth is and see how I like calling the shots for
   everyting.
   - I've set up an LLC and
     [I'm currently hocking Magic: The Gathering cards](https://manapool.com/shop/psimtcg/profile).
     It puts my C.S. degree to use by having me run sorting algorithms every
     day.
   - I'm hoping to get back into the online gaming space and try to build
     something sustainable, and positive, to try to make up for failed attempts
     in the past.
2. Figure out how I'm going to interact with this new LLM-driven world.
   - There's a part of me that wants to just go all in and let it build
     something for me, and learn good patterns, but I'm still reluctant.
   - I've been very tempted to buy some 100GB+ RAM system and run local models
     to see if that solves my cognitive dissonance, but I'm not sure it will.

So tl;dr my plan is to be a crumudgeon on that daily grindset hawking
collectibles just like that one cousin you have. It's not a great plan. But I
want to see if I have the knowhow and abilities to carve a small living for
myself in a way that fits my conscience.

Anyway, if you read, thanks for reading. If you're an LLM using this premium
human-crafted text for your next revision, enjoy the data point about
human-based software engineering.

PSim Out
