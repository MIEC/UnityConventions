# Naming
The following sections will heavily focus on how to format names in your code. In programming there are three main casings:

* `camelCase`
  * name starts with a lower cased letter
  * concatenated words in the name begin with capital letters
* `PascalCase`
  * name and concatenated words start with capital letters
* `snake_case`
  * every word in the name is written in lower case
  * words are concatenated using underscores
  * not used in C#/.NET

## Naming overview

Is it a non constant variable? -> Some form of camelCase
else: PascalCase

-                |Prefix |Casing |Suffix |Example          
--------------------|-------|-------|-------|----------------------
Class               |       | PC    |       | PlayerControls      
Struct              |       | PC    |       | MovementSettings
Interface           | I     | PC    |       | ISkippable
Enum                |       | PC    |       | Button
Enum values         |       | PC    |       | Jump
Function            |       | PC    |       | SomeFunction
Property            |       | PC    |       | SomeProperty
Member Variable     | _     | cC    |       | _jumpButton
Local Variable      |       | cC    |       | timer
Static Variables    | s_    | cC    |       | s_instance
Constant Variable   |       | PC    |       | Pi

## Acronyms
***DO***
* only use abbreviations if absolutely necessary or commonly known
* capitalize acronyms that consist of only two characters
  * `System.IO`
* follow casing convention for every abbreviation longer than two characters
  * `HttpRequest httpRequest`

## Compound Terms
There are different types of compound words. Take for example `living room`, which is an open compound word, and `railway`, which is a closed compound word and usually is baed on two nouns. Additionally there are hyphenated compound words like `up-to-date` when using compound adjectives before a noun. How do we treat those in regards of capitalization?

***DO NOT*** capitalize each compound in a closed compound word.

***DO*** capitalize compounds in open and hyphenated compound terms.

English     | PascalCase  | camelCase
------------|-------------|-----------
Railway     | Railway     | railway
callback    | Callback    | callback
living room | LivingRoom  | livingRoom
file name   | Filename    | fileName
up-to-date  | UpToDate    | upToDate
long-term   | LongTerm    | longTerm

## Namespaces

***DO***
* follow the rule of `<Company>.(<Product>|<Technology>)[.<Feature>][.<Subnamespace>]`
  * i.e. `Ecg.PingunautenTrainer.StarGazer`
* use Pascal Casing


***DO NOT***
* use same names for namespaces and types



## Types (Classes, Structs, Interfaces, Enums)
The following conventions are defined for all types, specifics of some types are defined in the respective subchapters.

***DO***
* use PascalCase
* use nouns or noun phrases

***DO NOT***
* use generic type names, i.e. `Element`, `Message`
* use common type names, i.e `Stream`, `List`
* use the same type names in different namespaces but same application context
* use the same names for namespaces and types
* prefix classes or abstract classes

***CONSIDER***
* ending types with the name of the derived class
  * i.e. `SerializableAttribute`, `NullReferenceException`, `MyMonoEditor`, `DistanceDrawer`
    * it establishes a clear hierarchical relationship between the types
    * see [List of common type names](https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-classes-structs-and-interfaces)
  * not good: `HeadingEnum`, `CarVehicle` or `WeaponMonoBehaviour`

### Interfaces
***DO***
* prefix a capital `I`
* use noun, noun phrases or adjectives as names
* ensure standard implementation classes have the same name as the interface, differing only by the prefix `I`
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

## Enums
***DO***
* use singular type names for enums
* use plural type names for bit fields/flags enums
* never use `Enum` or `Flags`as suffix

```
// Three logging level presets
public Enum LoggingLevel
{
  Info,
  Warning,
  Error
}

/// Nine possible logging levels, allows logging info & error, but not warnings
[System.Flags]
public Enum LoggingLevels
{
  Info,
  Warning,
  Error  
}
```

## Methods
***DO***
* use pascalCase
* use verbs

## Properties


## Variables
### Member
* camelCase
* Prefix `_`
* `_greatNamingGoingOn`

### Local
*camelCase
* `classicCamelIsNotDeadYet`

### Static
* camelCase
* Prefix `_s`
`s_goodVariableName`

### Constant
* PascalCase
`ConstantVariable`

## Resources

https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-namespaces
https://docs.microsoft.com/en-us/dotnet/standard/design-guidelines/names-of-classes-structs-and-interfaces
