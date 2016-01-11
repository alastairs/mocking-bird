# Using Test Doubles

## Description

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

## Bootstrapping

Start with an `Expenditure` class that looks like this:

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

To keep things simple (we're focussing on test doubles here, not principles of object orientation), use `double`s and `string`s to represent dates, amounts, etc.

Test your implementation's interactions using all three of the different test double types. Start with Fakes, and pull in a mocking framework only when you feel it will make things easier for you. 

## FAQ

### What are the Test Double types again?

🙈 **Fakes** are hand-rolled test-only implementations of a dependent interface. You completely control everything about this implementation, so you and your tests see no evil. 

🙊 **Mocks** can be used when you want to assert that some method was called. You are verifying their behaviour to ensure your tests speak no evil.

🙉 **Stubs** can be used to specify canned responses to requests that are made to a given dependency. You are stubbing out the wider environment to ensure your tests do not mislead you, that you hear no evil. 
