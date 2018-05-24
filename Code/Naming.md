The following sections will heavily on how to format names in your code. In programming there are three main casings:

* camelCase
  * name starts with a lower cased letter
  * concatenated words in the name begin with captial letters
* PascalCase
  * name and concatenated words start with capital letters
* snake_case
  * every word in the name is written in lower case
  * words are concatenated using underscores
  * not used in C#/.NET

## Acronyms
* Use PascalCase or camelCase for acronyms based on the convention for names longer than two characters
  * `HttpRequest`
* Capitalize acronyms that consist of only two characters
  * `System.IO`
* Only use abbreviations if absolutely necessary or commonly known

## Namespaces

* Pascal Casing

## Classes

```
public class SomeClass
{
  //...
}
```

## Structs

```
public struct Key
{
  //...
}
```


### Exceptions
There are a few Exception to this rule.

* Exceptions usually are suffixed with the `Exception` keyword, ie. `NullReferenceException`
* Custom Editors end with `Editor`
* Property drawers end with `Drawer`
* Attributes have the suffic `Attribute`

## Abstract classes

* Like Classes
* Don't use any "abstract" or "base", etc.. keywords


## Interfaces
* Prefixed by a capital `I`
* PascalCase
* Name should be noun or adjective

```
interface ISelectable 
{
  //Objects of this type can be selected
}

interface ICollection
{
  //Objects of this type are collections, ie. list, sets, queue, ...
}
```
## Functions

## Properties

## Variables

### Public

**THERE ARE NO PUBLIC VARIABLES**
Use public properties with or without private backing field.
If you just want to see the varaible in the inspector use the [SerializeField] attribute

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

### Static
`s_goodVariableName`

### Constant
`ConstantVariable`


### Member
`_greatNamingGoingOn`

### Local
`camelIsNotDeadYet`

## Enums
* Class and Entries PascalCase
* Singular naming
  * i.e. `Finger`, not `Fingers`

```
public Enum Heading
{
  North,
  East,
  South,
  West
}
```


## Compound Terms
There are different types of compund words. Take for example `living room`, which is an open compund word, and `railway`, which is a closed compund word and usually is baed on two nouns. Additionally there are hyphenated compound words like `up-to-date` when using compud adjectives before a noun. How do we treat those in regards of capitalization?

*Do not* capitalize each coumpound in a closed compound word.
*Do* capitalize compund in open and hyphenated compound terms.

English | Pascal  | camel
---------------------------
living room | LivingRoom  | livingRoom
file name   | Filename    | fileName

railway     | Railway     | railway
metadata    | Bitflag     | bitflag
callback    | Callback    | callback

up-to-date  | UpToDate    | upToDate
long-term   | LongTerm    | longTerm



## Naming overview

Is it public? PascalCase
Is it a variable? camelCase
Else: PascalCase

Type            |Prefix |Casing |Suffix |Example          
----------------|-------|-------|-------|----------
Class           |       |PC     |       |PlayerControls      
Struct          |       |PC     |       |MovementSettings
Interface       |I      |PC     |       |ISkippable
Function        |       |PC     |       |SomeFunction
Property        |       |PC     |       |SomeProperty
Member Variable |_      |cC     |       |_jumpButton
Local Variable  |       |cC     |       |timer
Static Variables|s_     |cC     |       |s_instance


USE JUST ONE LANGUANGE