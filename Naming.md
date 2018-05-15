The following sections will be heavily focused on how to format your names. In programming there are three main casings:

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


Use meaingful names

## Namespaces

* Pascal Casing

## Classes & Structs

```
public class SomeClass
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

## Exception Classes

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
### Static
`s_goodVariableName`

### Constant
`ConstantVariable`


### Member
`_greatNamingGoingOn`

### Local
`camelIsNotDeadYet`

## Enums
Class and Entries PascalCase


## Naming overview

Type            |Prefix |Casing |Suffix |Example          
----------------|-------|-------|-------|----------
Class           |       |PC     |       |PlayerControls          
Struct          |       |PC     |       |MovementSettings
Interface       |I      |PC     |       |ISkippable
Function        |       |PC     |       |SomeFunction
Property        |       |PC     |       |SomePr
Exception       |       |PC     |Exception|InvalidExampleException
Member Variable |_      |cC     |       |_jumpButton


