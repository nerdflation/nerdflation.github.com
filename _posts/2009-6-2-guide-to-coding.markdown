---
title: Guide to Coding, Part 1
layout: post
category: coding
---

### Be consistent

Consistency is like compression. It increases your available mental
bandwidth. When writing, use consistent names, consistent formatting, and
consistent coding patterns.

### Be concise

Shorter is better than longer, and thorough is better than incomplete.

### Write for the reader

> Programs must be written for people to read, and only incidentally for
> machines to execute
>
> -- *Abelson, SICP*

The majority of time you spend writing code is actually spent reading. Make your
code as clear as you can, because you and others will be spending a lot of time
wondering what in the world you were thinking.

Treat your reader as if he or she is intelligent but busy, and new to the
area. Act as a local guide to the reader. Show him or her around the
place. Assume the reader is unfamiliar with all the ins and outs of the region,
and take time to explain it (succinctly) in places that he or she is likely to
see.

### Write for the user

Make sure you know that what you're building will be useful and pleasant for
your intended audience. If you discover that you need to change direction, do it
now. It's better to go back to the drawing board now than it is to continue
working on a unfit product and have to go back to the drawing board later.

### Set a goal and measure yourself against it

This is a fractal rule. It applies at every scale of the timeline from years to
a single day. It is important not only to set a goal you can achieve, but to
also specify how you will know when you've achieved it. Goals should be
Specific, Measureable, Achievable, Realistic, and Timely.

### Use the Flow

Flow is a state of heightened concentration and intense productivity. It takes
about ten to fifteen minutes of uninterrupted concentration to get into the
flow, and about two seconds to get knocked out of it. Any type of distration
will do: a ringing phone, checking your email, being asked a question, a shark
attack, etc. Make every effort to reserve and protect at least 30% of your
working hours as flow time.

### Observe and listen

Observation is the heart of creativity and intelligence in all areas and
endeavors.

Sharp observation doesn't mean paying attention to every detail. It means
picking out the important details and paying attention to them, seeing how
things fit together and affect one another. Just watching is not enough; you
have to think as well, and you have to work to incorporate what you see into
your mental model of what is happening.

Observe as much as you can in all areas of life. The most creative people have a
huge and diverse mental library of things they've seen and understood.

### Make mistakes safely

> Success is moving from failure to failure with no loss of enthusiasm
>
> -- *Winston Churchill*

You will learn more from your mistakes than from your successes. You will learn
best from your mistakes if you take the time to examine them and revisit the
decisions you made.

If you are going to make mistakes (and you should), arrange them to soften their
impact. Make your mistakes early on in your projects (and career) and use them
to figure out what you're doing. Make mistakes in mini-projects and use them to
inform the bigger projects.

Successful designs and projects are built on a pile of focused failures, so try
to build that pile as fast as you can. If you aren't making mistakes, you aren't
trying anything new.

### Be clear, not clever

Clarity beats out most other concerns most of the time. Clarity should be your
default metric for code quality. The only time you are allowed to let anything
else trump clarity is when the global picture demands it. Local concerns must
not override the primacy of being clear.

### Design around a compact core

Form your code around foci of compact algorithms or concepts. "Compact" means
that you can fit *all* of its operations into your head at one time. Make sure
the algorithm is complete, clear, and solid. The rest should just be plumbing.

### Keep your designs compact

A compact design has as few operations and conditions as possible, and every
operation in the design conforms to a global, unifying concept.

### Keep your code compact

In compact code, closely related lines of code are also closely located.

If some bit of code has some requirements for its proper operation, the code
that meets those requirements should also be close by.

### Use clear, descriptive names

Call everything by its right name. If you can't find the right name for it, then
you don't know what you're writing. Remember, humans will spend more time
reading your code than compilers ever will.

Don't use abbreviations unless they are well-known. And certainly don't create
abbreviations by dropping all the vowels or other random subset of letters from
the middle of a word.

### Design interfaces to be orthogonal

Orthogonal operations are those which change just one thing without affecting
others. When using an orthogonal interface, you can reorder and recombine
operations without having to worry much about unseen ramifications.

Orthogonal interfaces are always easier to implement and use than non-orthogonal
interfaces.

### Complexity is your enemy, simplicity is your ally

Work hard to keep complexity down. Work especially hard to keep global
complexity down. You can juggle only so much before you start dropping things,
and once you start dropping things, your problems will start cascading.

Complexity will keep cropping up, so be ruthless in weeding it out.

### Put mechanism in code, put policy in config files

When possible, design the program so that its core algorithms can be driven by
configuration files -- what is known as a data-driven design. This can help your
code to be simpler, clearer, and less buggy.

Policy is the part that connects software to the real world. By separating it
from the code and by making it easy to iterate on and edit, you make it easier
to tweak and adjust the policy to fit the real-world requirements. That's the
part that is often the hardest to do and takes the longest time to get right,
anyway.

### Design for organic growth

Organic growth means a constant, piecemeal adjustment to a changing environment,
and a gradual extension of functionality into new areas.

To design for such growth, the design needs to be modular. Modularity means that
the system is constructed as a collection of components connected by
interfaces. Components and their interfaces must be designed so that the
components' implementations can be entirely replaced without disturbing the rest
of the system.

### Design your protocols to be extensible

This includes interfaces between components and on-disk formats for data. An
extensible protocol is one to which additional semantics can be added without
disturbing existing consumers of that protocol.

### Design your protocols to be human-editable

Or at the very least, write good tools so you can easily inspect and edit
them. If you must have a binary format, have a well-defined way to translate it
into plain text and back. Reuse well-known protocols whenever possible (but
don't create surprising differences).

### Write interface comments like road signs

Assume the reader is zipping from one place to another at sixty miles an
hour. Tell them right away whether or not they need to bother with this exit.

### Write comments to answer "why?"

There's no point in telling the reader *what* code is doing unless it is
extremely complex and opaque. It is usually far better to say *why* the code
exists at all.
