# Layout

* Use 4 Spaces per indentation level
* Curly braces on new lines
    * Exception: Entire statement in block fits in one line
* One statement per line
* One namespace-level class per file
* File name correspond to class names contained in file
* Methods and propery definitions are separated by an empty line

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



