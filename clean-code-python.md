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

## Hour 2

Read Pythonic Code

* Doesn't give any reason for "Pythonic" idioms.  Contrast with something like "algebra driven design".

* Compare `ContextManager` to [`bracket`](https://www.stackage.org/haddock/lts-18.3/base-4.14.1.0/Control-Exception.html#v:bracket)
"
* `contextlib.contextmanager` is great, but it would be much better if Python supported lambda blocks!

* "we could yield a statement" an *expression* (or perhaps just a value)!

* I very much approve of the functional style of the comprehensions

* Walrus operator `:=` brings tears to my eyes

* `collect_account_ids_from_arns` example should be

  ```
  collect_account_ids_from_arns = mapMaybe $ \arn ->
      case match ARN_REGEX arn of
          Nothing -> Nothing
          Just matched -> groupdict matched "account_id"
  ```

* `_` private properties are a horrible convention

* Command and query separation sounds like a terrible idea, but it seems it has an illustrious history.  Seems like it strongly couples the command and the query.

* Dataclasses are great

* Iterables are a great idea, but with lambda blocks `for` could just become a function.

* `mark_coordinate`: I don't see why it's so helpful to overload `in`.  Just `grid.withinBounds(coord)` seems fine.

* `__call__` is just for syntactic convenience.

* Mutable default arguments: I don't really like default arguments at all.

# Hour 3

Read General Traits of Good Code until Inheritance in Python

* "Some parts of the software we are working on are not meant to be called directly by users". You don't say!

* DbC sounds like just "Have your functions do a particular thing that you can describe"

* "The mechanism for accomplishing this is an exception" "*The*"?  No, just one mechanism.  Errors-as-values is another.

* "exceptions should be used for—clearly announcing an exceptional situation, and not altering the flow of the program according to business logic" Debatable

* "If the code tries to use exceptions to handle expected scenarios or business logic, the flow of the program will become harder to read." Yes. If the code tries to use exceptions for *anything* it will become harder to read.

* ```
  result = condition.holds()
  assert result > 0, f"Error with {result}"
  ```
  
  What?!
  
* "YAGNI" Great idea!

* "KIS"(!) also a great idea!
