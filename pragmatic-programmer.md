# The Pragmatic Programmer

## Hour 1

Read foreword, (skip "Preface to Second Edition"), read "From the Preface to First Edition" and read "Chapter 1. A Pragmatic Philosophy" (60 mins)

Responsibility/team trust: says "team needs to be able to rely on you" but should also say "team members need to feel team *does* rely on them, i.e. trusts them to do what is right".

Entropy: do no harm, no broken windows

Good enough software

## Hour 2

Read "Chapter 2. A Pragmatic Approach" (75 mins)

DRY is a bad name for a good idea.  It's about "knowledge or intent" *not* about repeated lines of code.

Good design is *that which* is easier to change.

Orthogonality: how does it differ from DRY?

Tracer bullet: is it saying get *something* working end-to-end first?

Domain languages: only use embedded languages: YAML is a case in point.

## Hour 3

Read "Chapter 3. The Basic Tools" (45 mins)

"Each tool will haveits own personality and quirks"  Git!

"The problem with most binary formats is that the context necessary to understand the data is separate from the data itself. You are artificially divorcing the data from its meaning." Is this still true with things like protocol buffers?  The schema is still separate from the data, but that's probably desirable.

"Always Use Version Control"

Branching strategy: There are 'thousands of people out there telling you how you should do it. And that advice is largely meaningless, because what they're really saying is “this is what worked for me.”'

"How long would it take to get [a replacement] machine back to the same state it was in (with all the SSH keys, editor configuration, shell setup, installed applications, and so on)?"

Engineering daybooks: actually I want to keep *less* information, not more.

## Hour 4

Read Chapter 4 (Pragmatic Paranoia) plus Chapter 5 (Bend and Break) intro, Topic 28 Decoupling and Topic 29 Juggling the Real World (65 mins)

"The fact that the routine has a postcondition implies that it will conclude" Hmm, I don't think so!

Must be pretty expensive to check these pre- and post- conditions at run time!

Types can be considered a (very weak) form of pre- and post- conditions that are checked at compile time.

Dynamic contracts sound highly implausible.

Exceptions should be dealt with by the block of code that knows how to deal with them.

Exception antipattern: only things bound before `begin` should be in scope in `finally`!

A finite state machine is just a collection of mutually-tail-recursive functions.

## Hour 5

Read from "Topic 30. Transforming Programming" to the end of Chapter 5 and all of Chapter 6 Concurrency

Transforming programming: basically data pipelines



