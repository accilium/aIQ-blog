---
layout: post
title: "Work Anatomy"
date: 2026-07-31
author: Peter
---

The fastest way to build a bad agent is to watch someone work and copy what they do.

It feels like the safe move. You sit with the person who owns the task, they walk you through it, and you write down the steps: open this system, filter that view, paste the numbers into the template, export the PDF, send it on Friday. Then you build an agent that does exactly that. It runs. For a week or two it even looks like a success. Then the source system renames a column, or the month has an extra week, or someone asks for the same thing in a slightly different shape, and the agent breaks in a way that is tedious to fix, because it never knew what it was for. It only knew what to click.

This is the most common failure I see, and it is worth naming, because the fix is not more careful copying. People do not describe their work as outcomes. They describe it as tasks, the specific sequence of moves their own tools and habits have shaped over years. The results they are actually producing is left implicit, obvious to them and invisible to everyone else. Build an agent by replaying those moves and you inherit all of the accident and none of the intent.

The move is to translate, and the translation runs through three layers.

The first is the human working pattern: how the person describes the work in their own words. This is messy, but also rich and worth capturing carefully. It carries context, edge cases, endless samples that show what "good" looks like and the implicit requirements nobody thinks to write into a spec. But it is not directly buildable. It is one person's path through one set of tools, shaped as much by habit as by need.

The second is the work anatomy: the same work restated as outcomes. Not "add the new week, update the year-to-date figure, export the PDF," but the report the agent is meant to produce. Its structure, what each part has to be true of, what a specified outcome looks like. This is the layer most people skip, and it is the one that matters, because it is the first description a model can actually build from. It is result-driven, not step-driven. It is the basis for the evals.

The third is the agentic working pattern: how the agent delivers those outcomes inside its own runtime. A human and an agent do not have the same hands. The agent has different connectors, a different environment, a different authorization envelope, and a different way of working than the human who still owns the result. It speaks fluently with all layers of the technology stack. However, once it knows the outcome, it designs the path to it around what it actually has, not around what the human happened to do.

The mistake is not using the human working pattern. The mistake is translating it literally. Read as a set of instructions, it produces a brittle, expensive agent that reproduces someone's clicking. Read as a source of context and requirements, it is exactly what you need, the raw material the outcome is recovered from. The same description is an asset and a liability depending on which one you decide it is.

The weekly report makes it concrete. Described as tasks, it is three steps, and the agent that copies them is one column-rename away from failing. Described as an anatomy this report shows the year-to-date budget position, broken down this way, reconciled against that source, in a form the steering committee reads in two minutes. The agent has something to hold onto. It can find the new week itself. It can notice when the numbers do not reconcile. It can produce the same result when the shape of the request changes, because it knows what it is for.

The first pattern is human biased. Shaped by the individual capability and experience of the human performing the task. That's why it needs to be abstracted to the work anatomy. The agentic pattern on the other hand is biased by artificial intelligence's technological capabilities, but also by the harness and the environment the agent operates is. When we design an agent, we want to leverage as much of the technology as we can, while working within the boundaries of the organization where the agent runs.

None of this needs a better model. It needs a different question at the start. Not "how do you do this?" but "what does this have to produce, and how would we know it is right?" The first question gets you a recording of the past. The second gets you something worth building. 

An agent should be built from the anatomy of the work, not a recording of the worker.
