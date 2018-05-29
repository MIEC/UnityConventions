# Layout

* 4 Spaces per indentation level
* Curly braces on new lines
    * Except entire statement in block fits in one line
* One statement per line
* One namespace-level class per file
* Methods and property definitions separated by an empty line

```
namespace Examples
{
    public class ExampleClass
    {

        [SerializeField] private bool _backedProp;

        public bool Prop
        {
            get; set;
        }

        public bool BackedProp
        {
            get { return _backedProp; }
            set { _backedProp = value; }
        }

        public void Foo()
        {
            FooBar();
        }

        [ContextMenu("FooBar")]
        public void FooBar()
        {
            while(true)
            {
                // Die
            }
        }

    }
}
```



