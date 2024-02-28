---
title:  Decomposing STL for Safe Planning
subtitle: 
description: A theory for decomposing Signal Temporal Logic Specifications
layout: product
image: ../assets/img/parvproj2.jpg
features:
    - label: Trajectory Planning
      icon: fa-fighter-jet
    - label: Signal Temporal Logic
      icon: fa-code
    - label: Convex Optimisation
      icon: fa-cogs
---

Trajectory planning is a critical process that enables au-
tonomous systems to safely navigate complex environments. Signal tem-
poral logic (STL) specifications are an effective way to encode complex
temporally extended objectives for trajectory planning in cyber-physical
systems (CPS). However, planning from these specifications using exist-
ing techniques scale exponentially with the number of nested operators
and the horizon of specification. Additionally, performance is exacerbated
at runtime due to limited computational budgets and compounding mod-
eling errors. Decomposing a complex specification into smaller subtasks
and incrementally planning for them can remedy these issues. In this
work, we present a way to decompose STL requirements temporally to
improve planning efficiency and performance. The key insight in our work
is to encode all specifications as a set of reachability and invariance con-
straints and scheduling these constraints sequentially at runtime. Our
proposed technique outperforms the state-of-the-art trajectory synthesis
techniques for both linear and non linear dynamical systems. 