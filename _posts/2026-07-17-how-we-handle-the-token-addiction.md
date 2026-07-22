---
layout: post
title: "How We Handle the Token Addiction"
date: 2026-07-17
author: Sebastian
---

Last week our Head of IT sent me a screenshot. A Microsoft purchase screenshot: prepaid Copilot credits, and a single button that would commit a little over two million euros to buy them. One click, no procurement, no signatures. He sent it the way you send something you can't quite believe.

A bill like that does not appear out of nowhere. It appears when a tool has quietly become part of almost everything you do. We half-joke about token addiction; nobody is actually addicted. What happened is more ordinary: AI moved into a large part of how we work. We no longer only draft and summarise with it - we build with it, the skills and agents that now carry real work. For two years that cost the same whether we ran it once or twenty times a day. Flat pricing hid the bill, and we always knew it would not last - metering and lock-in were the obvious next chapter. So we did not wait for the announcement but went to work. The usage meter wears different faces - Copilot credits, per-token API lines, the five-hour session window we consultants work inside - but it is the same shift: what used to be bundled in a flat-rate is now counted as you go.

We are consultants. What clients buy from us is judgment, and judgment now reaches into questions it never used to: what a task should cost, and which model it deserves. Increasingly, that is also what clients ask us to help them work out. So rather than tell people to use less - which produces guilt and little else - we made the cost visible at the moment someone decides. Three things, so far.

We measure. Our skill-building routine has always tested a skill before it ships; now the test also records its token burn on a real run. What we never priced until now, we now write down.

We write it into the skill. Every skill carries frontmatter - the metadata at the top of the file that says what it does and when it runs. Now it also declares what it costs, so the price sits in plain sight beside the purpose, visible to anyone who will use it.

We gate it. A skill that will run up a large bill stops before it begins and says plainly what it costs and where the cheaper path lies. And the cheaper path is rarely one vendor's menu: Copilot alone puts Claude and GPT models next to each other, and Mistral sits within reach too. Most tasks do not need the frontier model - for this task e.g. use Sonnet instead of Opus, start the next session on the smaller model, and reach for the large one only when the task needs the depth. The point is not any single switch; it is picking the model the task deserves. Token gating is a deliberate half-second of friction, placed exactly where the money is committed.

One thing we learned the hard way: it is far cheaper to live within a session than to buy your way past one. A session runs for five hours, and the discipline is to decide at the start what those five hours are for. When the work runs long, the tempting move is to keep going past the included limit - which switches you to consumption billing at standard API rates, on top of the flat rate you have already paid. We stopped doing that. If we run out before the window closes, we wait for the next one rather than pay a premium to finish a little sooner. Planning the session a bit more and waiting a bit turns out to be cheaper than powering through it.

None of this is a finished solution. Measuring token burn is rough, the choice between a large model and a small one is a judgment we sometimes get wrong, and a gate shown too often becomes a box people click through without reading. We would rather ship it blunt and sharpen it than wait for the complete version that never arrives.

But the longer I sit with that screenshot, the less it looks like a bill and the more it looks like a challenge. A price on every token forces a question the flat-rate years let us dodge: how much (artificial) intelligence does this task actually need? Most of the time, the honest answer is less than the frontier model. That reopens a conversation the industry has been postponing - about open-weight models, running on infrastructure we control, capable enough for the bulk of the work, cheaper to run at scale, and free of the lock-in that put a two-million-euro button on someone's screen in the first place. And cost is only half of that argument: a European model like Mistral, or a model run on our own infrastructure, also answers the question clients ask right after the price - where the data goes. The token meter is uncomfortable but it might also be the most clarifying thing to happen to the way we use AI in a while.
