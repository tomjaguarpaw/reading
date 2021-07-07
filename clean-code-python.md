# Clean Code in Python

## Hour 1

Read Preface and Introduction, code formatting and tools

* "Having good intentions doesn't scale"

* "Clean code is not a luxury, it's a necessity"

* "The true nature of clean code depends on other engineers to be able to read and understand it"

* "If you want to move at a steady, constant, and predictable pace, the code needs to be maintainable and readable."

* "Not everything can be caught by automated tools, but whenever it's possible, it's a good investment."

* Only drop clean code standards for code that will definitely be thrown away.

* "when the position was random, the novices did as well as the chess masters; it was just a memorization exercise that anyone could do at reasonably the same level. When the positions followed a logical sequence that might occur in a real game (again, consistency, adhering to a pattern), then the chess masters performed exceedingly better than the rest."

* "we should aim to have as few code comments as possible. That is because our code should be self-documenting."

* "There is, unfortunately, one downside to docstrings, and it is that, as happens with all documentation, it requires manual and constant maintenance."

* `data_from_response`: Writing a function of type `dict -> dict` makes the type annotion almost useless in this case. Improve the type, not the docstring!

* "All of these checks should be automated ... If these checks do not pass, make the build fail."

* Iterating over every character in an email address: I've seen it in practice!

* "it would be wise for the team to agree on a writing convention ... if these rules aren't enforced, they'll get lost over time"

* Rewriting history by running black on every commit seems crazy.

