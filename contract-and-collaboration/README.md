# Contract and Collaboration tests

We will use the same expense-tracking application as in the [Test Doubles](https://github.com/alastairs/mocking-bird/blob/contract-and-collaboration/test-doubles/README.md)
exercise. 

Start over with a new pair, and be sure to use test-first development this time (even if you didn't last time). You don't have to fully
respect the TDD process of red-green-refactor, but do ensure you write your tests first so you define your collaborations and contracts
before implementing them.

## Recap
### Collaboration tests

Use mocks and stubs to verify your collaborations with your interfaces. Mocks are for verifying a method was called, and was called
correctly; stubs are for returning expected results from your interfaces. 

### Contract tests

Here you need to verify that your implementation adheres to the contract of the interface. Write your contract tests first, and don't
forget to test any fakes you write with the same contract tests. (Remember the Template Method trick.)
