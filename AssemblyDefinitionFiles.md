# Assembly Definition Files

Have you ever changed a tiny piece of code and it took years for unity to recompile and be able to start a game? The bigger your project grows, the more time will get wasted by this behaviour but now there is a way to fix that: Assembly Definition files.

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
With assembly definition files you manually split the project into multiple code assemblies. 

TODO

## How to do it?

TODO

## Resources

https://docs.unity3d.com/Manual/ScriptCompilationAssemblyDefinitionFiles.html

https://coffeebraingames.wordpress.com/2018/01/21/reducing-compile-time-in-unity-using-assembly-definition-files/