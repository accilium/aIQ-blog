---
layout: post
title: "Securing the Wrong Thing"
date: 2026-08-28
author: Christian
---

This week we sat down to figure out what to post next on the aIQ blog. We argued about technical specs, dos and don'ts, even a sneak peek of our internal autonomous agentic risk management approach.

But we decided on something that's more relevant in our eyes: what is AI allowed to do, and what isn't? What tools should my workforce use? What data can they feed into which tool? In short: AI security and governance policies, a topic we already have direct experience with, both for our clients and for ourselves.

So I put the ideas into a storyline, opened a GitHub issue for an initial draft, and sent it straight to my colleagues for feedback. One of them gave detailed, genuinely helpful feedback (this was before I wrote this paragraph). Later, on a Teams call about something else entirely, he complimented me on how fast I'd incorporated it.

But: what feedback? What changes?

So I went back to GitHub. And there it was: an updated draft of my blog post. I went straight to Claude to ask what had happened. And yes, Claude had read the feedback and updated my draft.

I was genuinely shocked. I had never configured a setting allowing it to act autonomously, nor had I approved the task.

Rogue AI? No.

When I asked, Claude explained: "The 'PR Activity Events' and 'drive-to-green' instructions are baked into my system prompt for this environment, under the GitHub Integration section of the Claude Code Remote setup: auto-subscribe after creating a PR, address review comments without asking first. That's environment-level configuration, not something you typed in this chat."

So: company settings, and precisely scoped and intended ones. What that setting allowed: reading a review comment on a draft blog post and pushing an update to that same file, in an internal repository with no client data, plus one reply comment on the pull request. Nothing else. No client data was touched, no compliance issue triggered, and a real time saving for me.

And this is exactly the lesson we try to share with our clients: there's no workable AI policy without mapping your value streams and information flows first. Everything else is guesswork.

So let's get into why most AI policies get this backwards, and how we approach it.

Plenty of companies now have an AI governance, security, or usage policy. Most of them share one root cause behind two very different-looking problems. Some policies are far too strict: written to cover every risk, they end up blocking the value creation or AI transformation the business was trying to unlock in the first place.

Others are far too generic: pulled together from a template or an OWASP Top 10, they were never built around the specific business model. Both come from the same gap. Nobody mapped where the business's real risk and real opportunity sit before writing the rules. The policy is strict in general but still leaves the core value creation exposed, and permissive in general but still shuts down the AI use cases that would have mattered most.

Our approach starts somewhere most policies skip: an analysis of core business. What value streams does the company run? What information flows through each of them, and what kind of information is processed: personal data under GDPR, other regulated data, or simply commercially sensitive information? Only once that picture is clear do we take a business-first look at the realistic high-level AI use cases inside those value streams, not a brainstorm of anything AI could theoretically do somewhere in the company.

The policy then is scoped to secure exactly those use cases. Tight enough to hold up under real risk, but built to leave room for AI transformation, value creation, and rethinking how the work itself gets done.

Two things behind this already run in our own security practice today: a use-case assessment method that maps value streams and information flows to a risk rating and control set before a policy gets written, and an internal tool that checks a built agent's configuration against its policy before it reaches production.

What is also taking shape is the other half. We've named it `ai-policy-assessment-skill`: a skill that reads an existing policy itself, and checks it against the business behind it instead of a generic checklist. It is built, and we've already run it end to end against a real, anonymised governance document.

It delivers two kinds of findings for two perspectives. On the one hand, it flags rules that are too strict and block potential use cases that could transform the business. On the other hand, it evaluates the rules against the value streams, use cases, processed data, regulatory compliance, etc., and flags where the ruleset is too loose and exposes the company to actual risk. In short: one skill improves your policy from two perspectives, the CIO's business approach as well as the CISO's security approach.

If you want to check where your own policy stands, three questions tend to surface it fast. Does it name specific use cases and information types, or only tools and generic rules? Which valuable use case is it currently blocking, and can anyone in the room say why? And if someone needs an exception, who approves it, and how long does that take?

Does your AI policy enable your value creation, or slow it down?
