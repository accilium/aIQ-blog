---
layout: post
title: "The Cheapest Hacker You'll Ever Face"
date: 2026-10-30
author: Cristian-Marian
---

In January, an attacker broke into the IT network of a water utility in Mexico and decided, as we all so often do, to hand part of the work to an LLM. For this task, the attacker picked Claude, which did the reconnaissance. Soon, Claude had independently found a SCADA gateway, decided it was interesting, and started reading through the vendor documentation. It concluded that the logical next step was, of course, to build a password list and try to break in.

When Dragos published its analysis in May, it did not make major headlines.

As of today, AI has not, in the wild, invented a single new way to attack an industrial control system. In Monterrey, the attacker brought no OT knowledge, no OT objective, and no novel technique. The AI super-hacker that can take down a nation's energy grid with a very clever prompt is what I used to call a "future us" topic.

There is, however, a very serious and immediate discussion to be had right now: **the economics heavily favour the attacker.**

Think about what an OT attack actually requires. There are two stages. Stage one is the boring part: break into IT, look around, and move sideways until you find the door to the OT network. Stage two is the really hard part: making a physical process misbehave in a way that is reliable, controllable, and actually does what you want it to do. That takes significant effort and expertise across several disciplines, and in the wild, AI has done very little for it so far.

In the labs, the situation is changing fast: already in May, a newer version of Anthropic's Claude Mythos Preview completed the UK AI Security Institute's simulated power plant attack in 3 of 10 attempts, against a network with no active defenders. "Future us" is arriving faster than expected. But the real problem today is stage one, because the attacker is now able to solve it for pennies on the dollar.

In Monterrey, Claude identified OT-adjacent infrastructure within hours of getting into IT. In the UK AI Security Institute's testing, GPT-5.5 solved a reverse-engineering task that took a human expert twelve hours in about ten minutes, for $1.73 in API costs.

**The marginal cost of an attack is falling toward zero,** and the time between getting into a network and the first attempt on OT is shrinking fast.

As I write this, the threat is twofold. There is still the brilliant attacker, backed by significant resources and ready to do serious damage. That threat is not new. But there is a new one on the horizon: a swarm of mediocre attackers, running at machine speed, who used to ignore OT because it was too much effort and now trip over it because a general-purpose LLM literally points them toward it.

**The threat is already here, and the basics are what matter**

As a Romanian, I am constantly reminded how vulnerable we are when the basics are not done right. In December 2024, the Lynx ransomware gang breached Electrica, one of Romania's largest electricity suppliers.

Then, in December 2025, Apele Române, the national water authority was hit. The attackers encrypted roughly 1,000 IT systems across its headquarters and 10 of its 11 regional basin administrations. The hydrotechnical structures kept working, albeit operated manually. Romania's National Cyber Security Directorate (DNSC) noted that the authority was not yet enrolled in the national protection system for critical IT infrastructure.

The day after Christmas, CE Oltenia, Romania's largest coal-based power producer, was hit by yet another ransomware attack, which took down its ERP, document management, email and website. Then, in February, the Qilin ransomware gang hit Conpet, the national crude oil pipeline operator, disrupting its IT and taking down its website. Oil transport was not affected.

Notice what every one of those has in common. The attack landed in IT, but operations largely kept running, mostly thanks to segmentation, backups and, to be honest with ourselves, a fair amount of luck.

Then came ANCPI this July. ANCPI is Romania's national cadastre and land registry agency. It is not an industrial operator, but it is the purest example yet of a cheap attacker at work. According to testimony in Parliament, the way in was a vulnerability known since 2021, on a publicly exposed server handling user authentication. The same administrator password had been used across different accounts. The attacker was inside for more than three days before anyone noticed, deleted virtual servers, and hit the Romanian property market like a truck, freezing transactions for almost a month. The head of DNSC said it was not a complex attack and could have been prevented.

Realistically, no one needed AI for that one. Now give the same attacker a capable model, and the threat model paints itself: commodity attacks, in IT, forcing expensive OT consequences.

**The end of the world? Not quite.**

AI has made existing weaknesses cheaper to exploit, so known gaps are more dangerous this year than they were last year.

The answer is not an autonomous SOC. At least, not yet. It is the work everyone already knows about, now with real urgency attached. The basics: an asset inventory that is actually maintained. Then, IT/OT segmentation and MFA on every remote access path. Investment shifted from prevention-only toward detection and response inside OT. Vulnerabilities prioritized by whether they can reach a physical process, not by their CVSS score. And yes, AI on the defenders' side too, carefully bounded, because it cuts an assessment from weeks to days.

None of this will get anyone a keynote slot.

The basics seldom fail because nobody knows them. They fail because nobody owns them. And getting them right is the name of the game, because the cheapest hacker we will ever face is not brilliant. He does not need to be. He just needs your known gaps to still be open when his AI finds them.
