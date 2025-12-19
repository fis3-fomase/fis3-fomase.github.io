---
title: Project Details
#view: compact # Listing view
---

Here we provide some detailed information about the project FoMaSE (Foundations of Macroprogramming-based Software Engineering).

{{<toc>}}

## FoMaSE Project Abstract

*The Foundations for Macro-programming-based Software Engineering (FoMaSE) basic research project aims to address the long-standing micro-macro link problem by the computer science and software engineering (SE) viewpoints: how to effectively engineer the software driving the micro-level computational parts of a system so that these collectively produce the designer’s intended macro-level behaviour (and how that intention could be specified)? On this, previous research on multi-agent (MAS) and collective adaptive systems (CAS) showed that domain-specific paradigms and “macro-level” abstractions (e.g., organisational, choreographical, and aggregate programming) can support analysis and development of software driving, e.g., robot swarms and Internet of Things systems. What is missing is a general theoretical and methodological framework for “macro-programming”, able to connect source code and computations to fundamental scientific principles on emergence, coarse-graining, and multi-scale dynamics, and to support systematic design of the micro-macro link. Concurrently, artificial intelligence (AI)-based methods like multi-agent reinforcement and evolutionary learning, often used for automatic design of swarm controllers, tend to suffer from issues like those on scalability, interpretability, and reward/fitness design. FoMaSE aims to fill these crucial gaps, by linking recent insights from physics on the discovery of emergent phenomena to the realm of programming languages and SE, and exploiting coarse-grained “macro-programs” to mitigate issues in AI-based design. Specifically, FoMaSE aims to provide: (i) novel formalisations of collective computation and macro-programming; (ii) innovative scalable methods for testing and analysis of software systems exhibiting emergent multi-scale dynamics; (iii) integrative macro-programming languages and hybrid AI-based methods supporting understanding, development, interpretability, and validation of the target micro-macro link. Conceptual and methodological tools emerging from FoMaSE are expected to open new research directions on “software engineering for multi-scale dynamics and artificial collective intelligence”, fostering a virtuous cross-disciplinary synergy among SE, computer, and complex systems science.*

## History and background

Term **[macro-programming](https://en.wikipedia.org/wiki/Macroprogramming)** was introduced in early 2000s in the context of programming paradigms for wireless sensor networks (WSN).

{{< callout note >}}In basically all the research papers, term macro-programming was always introduced informally and in limited extent.{{< /callout >}}

{{< callout note >}}By a terminological perspective, macro-programming appears to recall "macros" (the technique for symbolic substitution in programs); however, it actually refers to **"macroscopic"**.{{< /callout >}}

The notion was never addressed directly and in explicitly terms, until two surveys that emerged in 2021/2022, one of which from the FoMaSE principal investigator:

- **[Macroprogramming: Concepts, State of the Art, and Opportunities of Macroscopic Behaviour Modelling (Roberto Casadei, 2023, ACMSUR)](https://doi.org/10.1145/3579353) (see also the [longer arXiv version](https://doi.org/10.48550/arXiv.2201.03473) in 2022)**
- Macroprogramming in the internet of things: A systematic mapping study (Santana et al., 2021, SBCUP)

Conceptually, macro-programming is related to (at least) three broad areas:

* **multi-agent systems (MAS)**, including normative MAS, organisational paradigms, holonic MAS, etc.
* **distributed systems**, including service computing (e.g., choreographies), WSNs, etc.
* **collective adaptive systems (CAS)**, including **self-organisation/swarm programming**, [aggregate computing]() (cf. spatial computing, amorphous computing)

{{< callout note >}}The **micro-macro link** is a long-standing issue in MAS research, as well as in "complexity science" threads (e.g., study of emergent phenomena).{{< /callout >}}


However, the idea of *macro-programming* is more specific than what you normally find in those areas.
In some way, the idea is of programming the overall collective behaviour of a computational system (possibly distributed) using denotations of macroscopic entities or outcomes.
So, conceptually, the entire distributed computational ensemble is the "single machine" that you program against.

{{< callout note >}}Macro-programming appears to entail a **macro-to-micro** directionality: the program talks about macroscopic aspects, and micro-level behaviour is induced in turn.{{< /callout >}}

What are the benefits of macro-programming? Intuitively, you get a simplified, coarse-grained description of a collective behaviour. Of course, when talking about Turing-equivalent programming paradigms, it is a matter of practical expressiveness and the benefits related to program understanding, maintainability, and so on.

## Related projects

- [COMMON-WEARS: COMMunity-OrieNted WEARrable Computing Systems](https://common-wears.github.io/2022/consortium/) (2022-2025)
- [Fluidware](https://fluidware-project.github.io/consortium/) (2019-2023)


## Selected Bibliography

For project FoMaSE papers, see the [corresponding Publications page](/publication).

### Main papers

{{<cite page="/publication/casadei-2023-acmsur-macro" view="4">}}
{{<cite page="/publication/casadei-2025-tosem" view="4">}}
{{<cite page="/publication/casadei-2023-artl-ci-survey" view="4">}}

### Recent papers

{{<cite page="/publication/aguzzi-2025-lmcs-macroswarm" view="4">}}
{{<cite page="/publication/dblp-confacsos-farabegoli-vc-24" view="4">}}
{{<cite page="/publication/casadei-2024-ppdp-ac-declarativity" view="4">}}
{{<cite page="/publication/casadei-2023-frasp" view="4">}}

### Historical papers

{{<cite page="/publication/newton-2004-region-streams" view="4">}}
{{<cite page="/publication/sawyer-2003-micromacrolink" view="4">}}



<!-- {{< icon name="github" pack="fab" >}} -->

