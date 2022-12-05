# Test driven development

## Automated testing

Automated testing is the process of writing extra code which tests out
business code. For every part of code we write, we write a set of tests
to correspond to get the expected output. We may also test for predicted
outputs as well as the expected output.

Automatic tests are a safety mechanism. we know that if we pass the
tests, the code is delivering what it is supposed to.

We can also check how much of the code is covered.


## Unit Testing

Unit testing ensures that small sections of code produce the expected
output.

Determining the test to actually do is the most difficult part of unit
tests. Hard to make sure we are capturing all the cases. Requires
additional thought on what the method is doing as well as exceptional
cases.

Unit tests focus on a single "Unit of code". Usually a method but can be
a class.

Should test a single use case.

Isolated from dependencies. Could mock dependencies to sure that they
are called appropriately.

Not everything is suitable for unit tests.

## Tools

As testing has become more common place and required, there are specific
tools to aid with testing.

* Test runner - tool searches for methods in which it knows are tests
  and runs them with a single command.
* Assertion framework - library with methods that make it easy to check
  value type expectations and throws an exception if they are not.
* Mocking framework - creates dummy objects which can be passed into the
  method we are testing.

## Code coverage

The number of lines of code which were executed by tests. Not all line
of code will be covered because some lines depend on external features
or some parts will not be suitable for unit testing.

## Test driven development

Emerged from extreme programming which wanted to move away from the top
heavy design lead practices.

Write tests before writing the code.

Testing driven development can feel process heavy.

TDD helps us to spot mistakes early on.

TDD allows to see incremental improvements constantly which builds
confidence.

Avoids running entire application.

### Advantages

* Bugs are found earlier. Solving the bugs as we are coding. Not
  requiring testing feedback before continuing.
* Incremental improvement means that we do not introduce bloat.
* Tests can also act as documentation
* Results in good code coverage.

### Disadvantage

* More time-consuming due to the specific workflow that must be
  followed.
* Can cause developers to write unnecessary tests for methods that may
  not need to be tested.
  * As well as potentially not enough tests for more complex methods.
* Additional workload to maintaining a test set.
  * Large tests will be difficult to refactor down the road if
    specification changes. Older tests will need to be updated.
* The focus on testing may neglect other aspects of software such as
  security and performance.
