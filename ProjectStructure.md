# Project Structure

## Structuring YOUR project

* Grouping by asset type on root level

```
Assets
└─── Scripts
│   │   Posision.cs
│   │   HideSystem.cs
│   │   ...
│   └─── EventSystem
│       │   GestureInputModule.cs
│       │   ...
│   
└─── Textures
    │   ConcreteWall.png
    │   CancreteWallNormal.png
```

## Other Assets
Often a project will contain Assets that are licensed from somewhere else or developed as separate packages. Those assets do not have any dependencies to the project at all, but they will clutter up the project. Altough the new unity package manager solves this problem for many of the unity assets it still remains, this document proposes two ways of handling this issue:

### Using a _Lib folder

Move all the non-core stuff into a separate `_Lib` folder

```
Assets
└─── _Lib
│   └─── GoogleVR
│   └─── Plugins
│   └─── ProCore
│   └─── StandardAssets
│   └─── TextMeshPro
│   
└─── Materials
└─── Models
└─── Scripts
└─── Textures
```

#### Pros
* Separation of project core and other stuff
* No other additional assets or folders in the root (in theory)

#### Cons
* Some Assets don't use relative paths and can't handle being moved
    * They need to stay where they are 


### Using a _Project folder

Move core project into a `_Project` folder

```
Assets
└─── _Project
│   └─── Materials
│   └─── Models
│   └─── Scripts
│   └─── Textures
│   
└─── GoogleVR
└─── Plugins
└─── ProCore
└─── StandardAssets
└─── TextMeshPro
```


#### Pros
* Separation of project core and other stuff
* Assets will definitely work as intended, because they are where meant to be

#### Cons
* Slightly more complex navigation in your assets