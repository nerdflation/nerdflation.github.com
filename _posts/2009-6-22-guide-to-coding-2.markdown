---
title: Guide to Coding, Part 2
layout: post
category: coding
---

### Separate logic code from configuration code

You should be able to separate your code into two groups: code that does stuff,
and code that connects code together. The former should rarely create new object
instances on its own. The latter should never contain any real logic.

### Use dependency injection

If one class requires another class, don't let the first class instantiate the
second class directly. Instead, pass an instance of the second class into the
constructor of the first. If the first class needs many instances of the second
class, pass in a factory.

Using dependency injection will help your code to be modular, reusable, and
testable.

### Make the order of operations irrelevant

A module is much less likely to break if the methods in its classes can be
called in any sequence and still have the intended effect. Try to make methods
do the right thing regardless of the state of the class.

### If order of operations is important, create a controller

If you need operations to happen in a certain order, the best and most robust
way to ensure it is to control the operations from a single method or class
dedicated to that task.

### Limit the scope of mutable elements

Variables, methods, and classes should not be visible to unrelated lines of
code.

### If it's too hard, you're doing it wrong

If you are running into trouble after trouble, sit back and think, "Do I have to
do it this way?. Rethink your approach, the design, and any implicit
requirements you might be adding. Try to identify what applicable skills or
patterns you might be missing that would make it easier.

### Write a spec before writing code

The spec must state what you are trying to achieve, the constraints on the
project, the major components involved, and at least 80% of the product's
behaviors. (The 80% is flexible, depending on the amount of risk and redesign
you are willing to accept.)

The spec is a cheap way to iterate on the hard parts of a design, since it is
easier to change than code. Use the spec to anticipate design troubles. Writing
a spec is hard work, so expect it to take some time.

### Ask the hard, painful-to-answer questions while writing the spec

Be terse, consistent, and precise in the spec. Specify each behavior in just one
or two sentences.

Keep the spec up-to-date as the project evolves. Include a Q&A section in the
spec and record any questions as they arise. The spec needs to be a living
document as long as the project is living. Write the spec so that it is easy to
edit.

### Redesigns are very expensive

Any time you need to redesign a component or feature, you need to make a full
trip through the iterative development cycle. If you don't, you risk the overall
coherence of the project and you have a higher chance of having to redesign yet
again in the future. Check the redesign against the spec, and update both.

### Until you write a spec, coding it is harder than you think

Whatever it is that you're thinking of writing, it is harder and will take
longer than you think. If you are a coder, then you are very good at creating
mental abstractions of complex processes. Unfortunately, those processes are
still complex.

If the spec gets too complicated to understand, then you know the code will be
far worse. Simplify!

### Business + users + technology = requirements

A requirements doc is the thing that tells you what goes into the spec. Any
meaningful set of requirements must take into account the needs of the business,
the needs of the users, and the limits of available technology.

### When starting a new project, never code with more than four engineers.

It is essential for a project to have conceptual coherence, and that is
impossible when more than a handful of contributors attempt to lay the
foundation. All the engineers involved must be in close communication with each
other and have a singular vision for the project.

Coordination and communication become exponentially more costly with the number
of people involved. The design and layout of a new project is always in a high
state of flux at the start, and that level of variability makes coordination a
nightmare and a huge distraction when there are too many people involved.

### Build prototypes

Identify the riskiest and hardest parts of the project, then build
proof-of-concept prototypes for those parts. Incorporate the lessons learned
from those prototypes into the design and code. Prototyping should happen during
the design phase.

"Risky" means anything you're not sure of or don't yet know how to do.

### Write code to be modular and testable

If your code is easily testable, then it is also modular, and vice-versa. The
essential element of both is substitution: each component can easily be replaced
by a different implementation without disturbing the components on the other
side of its interfaces. This is another reason to have simple, easy to implement
interfaces.

### Write unittests

Over half the value of writing unittests comes before you even check the code
in. Unittests can help you squish bugs in the code you've just written, when it
is still fresh and before other code relies on it.

Each test method should cover a single behavior or invariant that you want to
check. There may be multiple test methods per method being tested. The average
length of a test method should be about five lines. It should be easy to see
what a test method is testing. In particular, it should be easy to compare two
test methods to see the difference in what they are testing.

### Use a source control system

Check in your changes frequently. You need to be as familiar with your source
control system as you are with the filesystem. The more comfortable you are with
source control, the more you will be able to make daring changes without risking
your codebase.

### When in doubt, throw it out

Wondering whether or not to keep some complicated feature, some bit of code or
definition "just in case? Toss it. It will be more of a liability than a
benefit. Remember, simplicity is the key to long-term maintainability.

### Keep the bug count low

You may be tempted to check in code that you know is buggy. Resist the
temptation. Buggy code sucks up more and more of your time the older a project
gets. Bugs will impede you as you're writing new code, and older bugs cost
disproportionately more to fix than if they were fixed before the code was
checked in.

### Bugs tend to congregate together

When you find a bug in a feature or in a section of code, there is a high
probability that others are lurking in the same area. When you start finding
many bugs, take a step back and see if a redesign is warranted.

### Limit the scope needed for proper operation

The fewer environmental requirements any class, method, module, or program has,
the easier it is to reuse, maintain, and test. Limiting the connections between
a component and its environment is also called decoupling.

### Pass in the values you need, not the container

When writing a method that needs one or two fields from an object, pass just the
fields you need and not the entire object. The method will be easier to reuse,
maintain, and test.

### Correct is better than fast

Don't optimize code until you know that it does what it is supposed to do.

### Ignore performance problems until you can't

Don't bother to make local optimizations until you measure the performance of
the system as a whole. "When in doubt, use brute force.
