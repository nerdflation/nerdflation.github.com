---
layout: design-doc
title: Project Engagement Plan
---


### Rationale

The project engagement plan, or PEP, lists the basic parameters of the project.
It is the kernel around which the rest of the design will grow. It describes
*where* you are trying to go with the project and *why*, but not *how* you are
going to get there.

As the project nears completion, the PEP will contain a precise and complete
expression of the project's requirements. As the project begins, however, it
will be necessarily incomplete.  It will capture the lay of the land as seen
from the point of departure -- and for most creative projects of reasonable
scope, it is impossible to create a complete requirements spec at the outset.

It is critical that every part of the PEP is expressed clearly and succinctly,
and it is critical that the client and all members of the design team clearly
understand and agree on every part of the plan.

Like the other design documents, the PEP is a living document and will change
over the course of the project. It should be (a) kept up to date, and (b) used
as the canonical point of synchronization and validation between the client and
design team.


Goal
----------------------------------------------------------------------

Describe the primary goal of the project in very few sentences. If your goal is
too hard to describe succinctly, your project has an excellent chance of
failing.

During the project, you should be able to look at the goal and see if you are
moving towards it or not. At the end of the project, you should be able to look
back at the goal and see whether or not the design you've produced is sufficient
to achieve it.

Unlike the the rest of the PEP -- and indeed the rest of the design documents
you generate -- your goal should remain fairly stable over the life of the
project. It's expected that the other parts of the plan will change over time,
but a change in your goal is Big News.


Desiderata
----------------------------------------------------------------------

List the desirable features and attributes of the project. Desiderata should be
written in list format, with only one or two sentences per item.

This section represents the current, best-known map of your project's
requirements. Whenever you complete an iteration, or acquire new information, or
when the client shifts direction, you and your team should return to this map
and evaluate the new changes in context.

Group the desiderata logically and for ease of navigation, but don't worry if
the grouping seems unstable -- desiderata are generally graph-shaped, not
tree-shaped.

Desiderata can be coarsely prioritized with markers:

- Items marked with **MUST** are required for a satisfactory design.
- Items marked with **SHOULD** are not required for the success of the project,
  but they will likely become MUSTs in later iterations.
- Items marked with **MAY** are nice to have, but their implementation must not
  compromise the design or the delivery schedule.

You can also list desiderata you've considered but rejected, if it will help
you to focus your design efforts.


Constraints
----------------------------------------------------------------------

List the environmental, technological, or political factors that will force
particular design decisions or will force you to do work that you wouldn't
otherwise do.

- Constraints marked **OBSOLETE** no longer apply, due to environmental or other
  changes.
- Constraints marked as **ARTIFICIAL** are those imposed willingly by the design
  team.
- Constraints marked as **MISTAKEN** are those constraints that once were
  thought to be real, but with further examination turned out not to be.

Brooks writes:

> An explicit listing of constraints smokes them out early, avoiding unpleasant
> surprises. It also impresses them on the designer's mind, radically improving
> the chances that he will recognize when one goes away.
>
> One must carefully distinguish:
>
> - Real constraints.
> - Obsolete once-real constraints.
> - Constraints misperceived as real.
> - Intentional artificial constraints.
>
> Since constraints are the designer's friend, if the task originally seems
> unconstrained, first think harder about what is really desired, about the user
> and use models, and you will probably find some narrowing constraints.


Budgeted Resource
----------------------------------------------------------------------

You should explicitly identify the scare resource particular to your project's
design.  This is the primary resource that needs to be budgeted or rationed
throughout the entire design (bandwidth, disk space, latency, schedule days,
etc.).

Another way to think about it: each design or component eats up something
whenever you make a decision. What is that something?

Brooks writes:

> If a design, particularly a team design, is to have conceptual integrity, the
> project manager should:
>
> - Name the scarce resource explicitly.
> - Track it publicly, so that each team member knows the budget.
> - Control it firmly. It is imperative that only one person control budgeting
>   and rebudgeting of the limited resource. (Keep a small reserve of the
>   critical resource for late allocation.)


----------------------------------------------------------------------
Next: [User Model](user-model.html)
