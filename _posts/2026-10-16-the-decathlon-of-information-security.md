---
layout: post
title: "Humanoid Robotics: The Decathlon of Information Security"
date: 2026-10-16
author: Felix
---

POV: It's 2026, Anthropic asks its users to stop being rude to Claude to not hurt his/her/its feelings, an OpenAI model escapes a sandbox training environment and autonomously hacks into Hugging Face, and a researcher quits a frontier lab, warning that its builders believe AI could kill us all by the end of the decade.

In the middle of that weirdness you have the honour of working in AI security. One could be overwhelmed, but I'm also a bit thrilled.

But definitions first: The latter example and most other x-risk stories are rather AI safety considerations (preservation of human life, health & property). Meanwhile AI security focuses on the CIA (Confidentiality, Integrity & Availability) of AI systems. But they are related concepts: AI security establishes a foundation on which AI safety can be ensured. You are well prepared now.

Even within this narrowed scope of AI security there are myriad novel topics to get your head around. Information security considerations for continuous learning models such as [Baby Dragon Hatchling](https://arxiv.org/abs/2509.26507) or Identity and Access Management (IAM) for our new virtual coworkers are just some of our current customer engagements.

However, I'd like to dedicate this post to the very niche niche of industrial humanoid robot information security. There are two reasons why. First, the convergence of various tech leaps (mostly electromechanical & AI) combined with growing industry demands, especially in industrial manufacturing, leads to an explosion in public attention. Second, and more importantly, the nascent and insufficiently mature field of AI security now gets thrown into our physical world. That means rogue AI may not only cause digital harm but may also kick our butts...

To structure the story I'd like to equip you with two main takeaways.

**The first takeaway: humanoids have an immensely large attack surface** compared to other components or systems on the shop floor (or wherever you deploy them).

Unlike their KUKA siblings, humanoids aren't bolted to the floor. They move wherever their reasoning takes them. Yes, AGVs are mobile too, but the combination of extensive mobility and continuous up- and downstream connectivity is unique. Good for versatility, bad for infosec.

Even more importantly, humanoids don't solely run on hard-coded rules but rely on AI, e.g. Vision-Language-Action models, for perception, thinking and acting. Again, a very useful feature, but simultaneously it introduces a whole new class of vulnerabilities to the threat model.

What's notable about those AI vulns compared to traditional ones is that applicability is not binary. A traditional CVE either affects a system, version or configuration or not, nothing in between. For most AI vulnerabilities, that's not the case. Their applicability is rather a probability, depending on the underlying model and harness. Moreover, vulnerabilities in AI systems can mostly only be mitigated rather than fully patched. A super sophisticated security system prompt can never fully rule out someone jailbreaking the system. Bottom line: Probabilistic AI systems (like humanoids) are inherently more complex to secure than deterministic systems.

Two crazy examples to make it more tangible: Within a range where the robot's optical, acoustic or electromagnetic perception can be reached, attackers can simply fool its senses. A [printed patch in the robot's field of view can push its VLA model toward movements the attacker chose](https://arxiv.org/abs/2411.13587), and [ultrasonic commands](https://arxiv.org/abs/1708.09537), inaudible to humans, are perfectly understood by the robot's microphones.

**The second takeaway: once compromised, robots become a dangerous attack tool themselves.**

The combination of some unique risk-amplifying conditions (e.g. operations within perimeters or a human-like action radius) essentially turns successful attacks into insider attacks without a human insider needed. It enables lateral movement across the cyber-physical boundary and significantly extends the potential blast radius. Just imagine bridging air-gapped systems by simply walking there and plugging in a malicious USB stick. Plenty of other scenarios are conceivable, but you get the idea...

So what can operators do? With the optimistic hope that standards and regulations might be only years instead of decades away, we are back to square one: Threat Modeling. With a rough understanding of what can go wrong (think the examples from above) we can at least equip operators with some risk-derived controls. Based on possible attack vectors (path or route used by the adversary to gain access to the robot) I mapped attacks to all vulnerability classes:

<pre>
     <b>VULN TYPE</b> │ <b>EXPLOITING</b>           │ <b>EXPLOITING</b>           │ <b>EXPLOITING</b>
<b>ATTACK VECTORS</b> │ <b>TRADITIONAL SOFTWARE</b> │ <b>AI SOFTWARE VULNS</b>    │ <b>PHYSICAL VULNS</b>
               │ <b>VULNS</b>                │                      │
───────────────┼──────────────────────┼──────────────────────┼─────────────────────
<b>CONNECTED</b>      │ REMOTE CYBERATTACKS  │ REMOTE AI            │ REMOTE PHYSICAL
<b>NETWORKS</b>       │                      │ EXPLOITATION         │ SABOTAGE
               │ e.g. exploiting      │                      │
               │ compromised OTA      │ e.g. executing       │ e.g. remote-
               │                      │ indirect prompt      │ triggering actuators
               │                      │ injection via        │ beyond safety
               │                      │ retrieval channel    │ envelope
               │                      │ [NEW]                │
───────────────┼──────────────────────┼──────────────────────┼─────────────────────
<b>PHYSICAL</b>       │ PROXIMITY            │ PHYSICAL AI          │ VANDALISM &amp; SABOTAGE
<b>ENVIRONMENT</b>    │ CYBERATTACKS         │ EXPLOITATION         │
               │                      │                      │ e.g. performing
               │ e.g. manually        │ e.g. activating an   │ lidar spoofing,
               │ flashing malicious   │ adversarial patch or │ blinding cameras or
               │ firmware via         │ attaching a hardware │ tampering with
               │ unsecured debug      │ implant for          │ hardware
               │ ports                │ perception deception │
               │                      │ [UNIQUE]             │
───────────────┼──────────────────────┼──────────────────────┼─────────────────────
<b>(MISALIGNED)</b>   │ ROGUE AI SOFTWARE    │ AI MISALIGNMENT      │ ROGUE AI HARDWARE
<b>ROBOT ITSELF</b>   │ THREAT               │                      │ THREAT
               │                      │ e.g. deception of    │
               │ (Theoretical threat  │ humans or malicious  │ (Theoretical threat
               │ where a robot,       │ reward hacking       │ where a robot,
               │ without external     │ [NEW]                │ without external
               │ triggering, exploits │                      │ triggering, exploits
               │ its own or other     │                      │ its own or other
               │ software             │                      │ physical
               │ vulnerabilities)     │                      │ vulnerabilities)
</pre>

Decathletes don't get to skip a discipline. Which of these nine is your security team least trained for?
