---
title: Guide to Coding, Part 3
layout: post
category: coding
---

### Add logging at component boundaries

Log at the beginning and the end of blocking operations and operations that are
likely to break. Log any parameters or results that could help in debugging a
problem. Don't log in the internals of a component, log only at its major
entrance and exit points, and at the points where it interfaces with other
components.

### When in doubt, rethrow the exception

If you're not sure how to handle an exception, just throw it. Eventually it will
reach a layer of code where it is clear how to recover from the fault.

### Create one class per responsibility

Before adding a feature or behavior to a class, ask yourself if that feature
absolutely needs to be tightly integrated with the internals of that class, or
if it can be provided by a separate class. You should be able to describe the
purpose of any class without using the word "and".

A class should be able to say, "That's not my job," and delegate the work to
another class. To connect the classes, use dependency injection.

### Create a single point of truth

Use named constants. Ensure that any decision is always made in the same place
in the code and not in many separate places. In other words, there should be
only one place in the code to find any particular thing.

### Once, twice, automate

If you need to do something a third time, automate it. Write a small program or
shell script, or even write code to generate code if the problem warrants it.

### Once, twice, generalize

If you need to write the same bit of code three times, generalize it into a
reusable component. Don't generalize too soon. Don't copy and paste.

### Reduce the number of conditional statements

Complexity is directly proportional to the number of conditional statements in
the code. Eliminate as many conditionals as you can.

### Separate components by narrow interfaces

A narrow interface is one that contains a minimal number of operations and
carries with it a minimal amount of assumptions. It takes effort to keep an
interface narrow. Before adding an operation to an interface, ask yourself how
hard it would be to add that operation to two separate implementations, each
completely different from the other.

### Shorten the edit-compile-debug cycle

The shorter you can make this cycle, the faster you can develop. Make every
effort to make the build fast. Add scaffolding and support code so that your
programs start as quickly as possible and go directly as possible to the part
you are testing.

If you can use a data-driven design for the difficult parts of your logic, do
so. It will probably be faster to edit and refresh a config file than to edit
and recompile the entire codebase.

### Elegance is utility divided by complexity

An elegant solution is one which exists at a local maximum of that
equation. Elegance is the point at which more is less and less is also less.

### Clean designs come from a messy process

To put it another way, you cannot go from *nothing* to *elegant* without passing
through *complex and messy*. You can't expect to start with a blank slate and
immediately create a design that is new, simple, and effective (or create a
well-structured taxonomy from scratch, or a clean and sensible package
hierarchy).

To create a clean and elegant design, start with quantity. Make a design that
does everything and more. When you get tired of that, sit down and think about
your project's ultimate goals for a while. Keeping those goals firmly in mind,
start pruning things from the design. Cut every feature you can, or merge it
with another. Be ruthless. Pretend that you're on a sinking ship and that you
need to get rid of everything that you don't absolutely need to survive (the
project may start to feel like a sinking ship once you're halfway into it).

Repeat this cycle until you are satisfied. Make sure that everyone involved with
the design knows the phases of the cycle and which phase you are on.

Don't be too afraid to throw it all out and start over. It's better to abandon a
misfit design than to commit a year of your life to it.

### Never rewrite an existing system

You may refactor the existing system and rewrite portions of it to meet your
current needs, or you may write a new system that is intended to compete with
the existing system, but you should never try to recreate the features of an
existing system from the ground up. It will take much longer than you think, you
will trade existing problems for brand-new problems, and the new system will be
missing all sorts of features and environmental adjustments that you never even
knew the old system had.

### Minimize round trip serialization

Serializing on a round trip is slow, especially across networks. Unlike local
optimization, this type of inefficiency exists at the interface level, so it is
difficult to change once the system is in place.

### Code is a liability

The more code you have, the more code you have to maintain and the more bugs you
have to fix. The fastest, most reliable, and most bug-free code is the code that
doesn't exist.

### Break rules with caution

First, make sure you know you *are* breaking a rule, then make sure you know
why. Make sure that your reason for breaking the rule is not the same as the
reason that the rule is there in the first place. Also, don't be lazy.

### Ask Why? five times

When figuring anything out, find the proximal, surface explanation, then dig
deeper to find a root explanation. You should probably stop when you hit
explanations that are too far out of scope, like the reasons for the formation
of the Sun, or anything about electrons really.

### Stand on the shoulders of giants

...and steal their giant hats. Reuse anything you can, including libraries,
designs, patterns, and philosophies. However, when reusing something, make sure
that it really fits your needs and that it can be customized to fit your needs
exactly.

### Simplify

Global complexity is your enemy. It makes your life harder and more
expensive. Try to stamp it out wherever possible. I repeat this because it is
worth repeating.

### There are no big-M Methodologies

There is no such thing as a Methodology that will guarantee success or allow you
to mechanically procede from problem to solution. There is no prescribed
procedure that will let you turn off your brain or let you rely on unreliable
people.

Software engineering is inherently creative, and like all creative endeavours it
requires you to continuously adapt to new situations. The specific things you
did to make the last project successful won't necessarily help with your current
project. You need to adapt to whatever new conditions you face.

Adaptation requires (1) Sharp observation and the ability to see things as they
are, not as you assume them to be, (2) Experimentation, first in the small, then
in the large, and (3) Measurement of results against your expected or desired
outcome.

You have to consciously and continually tailor your approach to the present
situation.

### The 80/20 rule applies

If you have two measurable things and one of them affects the other, there's a
good chance that the 80/20 rule applies. This can work to your advantage (80% of
issues are caused by 20% of the bugs) or to your disadvantage (the last 20% of
the code will take 80% of your time).

### Don't use inheritance if you can avoid it

Inheritance is more fragile, less flexible, harder to test, and harder to reuse
than composition. If you want to share behavior between classes, use
composition. Create a class that implements a particular behavior, then pass an
instance of it to the classes that want to share that behavior.

### Use delegate interfaces in framework code

Use delegates and listener interfaces to give decision-making power to clients
of your framework code. Give the methods in the interface clear and context-free
names.

### Write methods and functions to be orthogonal and composable

Make each method do one thing only. If you need a method to do several things at
once, put each of those things in its own method and tie them together with a
convenience method.

### Stretch goals require a good base of support

Stretch goals can be useful if you can absorb the risk of failure. If you are
embattled and desperate, don't attempt stretch goals. Instead, take the time to
invest in and strengthen your foundations.

### There must be feedback

between everything

### Create software in layers

Launch with a small set of useful layers. Add more layers later to the working
system. Don't try to launch all the layers at once.

### The bigger the project, the more social factors will tend to dominate

As soon as more than one person is involved in a project, social factors will
come into play. Projects succeed or fail because of the humans involved, not the
technology. You should learn how to deal with humans, but that subject is too
big to deal with here.
