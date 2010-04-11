---
layout: design-doc
title: Iteration Plan
---

### Rationale

Are you building the right thing? Will your design meet the needs that the
client has expressed? Are the needs that the client has expressed really what
the client needs? Will the technology you've chosen even work, or will it fall
apart under stress like so much cheap junk?

Those questions are hard, even impossible, to answer at the outset of many
projects.

If you naively assume that you can start building a production-worthy system in
*technology order* (that is, by building the technology stack from the top-down
or from the bottom-up) then you are likely to run into a situation where you
will have to throw away a lot of work -- including much of the effort you've put
into maintaining a good design style, production-worthy qualities, and
conceptual integrity -- when you uncover new information or when requirements
change. Two words come to my mind when I think about throwing away a lot of hard
work due to shifting requirements or avoidable design mistakes: *expensive* and
*demoralizing*.

You should instead design and build the project in *information order* (a.k.a
*risk order*). Plan your efforts to flesh out requirements, weed out design
issues, prove design concepts, and generally increase your confidence that where
you think you're going is in fact where you should be going.

The iteration plan is a tool to help your team do just that:

1. It is the formal expression of your team's plan to explore requirements space
   and solution space.

2. It is a scheduling tool that you can use to determine about when you will
   have a better idea of (a) the scope of the project, and (b) how long the
   project will take.

3. It is plan and reminder to *maximize* the amount and accuracy of relevant
   information you gather *earlier* in the project in order to *minimize* the
   risk of expensive changes later in the project.

The best, most fitting designs are those grown in the context of a constant,
two-way communication between the design team and the client. Get something
visible in front of your client as soon as possible. Get their feedback, and see
if the needs expressed in the [PEP][1] are still valid, or if revisions and
adjustments are necessary.

Brooks writes:

> Start with *one* or a *few* clear overriding objectives and *schedule
> urgency*. During design and development, balance system *function* against
> *schedule* and *cost*.
>
> Use *schedule urgency* as a defense against requirements creep and design
> bloat.


Questions to Validate
----------------------------------------------------------------------

List out the requirements, features, decisions, and questions that are the most
important to clarify, validate, or answer.  List them in their order of
importance: a question that has a larger effect on the direction or nature of
the project should be answered before others.


A Single Iteration
----------------------------------------------------------------------

For each iteration, list:

- Its [type](#iteration-type).
- Its [goal](#purpose-or-goal).
- Its [expected schedule](#delivery-schedule).
- Any information gathered as a [result](#after-action-report)

Each iteration should:

- End at a fixed time.
- Be focused on validating a major design decision, usecase, or open question.
- Deliver some kind of working product (or mock, or simulation).

After seeing the iteration's deliverable, the client may choose to alter the
requirements set forth in the [PEP][1].  That's fine as long as you are making
your major course corrections earlier rather than later.

Similarly, an iteration may show the infeasibility of a design decision or the
presence of an unanticipated constraint. Flush these out early, if you can.

After each iteration, your team should reevaluate where you are on the path to
your goal and whether or not any of the decisions or assumptions you've recorded
in your other documents need to change.

Don't list the entire lifecycle of the project to begin with. You will create
plans for more iterations as the project continues and as you construct clearer
picture of the problem and design spaces.

Do state the implications of a series of iterations: What will you know at
such-and-such a point? What will you have delivered?


Iteration Type
----------------------------------------------------------------------

The goal of the iteration depends on where it occurs in the design's lifecycle.

1. **Sketch** A low-fidelity rendering, done rapidly (e.g., in paper sketches,
   in clickable images, etc.). A visualization of potential design decisions,
   used to communicate with the client.

2. **Prototype** A functioning artifact, crude and massively incomplete, built
   to throw away, but demonstrating one or more major, user-visible desiderata.

    A prototype should be focused on one of these goals:

    - Demonstrating a feature.
    - Proving the viability of some technology.
    - Answering specific *design questions*.
    - Validating specific *desiderata*.
    - Validating specific *design decisions*.

3. **Component** A part of the overall design that is a necessary precondition
   of other parts of the design, built at production quality. You should try to
   minimize the number of component iterations, especially early in the project
   when there is a high degree of uncertainty.

4. **Spike** A barely functioning product, but one which exercises the entire
   technology stack from end-to-end. A spike is typically interesting only to
   the design team, not so much to the client.

5. **Alpha** A functioning product, missing major features, but, unlike the
   prototype, built as it will exist in production (i.e., using real
   infrastructure, not throwaway code).

6. **Beta** A functioning product containing all the major features, but not
   yet embodying all desiderata or conforming to all constraints.

7. **Wide release** If you get here, congratulations. This project is complete
   as far as the PEP is concerned. You now enter into the phases of maintanance
   and extention, with each extension having its own PEP and set of designs and
   requirements. Incidentally, this is where the effort and expense it takes to
   create a design with [conceptual integrity][2] really starts to pay off.


Purpose or Goal
----------------------------------------------------------------------

Describe the overriding goal of this iteration, whether it is to validate a
design decision, address a question, etc.


Delivery Schedule
----------------------------------------------------------------------

When will this iteration be completed? Choose a reasonable estimate based on
your goals and knowledge of the design space. If you aren't confident in your
estimate, then your goals for the iteration are probably too broad. Most
iterations should last a week or two -- any longer and you risk wasting work,
since the less frequently you correct your course, the more opportunity you will
have to drift off track.

If you are at all uncertain about the schedule for an iteration, state as
much. It is best to make it clear that there is a lack of clarity.

You can schedule multiple iterations concurrently, if it makes sense to do so
and you have enough people to do the work. (In fact, a pipelined iteration may
be an excellent way to start training up more junior members of the team: they
can work somewhat independently, but their work will receive formal review every
one or two weeks. Meantime, the rest of the project can proceed apace.)


After Action Report
----------------------------------------------------------------------

After the iteration is completed, what are the conclusions? Are you more
certain about anything? Do any of the requirements or design decisions need to
change? What are the implications for the project plan as a whole?


----------------------------------------------------------------------
Next: [Subproject Plan](subproject-plan.html)

[1]: http://nerdflation.github.com/design/pep.html
[2]: http://nerdflation.github.com/design/2010/04/06/design-of-design.html
