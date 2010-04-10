---
layout: design-doc
title: Iteration Plan
---

### Rationale

Are you building the right thing? Will your design meet the needs that the
client has expressed? Are the needs that the client has expressed really what
the client needs?

The best, most fitting designs are those grown in the context of a constant,
two-way communication between the designer and client. Get something visible in
front of your client as soon as possible. Get their feedback, and see if the
needs expressed in the engagement plan are still valid, or if revisions and
adjustments are necessary.

Brooks writes:

> Start with *one* or a *few* clear overriding objectives and *schedule
> urgency*. During design and development, balance system *function* against
> *schedule* and *cost*.
>
> Use *schedule urgency* as a defense against requirements creep and design
> bloat.


Iteration Goals
----------------------------------------------------------------------

Each iteration should:

- End at a fixed time.
- Be focused on validating a major design decision, usecase, or open question.
- Deliver some kind of working product (or mock, or simulation).

After seeing the iteration's deliverable, the client may choose to alter the
requirements set forth in the engagement plan.  That's fine as long as you are
making your major course corrections earlier rather than later.

Similarly, an iteration may show the infeasibility of a design decision or the
presence of an unanticipated constraint. Flush these out early, if you can.

After each iteration, your team should reevaluate where you are on the path to
your goal and whether or not any of the decisions or assumptions you've recorded
in your other documents need to change.


Iteration Type
----------------------------------------------------------------------

The goal of the iteration depends on where it occurs in the design's lifecycle.

1. **Sketch** A low-fidelity rendering, done rapidly (e.g., in paper sketches,
   in clickable images, etc.). A visualization of potential design decisions,
   used to communicate with the client.

2. **Prototype** A functioning artifact, crude and massively incomplete, but
   demonstrating one or more major, user-visible desiderata.

    A prototype should be focused on one of these goals:

    - Demonstrating a feature.
    - Proving the viability of some technology.
    - Answering specific *design questions*.
    - Validating specific *desiderata*.
    - Validating specific *design decisions*.

3. **Component** A part of the overall design that is necessary as a
   precondition for other parts of the design.

4. **Spike** A barely functioning product, but one which exercises the entire
   technology stack from input to output. A spike is typically interesting
   only to the design team, not so much to the client.

5. **Alpha** A functioning product, missing major features, but, unlike the
   prototype, built as it will exist in production (i.e., using real
   infrastructure, not throwaway code).

6. **Beta** A functioning product containing all the major features, but not
   yet embodying all desiderata or conforming to all constraints.

7. **Limited release**

8. **Wide release**


Purpose or Goal
----------------------------------------------------------------------

Describe the overriding goal of this iteration, whether it is to validate a
design decision, address a question, etc.


Delivery Schedule
----------------------------------------------------------------------

When will this iteration be completed? Choose a reasonable estimate based on
your goals and knowledge of the design space. If you aren't confident in your
estimate, then your goals for the iteration are probably too broad.


After Action Report
----------------------------------------------------------------------

After the iteration is completed, what are the conclusions? Are you more
certain about anything? Do any of the requirements or design decisions need to
change? What are the implications for the project plan as a whole?


----------------------------------------------------------------------
Next: [Subproject Plan](subproject-plan.html)
