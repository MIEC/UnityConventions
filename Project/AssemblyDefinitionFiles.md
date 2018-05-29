# Assembly Definition Files

Have you ever changed a tiny piece of code and it took years for unity to recompile and be able to start a game? The bigger your project grows, the more time will get wasted by this behaviour. But now there is a way to fix that: Assembly Definition files.

### Pros
* Faster compilation & reloading
* Enforced code dependencies

### Cons
* Needs to be structured by hand
* IDE start time may increase due to many projects

## Background
The usual Unity project from a code perspective looks like this:

IMAGE HERE

Basically you have once single assembly containing all the code in your project. But there are two, right? The second assembly contains all editor scripts, which are stripped from the main assembly.

Now imagine you include this cool pathfinding assets with tons of code into the project. It will be part of the same assembly and therefore it will be included in the recompile of changes you make on ui or whatever else code. This increases compilation and reloading time.

## How do asmdefs work?
With assembly definition files you manually define which scripts are part of an assembly, you basically split the project into multiple code assemblies. 

Scripts in other assembly must explicitly be referenced by referencing the assembly you wish to use in the assembly definition file. That way unity knows how the assemblies depend on each other and can optimize when recompiling.

Let's say we have the assemblies asm1, asm2 and asm3 where asm2 references asm1.
If there is a change in any script in asm1 the entire assembly will be recompiled and reloaded. asm2 has a reference to asm1 and has to bei reloaded as well.
If I make a change in asm3 the other two will not be recompiled and reloaded, since they do not reference the asm3 asssembly.

PIC HERE

## How to do it?

TODO


## Should I bother?
YES. Assembly definition files were integrated very recently and most assets from the AssetStore do not make use of them by default. Adaption will grow rapidly within 2018.

## Resources

https://docs.unity3d.com/Manual/ScriptCompilationAssemblyDefinitionFiles.html

https://coffeebraingames.wordpress.com/2018/01/21/reducing-compile-time-in-unity-using-assembly-definition-files/