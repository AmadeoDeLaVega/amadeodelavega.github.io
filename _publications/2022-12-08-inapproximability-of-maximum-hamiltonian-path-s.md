---
title: "Inapproximability of Maximum Hamiltonian Path-S"
collection: publications
category: manuscripts
permalink: /publication/2022-12-08-inapproximability-of-maximum-hamiltonian-path-s
excerpt: 'A paper on why a natural graph-path optimization problem stays hard even if you only ask for a good approximation.'
paperurl: '/files/Inapproximability%20of%20Maximum%20Hamiltonian%20Path-S.pdf'
citation: 'Amadeo De La Vega and Eashwar Sathyamurthy. (2022). &quot;Inapproximability of Maximum Hamiltonian Path-S.&quot; Manuscript.'
---

This project introduces a graph problem that looks simple but is hard to solve, even approximately. Instead of asking for a path that visits every vertex exactly once, it asks for the longest path that must pass through a required set of vertices. The paper shows that even finding a *good approximation* to this problem is computationally hard.

This is a nice example of how ideas from complexity theory connect across topics: boolean formulas, NP-hardness, approximation algorithms, and graph constructions all show up in one place. The core proof builds a chain of reductions starting from 3SAT, giving a concrete look at how theoretical computer science turns logical constraints into structured graph gadgets.
