---
layout: design-doc
title: documents for software design and planning
---

These documents are my attempt to systematize an effective iterative development
process using a **navigational** metaphor.


### Basic Assumptions of Iterative Navigation

1. We have imperfect and often inaccurate knowledge of both (a) the problems
   we're trying to solve and (b) the means by which we will try to solve them.

2. The requirements and designs we start with are very likely to change over the
   course of the project as we acquire new information.

3. We need to systematically explore both problem and solution spaces.

4. We need to systematically schedule and track our explorations to provide
   visibility and justification of our efforts.

5. We need to alternate between periods of focused work with a clear, short-term
   goal, and periods of reflection on and reevaluation of the bigger picture and
   our progress toward our goals.

In short, we assume that creating software is like sending a team to explore an
uncharted territory while providing them with only a general idea of a
satisfactory destination.


### The Role of Documentation in Design

Well-structured design and planning documents are like maps in the hands of an
explorer. They let you track where you've been and what you've discovered, and
they help you plan avenues for upcoming expeditions.

Most importantly, they let you observe all the important points of the territory
in one place. When your explorations into avenue *A* tell you that you need to
change your assumptions about *B*, you and your entire team can study all the
implications of that change for *C* through *Z*. Having that information in one
place, visible, shared, and reviewed by the entire team is the best way to avoid
unpleasant surprises and an unnecessary waste of effort.


### Design Documents Are Living Documents

The documents you generate during development should be living, working
documents -- frequently referenced, canonical, and updated when new decisions
are made -- not a set of fixed contracts that are generated, agreed upon, and
cemented prior to construction.

Write the documents so that they can be lived in. They must be readable,
browsable, and editable. They must not contain extra fat, formatting, or
superfluous organization that detracts from those qualities. An unreadable
document is a waste of time.  If the docs aren't evolving over the course of the
project, then there's something wrong with how you're using them.

Treat your design documents as first-class artifacts of the development
process: Use a change-control system, and make sure all design changes get
reviewed and propagated to the entire team.


### Primary Documents

Here is my [Jr. Lightweight Foldable Software Explorer Mapping Kit][1].

1. [Project Engagement Plan](pep.html) &mdash; "Where are we trying
   to go and why?".
2. [User Model](user-model.html) &mdash; "Who is this for?"
3. [Design Decisions](design-decisions.html) &mdash; "How will we get
   there?"
4. [Iteration Plan] (iteration-plan.html) &mdash; "What do we need to do
   next?"


### Supplemental Documents

- [Subproject Plan](subproject-plan.html)
- [Style Guide](style-guide.html)


[1]: http://nerdflation.github.com/design/2010/04/10/design-as-navigation.html
