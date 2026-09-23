---
title: Macroscopic Design of Swarms with Collective State Machines
authors:
- Gianluca Aguzzi
- Giorgio Audrito
- Roberto Girau
- Gianluca Torta
- Roberto Casadei
date: '2026-01-01'
publishDate: '2026-09-23T11:36:21.808850Z'
publication_types:
- chapter
publication: '*Computational Collective Intelligence*'
doi: 10.1007/978-3-032-36868-3_28
links:
- name: URL
  url: http://dx.doi.org/10.1007/978-3-032-36868-3_28
tags:
- fomase
---

Key links

- **[paper presentation @ ICCCI'26 at /talk-2026-iccci-fsm/](https://fis3-fomase.github.io/talk-2026-iccci-fsm/)**
- **[GitHub repository of experiments: experiments-2025-collective-state-machines](https://github.com/cric96/experiments-2025-collective-state-machines)**

## Abstract

Promoting collective intelligence in artificial collectives, such as robot swarms, is complex and generally addressed with different methods ranging from machine learning to dynamic control. In particular, macro-programming approaches like aggregate computing tackle selforganising spatiotemporal formation and distributed information processing using ad-hoc computational models and domain-specific languages (DSLs) following a macroscopic perspective. However, these approaches come with limited support for (i) effectively specifying the collective phases of a mission, and (ii) ensuring that the collective quickly and consistently reaches an agreement on the collective task to be carried out. To address this, our work proposes the novel notion of collective finite state machines (cFSM), where states and links denote collective tasks and agreements on collective strategy evolution, respectively.
Specifically, we provide a general formal characterisation of the approach on event structures, and develop a linguistic implementation in terms of a new DSL layer over the ScaFi aggregate programming language. We also show that our design provides formal guarantees on collective agreement, and its implementation, tested on a swarm robotics case study, is correct, withstands perturbations, and works with bounded memory.