# Formatting

This chapter focusses code formatting.

* 4 Spaces per indentation level
* Curly braces on new lines
    * Exception: Entire statement in block fits in one line

Example property:
```
public bool Value
{
    get{ return true; }
    set
    {
        SomeFunction();
        _value = value;
    }
}

```


ONE TYPE PER FILE
FILE NAMES ACCORDING TO CLASSNAME