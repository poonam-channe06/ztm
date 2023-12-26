# JavaScript is a single threaded programming language.

What does that mean?

Well, being single threaded means that only one set of instructions is executed at a time.It's not doing multiple things. And the biggest way to check that a language is single threaded is, well, it has only one call stack.

This one call stack allows us to run code one at a time.We're never running functions in parallel, as we saw.The stack keeps growing as we push new functions on the stack, and then we pop them one at a time.


## JavaScript is synchronous.

That is one at a time in order that it appears only one thing can happen at the time.

## What probems do we see in the synchronous code ? 

Well with single threaded synchronous code that JavaScript engine runs.

It's going to make it really, really difficult if we have long running tasks.