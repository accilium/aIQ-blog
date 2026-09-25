---
layout: post
title: "What People Get Wrong About Skills"
date: 2026-09-25
author: Leo
---

Last week a colleague showed me a skill he had built. He pasted a meeting note into the chat, typed the name of the skill, and twenty seconds later had a status mail in the house format, ready to send. It used to take him half an hour. People in the call were impressed, and so was I. Then I noticed what I was actually looking at: a person, sitting in a chat window, pressing enter.

Almost every skill request I get has that shape. Make me faster at the weekly status. Take the repetitive part out of the RFP screening. Turn my notes into slides. The skill fires a workflow, the workflow runs, the human reads the result and moves on to the next prompt. That is how we use skills today, and in the [June post](https://accilium.github.io/aIQ-blog/2026/06/03/how-we-ship/) we described them exactly that way, as markdown files that encode a consulting workflow.

I think this is the big misconception. The German word is Irrtum, and it fits better, because it is not a misunderstanding of what a skill does. It is an error about what a skill is for.

Look at the picture again. The human still opens the chat. The human still decides that now is the moment to run the skill. The human still reads the output and decides whether it goes out. The skill made one step faster. The person is still doing the work, and the chat window is the proof. A faster human is a fine result, but it is not where this goes.

Said out loud, it is obvious. Today humans do the work. Soon agents do the work. A skill is the step in between. It exists because we are moving from one to the other, and its real job only shows up once we get there. When the agent runs the weekly status on its own, nobody is in the chat. Nobody types the skill name. So what is the skill doing then?

It is making sure the agent does the real work correctly. That is the whole point, and it was the point all along. We just met skills first in the one place where it is hardest to see, the chat, where a person is still doing the steering by hand.

A skill is written in plain language. A consultant wrote it, a consultant can open it and read it, and an agent executes it. It is the one artefact both sides can read without translation. That makes it the layer where a human steers a machine that will act without them. The agent we put into a Teams chat this summer is the clearest example I have. Which folder it reads, when it posts, what it may never do, what it says when it cannot finish: all of that is in a file a colleague can open and change. We swapped the model underneath twice. The file stayed.

The other half is the quality gate. A skill written for a chat says what to produce. A skill written for an agent also says what done looks like. What shape the output has, which checks run before anything leaves, which questions it must refuse to answer, when it stops and asks a person. The [judgement post](https://accilium.github.io/aIQ-blog/2026/08/07/judgement-you-cant-grade/) made the argument that the test only works because the output has a shape. That shape has to live somewhere the agent reads on every run. The skill is that place. Without it, an autonomous agent is a confident junior with no reviewer. With it, the reviewer's judgement runs at three in the morning while the reviewer sleeps.

So the two things people celebrate, personal speed and less repetition, are side effects. They are real and I will take them. But building skills for the chat, tuning them so the prompt feels smooth and the answer comes fast, optimises for a moment we are about to leave. Skills are the control layer between people and autonomous agents. Steering and gating, not typing less.

This changes how we should write them. The test I apply now: imagine this skill runs on its own, on a schedule, with nobody reading along. Would I let the output go to a client? If the answer is no, the skill is missing half of itself. Usually the missing half is the boring half: the list of what must be true before the result counts, and the instruction to stop instead of guessing.

It also changes what our expertise is worth. A consultant who knows how a good RFP screen looks, and can write that down precisely enough that an agent gets it right without them in the room, has turned ten years of judgement into something that runs every night. The one who only got faster at doing it themselves has a nicer Tuesday.

We said in June that the word skill will probably be gone in a year, bundled into plugins or whatever comes next. I still think so. The layer will not be gone. Something between a human's intent and an agent's actions has to say what correct means, and a human has to be able to read and change it. Call it whatever you like by then.

So the next time you build one, who are you writing it for? Yourself in the chat, or the agent that will run it when you are not there?
