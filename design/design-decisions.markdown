---
layout: design-doc
title: Design Decisions
---

<div id="doc-status">Doc Status: DRAFT 15 April 2010</div>


### Rationale

The design team needs to explain and agree on the particulars of the design. The
design needs to be recorded, tracked, and checked against so that the
implementation does not suffer any conceptual skew during construction --
particulary skew due to design decisions being made in isolation.

Remember, this document is meant to be a **map** of the territory, not the
territory itself. You will use it to examine and discuss the major features and
particulars of the territory, especially as they *relate to each other* and to
the problem space. Thus, you will need to balance detail against brevity.


Key Decisions
----------------------------------------------------------------------

List the primary, formative decisions that affect the entire design.


Corollaries
----------------------------------------------------------------------

For each decision, list any corollaries that come as a consequence of it.


Decisions
----------------------------------------------------------------------

List any other design decisions, including corollaries.


Questions
----------------------------------------------------------------------

List open questions that will need to be answered before the design can be
completed.


Simpler Approaches
----------------------------------------------------------------------

List justifications (including any underlying assumptions) for every hint of
complexity in each of the design decisions. If the complexity is not strongly
justified by the desiderata or constraints, then it should be removed.

You should strive to create a design that is as simple as it can be while still
meeting the needs set out in the [PEP][1].

A simple design has several benefits over a more complex one:

- It is easier to implement correctly.
- It is easier to implement at all.
- It is less likely to be misused due to a lack of [comprehensive knowledge][2] of
  its particulars.
- It is easier to extend.
- It is less subject to conceptual drift and shifting requirements.
- It is easier to replace.

At the same time, you need to balance local simplicity against global
simplicity: A design that looks simple in a local scope may in fact be
increasing the global complexity of the system.


----------------------------------------------------------------------
Next: [Iteration Plan](iteration-plan.html)


[1]: http://nerdflation.github.com/design/pep.html
[2]: http://nerdflation.github.com/code.html#design-around-a-compact-core
