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

Current projects:
======
**1. Towards automatizing programming**

As coding agents become better at generating patches for real software repositories, the main bottleneck is no longer just generation, but trust. A patch can compile, pass the existing unit tests, and still misunderstand the bug report or quietly violate the user's intent. This matters because software teams are starting to rely on AI systems for debugging and repair, and weak verification can create a false sense of correctness in high-stakes settings.

As a continuation of [A new verifier for coding agents](/files/A%20new%20verifier%20for%20coding%20agents.pdf), we are building a multi-layer verification harness that goes beyond standard test-suite evaluation. Our current approach combines static analysis, baseline dynamic testing, and a semantic verification layer driven by the natural-language issue description. More specifically, we extract behavioral claims from issue reports, ground those claims to the parts of the program touched by a patch, and turn them into executable checks. The goal is to ask not only "Does this patch pass the tests?" but also "Does this patch actually do what the issue says it should do?"

One of the main challenges is that issue descriptions are messy, incomplete, and often ambiguous. Important behavioral requirements may be implicit, while generated semantic tests can fail for the wrong reasons because of bad imports, weak fixtures, or brittle assumptions about the repository. Another challenge is balancing practicality with rigor: full formal verification is out of reach for arbitrary software, so the system must combine noisy signals in a way that is still useful in real development workflows. A big part of the ongoing work is therefore an agentic refinement loop that uses execution feedback to improve semantic checks and recover coverage when the first attempt is too weak.

**2. Towards automatizing mathematics**

I am also currently working on the question of how to automate mathematics with AI. This is exciting not only because proving theorems is one of the clearest tests of reasoning, but also because mathematics is full of bottlenecks that are difficult, repetitive, and time-consuming even for experts: exploring examples, generating plausible conjectures, searching for the right proof strategy, and translating informal ideas into rigorous arguments. At the same time, recent progress shows that AI is no longer just a calculator for this domain. Systems such as [AlphaGeometry](https://deepmind.google/blog/alphageometry-an-olympiad-level-ai-system-for-geometry/) and [AlphaProof](https://deepmind.google/blog/ai-solves-imo-problems-at-silver-medal-level/) already solve hard olympiad-style problems, and Terence Tao's [Equational Theories Project](https://terrytao.wordpress.com/2026/03/13/mathematics-distillation-challenge-equational-theories/) has used Lean and automated theorem proving to settle over 22 million formal true-false problems in universal algebra. More recently, AI-assisted systems have even started to resolve individual Erdős problems, such as [Erdős Problem #728](https://arxiv.org/abs/2601.07421). Just as importantly, mathematicians such as [Terence Tao](https://terrytao.wordpress.com/2024/03/17/talks-at-the-jmm/) are actively pushing machine-assisted proof and AI-supported mathematical workflows into mainstream research.

My current plan is to develop an agentic workflow for mathematics with a planner agent, a generator agent, a formalizer agent, and a feedback loop connected to a formal library. In this workflow, the planner proposes directions from a conjecture or research question, the generator produces candidate proof ideas, constructions, or intermediate lemmas, and the formalizer tries to translate those ideas into a form that can be checked against a proof assistant and a formal library. Feedback from failed proof attempts, missing lemmas, and formalization gaps is then fed back into the system so the next round is more informed. The long-term goal is not just to get AI to write polished proofs, but to use it to generate new mathematical insight and then certify that insight rigorously.

 ![agent](/files/agn.png)

The challenges are substantial. Mathematical language is compressed and ambiguous, so translating human intuition into formal objects is hard; long proofs require planning over many steps; and the most valuable breakthroughs often depend on inventing the right concept, not just executing a known technique. There is also a serious evaluation problem: benchmarks are often narrow, or expensive, and success on olympiad-style tasks does not automatically translate into research-level creativity. So the central question is not whether AI can already do some mathematics, but how to build systems that help mathematicians discover genuinely new ideas while preserving rigor, interpretability, and mathematical taste.
