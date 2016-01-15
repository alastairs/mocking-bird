# Contract and Collaboration tests

We will use the same expense-tracking application as in the [Test Doubles](https://github.com/alastairs/mocking-bird/blob/test-doubles/test-doubles/README.md)
exercise.

Start over with a new pair, and be sure to use test-first development this time (even if you didn't last time). You don't have to fully
respect the TDD process of red-green-refactor, but do ensure you write your tests first so you define your collaborations and contracts
before implementing them.

## Description

Use [Contract](#contract-tests) and [Collaboration](#collaboration-tests) tests to test the integration between the different moving
parts. Try to avoid [header interfaces](http://martinfowler.com/bliki/HeaderInterface.html) and prefer instead
[role interfaces](http://martinfowler.com/bliki/RoleInterface.html): this will keep your design clean, making the tests easier to write,
and will help you avoid the [interface-implementation pair antipattern](http://martinfowler.com/bliki/InterfaceImplementationPair.html).

### System specification

Create a simple spend-tracking application that can:

  - Record spending on an ad-hoc basis
  - Display a summary of your spend
  
The summary should state:

```
> DATE       | AMOUNT SPENT | CATEGORY         | TOTAL  
> -----------+--------------+------------------+---------
> 2016-01-10 |       £35.83 | Groceries        | £226.79 
> 2015-12-21 |       £56.00 | Car:Fuel         | £190.96
> 2015-12-05 |      £134.96 | Gifts: Christmas | £134.96
```

### Bootstrapping

As before, start with an `Expenditure` class that looks like this:

```csharp
public class Expenditure
{
    public void Record(double amount)
    {
    
    }
  
    public void Summarise()
    {
    
    }
}
```

**Note: You may not add any more public methods to the Expenditure class during this exercise.**

To keep things simple (we're focussing on the tests here, not principles of object orientation), use `double`s and `string`s to represent dates, amounts, etc.

## Recap

### Collaboration tests

Use mocks and stubs to verify your collaborations with your interfaces. Mocks are for verifying a method was called, and was called
correctly; stubs are for returning expected results from your interfaces. 

### Contract tests

Here you need to verify that your implementation adheres to the contract of the interface. Write your contract tests first, and don't
forget to test any fakes you write with the same contract tests. (Remember the Template Method trick.)
