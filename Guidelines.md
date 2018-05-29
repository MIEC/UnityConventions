## General guidelines
Before we start with the hard and nitpicky definitions, here are some general guidelines to enhance the readability of your code.

* Let the code speak for itself
  * Use descriptive names. It might be more complex to think of good names, but descriptive naming can save so much unnecessary documentation.
  * Limit the length of functions. Any coder should be able to grasp the functionality of a function just looking at it. Split complex functions into easier to grasp parts.
* Be SOLID 
  * https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)
  * Components with a size of multiple hundred lines of code most probably can be split into multiple easier to understand components.
* Refactor early
  * Once you notice sections that can be improved through refactoring DO IT. Refactoring early is so much easier than trying to work even more spaghetti code.
* Use some kind of tests
  * Programming games in unity often looks like this: Make a change - Recompile - Play - Wait - Test functionality - Repeat. Depending on what you want to test the procedure takes most of the time. There is stuff that must be playtested, but then there are  features like health bars, damage dealing, serialization, ... that can be tested separately and much faster using automated unit tests.
  
**THERE ARE NO PUBLIC VARIABLES**
Use public properties with or without private backing field.
If you just want to see the variable in the inspector use the [SerializeField] attribute

```
[SerializeField] private bool _theField;

public bool TheField
{
  get{ return _theField; }
  set
  {
    //Skip this if no setter is needed
  }
}
```