---
layout: post
title: "Memory You Can Trust"
date: 2026-06-19
author: Peter
---

The first useful version of AI memory feels like relief. You stop repeating yourself. The assistant remembers the client, the project, the decision everyone agreed not to reopen. It starts to feel less like a tool and more like a colleague who was in the room.

Then the second problem appears. I ask for a briefing before a steering committee. The answer is good: it knows the workstream, the sponsor, the risk everyone is avoiding. Then one paragraph is wrong in a way that feels almost impossible. It belongs to another engagement. Not invented, exactly. Remembered from the wrong place.

That is easy to blame on the model, but it usually is not the model's fault. It reused something true somewhere else, under a boundary that was never carried with it. The question is not whether an assistant can remember more, but whether it can remember in a way we can trust.

Most talk about AI memory starts from storage: how much it holds, how far back it reaches. In consulting that is not the first question. A firm lives inside boundaries: one client, one matter, one set of rules. A memory that ignores them is not an asset but a way to leak one client's facts into another's. A bigger memory is not a better one, just a bigger surface for the leak.

Memory you can trust has to do four things. It has to be precise: true inside a defined scope, not vaguely true. Durable: still valid after the world has moved. Checkable: traceable to a source, a file or a meeting note. And available: there when the work needs it. The last one is the easiest to overrate. Fast recall is impressive, but recalling something quickly does not make it true, or make it belong to this case.

The consulting version of the rule is simple: the unit is not the user, it is the case. That is the idea behind Case Cortex: memory built around one problem, a deal or a transformation programme. Not a general memory for me, or the firm, or a client. A memory for one case, with the boundary built in.

The build is deliberately plain. A Case Cortex is a folder of text files that people and agents read and write together. If the memory matters, you should be able to open it and read it.

When a case earns structure, it settles into four layers. Canonical facts: what the case knows for certain, kept as one page per entity (a person, a client, a system) and one page per concept (a mechanism, a metric, a term of art). Working memory: an append-only log of decisions, questions, and risks, so a decision can be superseded but never quietly vanish. Derived outputs: the briefings, analyses, and decks generated from the rest, safe to delete because the memory can rebuild them. And pointers: links to the CRM, document stores, and repositories the Cortex tracks but does not own.

The hardest rule is keeping sources apart. A Cortex holds only what was given to that case. The agent may know more; the Cortex does not. A model may have seen similar deals, but none of that is case memory unless someone put it there. This is where memory becomes governance, not convenience. The question is not "what do I know?" but "what belongs inside this case?" If a client name, number, or risk shows up, it should trace back to something the case was given. Otherwise it is a confident mix of source, instinct, and accident.

Case Cortex came out of our own need. We were producing skills, briefings, and client work faster than the old way could keep up, and the failures were ugly: stale notes, duplicated facts, output nobody could trace. The fix was not telling people to be more careful. That is not a system. The fix was to make scope explicit and memory easy to review.

It is not finished, and a long-lived Cortex needs upkeep. But models will keep getting better at remembering, and tools better at storing. The difference will be whether a firm builds boundaries and checks around its memory.

Memory you can trust is not the memory that remembers everything. It is the memory that knows what it is allowed to remember.

---

*Case Cortex is open source. The skill we use to build this kind of memory lives at [github.com/accilium/accilium-skills](https://github.com/accilium/accilium-skills).*
