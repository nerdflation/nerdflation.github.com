---
layout: post
title: Guide to Coding, Part 4
category: coding
---

This one is Java-specific in its terminology, but the principles apply to OO
languages in general.


### Exceptions are part of the API

If you are creating a component, or module, or something that exports an API,
you should define a specific exception type as part of the API. Don't leak
internal details in the form of implementation-specific exceptions. Instead,
catch and and wrap any exceptions that your caller doesn't need to know about.

Bad:

    public void doFoo() throws FrobComponentException, IOException {
      useFrobBallast();     // throws FrobComponentException
      writeResultsToLog();  // throws IOException
    }

Good:

    public void doFoo() throws FooException {
      try {
        useFrobBallast();
      } catch (FrobComponentException e) {
        throw FooException.wrap(e, context);
      }
      writeResultsToLog();  // Rewritten to throw FooException, not IO
    }


### Use checked exceptions for boundary and IO errors

Throw a checked exception to indicate that the program encountered bad user
input, a broken subsystem, a corrupted file, or other environmental flaw.  That
is, throw a checked exception when the problem is with the environment outside
your code, and not within your code itself.

Checked exceptions should be something that you intentionally create as a part
of the contract of a correctly-coded and correctly-behaving module.


### Use unchecked exceptions for programmer errors

Throw an unchecked exception to indicate that there is a flaw in the code, not
necessarily in the environment. Examples are array-index exceptions, objects
being used before they are initialized, and other contract-breaking situations
caused by a mistake in the code.

Tag the exception with any data that might help you to track down its cause.


### Avoid subclassing

Subclassing gets in the way of reuse and expandability. It is generally more
fragile and harder to design right than the alternatives listed below.  You
*can* devise an inheritance hierarchy that correctly captures a problem, but in
many cases the odds are against you designing it right the first time around,
especially as requirements change.


### Avoid subclassing: To share behavior, use composition

Composition means that you wrap the desired behavior into a reusable class,
which the erstwhile subclass then uses as needed.  Instead of:

    // Subclass BAD

    class Base {
      int x = 0;
      void increment() { x++; }
    }

    class Sub extends Base {
      void say() {
        increment();
        Log.info("Now at %s", x);
      }
    }

...put the desired behavior into a composable component:

    // Composition GOOOD

    class Component {
      int x;
      void Component(int start) { x = start; }
      void increment() { x++; }
      int getX() { return x; }
    }

    class Use {
      Component c = new Component(0);
      void say() {
        c.increment();
        Log.info("Now at %s", c.getX());
      }
    }

This pattern is easy to use and gives your code flexibility, since mixing,
remixing, and replacing components is easier than mixing subclasses.


### Avoid subclassing: To share identity, use interfaces

When all you want is to be able to treat a bunch of different classes the same
way, then refer to instances via an interface, not a base class.


### Avoid subclassing, except when you can't possibly avoid it

*Sometimes* subclassing is the best, most flexible, and most appropriate way to
solve a problem.  One example is when you want to create a sort of miniature
domain-specific-language for subclass implementers to use. Another is when the
inherited implemetations of each subclass absolutely must be identical (although
even in that case, it may be better for subclassers to inject the desired
behavior via a delegate rather than to subclass).


