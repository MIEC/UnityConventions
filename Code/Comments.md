# Comments
***DO***
* use the english language
* write full sentences beginning capitalized and ending with a period
* be precise
* use documentation comments (`///`) where applicable
* write comments in separate lines above the code they comment
* use a space between comment delimiters (`//`, `/*`, `*`) and the comment

***DO NOT***
 * use comments to remove parts of code
 * leave outdated comments in the code

## Documentation comments
Documentation comments are formatted using XML tags. These are processed by the compiler, they can be exported into documentation files and shown in IntelliSense.

Documentation comments can be used on nearly everything except namespaces.

* The `summary` tag should only display the most important information
* Use `remarks`to add additional information to the documentation
* The comments rules from above apply as well

### Types
* Every type should have at least the `summary`documentation
* `summary` should begin with the keywords `Represents`or `Provides`

```
/// <summary>
/// Represents a mesh.
/// </summary>
public class Mesh { }

/// <summary>
/// Provides user input
/// </summary>
public class Input  { }
```

### Methods
* A method documentation should a include `summary` documentation starting with a verb

* 
* Thrown exceptions should be documented using the `exceptions` tag which descrobes the reason why there was an exception 

#### Parameters
* If there are method parameter they should be documented with `param`
* `bool` parameter descriptions begin with `Specifies wether`
* `enum` parameters should be documented with `Specifies ...`

#### Returns
* A return value should be documented using the `returns` tag
* In case of `bool` returns the description should follow the concept of `true if condition; else false`

#### Exception
* If a functions might throw an exception that needs catching it should be documented
* Use the `exception` tag with a reference to the type of an exception and describe why an exception occurred

```
/// <summary>
/// Writes the mesh to a file.
/// </summary>
/// <param name="path">The file system path</param>
/// <param name="overwriteExisting">Specifies whether an existing file will be overwritten</param>
/// <exception cref="ArgumentNullException"><paramref name="path"/> is <see langword="null" />.</exception>
public void WriteMeshToFile(string path, bool overwriteExisting)
{
    ...    
}

```

### Properties
* `summary` documentation stars with `Gets`, `Sets` or `Gets or sets` depending on whether it is read-only, write-only or fully accessible
```
/// <summary>
/// Gets or sets the vertices.
/// </summary>
public Vertex[] Vertices { get; set; }
```


# Resources
* https://docs.microsoft.com/en-gb/dotnet/csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments
* https://blog.rsuter.com/best-practices-for-writing-xml-documentation-phrases-in-c/