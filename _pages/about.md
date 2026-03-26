---
permalink: /
title: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi there! I’m Amadeo, a PhD student in Computer Science at the University of Maryland, College Park. My research lies at the intersection of Artificial Intelligence, Mathematics, and Programming. Guided by real-world challenges, I focus on two central questions:

1. How can we design AI systems that are safe, reliable, and robust? (trustworthy AI and its foundations)
2. How can we automate mathematics and programming using AI? (by combining the power of generative AI with the rigor of formal verification and testing)

I also have some experience in [quantum computing](/files/m-thesis.pdf). Outside of research, I enjoy singing, dancing, working out, hiking, reading, and meeting new people. So feel free to send me an email if you’d like to collaborate or just have a conversation!

   ![intersection](/images/int.png)

Current projects
======
**A multi-layer verification harness for LLM-generated code patches**

As coding agents become better at generating patches for real software repositories, the main bottleneck is no longer just generation, but trust. A patch can compile, pass the existing unit tests, and still misunderstand the bug report or quietly violate the user's intent. This matters because software teams are starting to rely on AI systems for debugging and repair, and weak verification can create a false sense of correctness in high-stakes settings.

As a continuation of [A new verifier for coding agents](/files/A%20new%20verifier%20for%20coding%20agents.pdf), we are building a multi-layer verification harness that goes beyond standard test-suite evaluation. Our current approach combines static analysis, baseline dynamic testing, and a semantic verification layer driven by the natural-language issue description. More specifically, we extract behavioral claims from issue reports, ground those claims to the parts of the program touched by a patch, and turn them into executable checks. The goal is to ask not only "Does this patch pass the tests?" but also "Does this patch actually do what the issue says it should do?"

One of the main challenges is that issue descriptions are messy, incomplete, and often ambiguous. Important behavioral requirements may be implicit, while generated semantic tests can fail for the wrong reasons because of bad imports, weak fixtures, or brittle assumptions about the repository. Another challenge is balancing practicality with rigor: full formal verification is out of reach for arbitrary software, so the system must combine noisy signals in a way that is still useful in real development workflows. A big part of the ongoing work is therefore an agentic refinement loop that uses execution feedback to improve semantic checks and recover coverage when the first attempt is too weak.
