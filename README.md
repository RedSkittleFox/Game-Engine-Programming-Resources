# About This Document
This document should serve as a learning resource and a reference for aspiring game engine programmers. It's focus is game engine programming, not game programming. It's going to cover low level topics such as networking, renderers, entitiy systems and physics engines. The language of interest in this document is C++ thus expect most of the resources use it.

## Usage
This document is not fit for people with basic programming knowledge. Please acquire high level programming language knowledge before using this as a reference. If you are interested in learning C++ please check out [this](https://github.com/RedSkittleFox/Cpp-Learning-Resources) document.

## Contribution and suggestions
Please use issues and create branches to make suggestions and comments.

# Table of Contents
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**

- [Memory Management](#memory-management)
  - [GPU Memory Management](#gpu-memory-management)
- [Rendering](#rendering)
  - [Rendering](#rendering-1)
  - [Ray Tracing](#ray-tracing)
  - [Rendering APIs](#rendering-apis)
    - [OpenGL](#opengl)
    - [D3D11](#d3d11)
    - [D3D12](#d3d12)
  - [Optimisations](#optimisations)
    - [Compressed Textures](#compressed-textures)
    - [Occulusion Culling](#occulusion-culling)
    - [Precomputed Lighting](#precomputed-lighting)
- [Physics](#physics)
  - [Collision Detection](#collision-detection)
  - [Physics Engines](#physics-engines)
- [Game Logic](#game-logic)
  - [AI](#ai)
  - [ECS](#ecs)
  - [Game Content](#game-content)
    - [Resource Management](#resource-management)
    - [Maps](#maps)
  - [Concurrency](#concurrency)
    - [Multithreading](#multithreading)
    - [SIMD](#simd)
  - [Misellaneous](#misellaneous)
- [Networking](#networking)
- [Mathematics](#mathematics)
- [Debugging and Developer Tools](#debugging-and-developer-tools)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Memory Management
## GPU Memory Management
[*D3D12 Memory Allocator*](https://github.com/GPUOpen-LibrariesAndSDKs/D3D12MemoryAllocator) - GPUOpen-LibrariesAndSDKs

# Rendering
## Rendering
[*Variance Shadow Maps*](https://http.download.nvidia.com/developer/presentations/2006/gdc/2006-GDC-Variance-Shadow-Maps.pdf) - NVidia

[*Design Patterns for Low-Level Real-Time Rendering*](https://youtu.be/mdPeXJ0eiGc) - CppCon 2017: Nicolas Guillemot

[*Rendering the World of Far Cry 4*](https://youtu.be/rD6KcxcCl_8) - GDC 2015: Stephen McAuley

[*Sand Rendering in Journey*](https://youtu.be/wt2yYnBRD3U) - GDC 2013: John Edwards

[*The Rendering of Below*](https://youtu.be/4D5uX8wL1V8) - GDC 2017: Colin Weick

[*The Physics of Light and Rendering*](https://youtu.be/P6UKhR0T6cs) - QuakeCon 2013: John Carmack

## Ray Tracing
[*Ray Tracing - Soft Shadows*](https://stackoverflow.com/a/31822904/10266364) - Stack Overflow

## Mesh Shaders
[*Turing - Mesh Shaders*](https://youtu.be/72lYVTlPfI8) - SIGGRAPH 2018: Christoph Kubisch

[*Geometry Reinvented with Mesh Shading*](https://youtu.be/rLEbO0Vrzz4) - SIGGRAPH 2019: NVIDIA

[*Advanced Mesh Shaders*](https://youtu.be/0sJ_g-aWriQ) - DirectX Developer Day: Martin Fuller

## Rendering APIs
### OpenGL
[*OpenGL*](https://youtube.com/playlist?list=PLIbUZ3URbL0ESKHrvzXuHjrcLi7gxhBby) - OpenGL Programming Tutorial Series by Brian Will

### D3D11
[*C++ 3D DirectX Programming*](https://youtube.com/playlist?list=PLqCJpWy5Fohd3S7ICFXwUomYW0Wv67pDD) - D3D11 Programming Tutorial Series by ChiliTomatoNoodle

### D3D12
[*Mesh Shaders*](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html) - DirectX-Specs

[*DirectX Raytracing*](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html) - DirectX-Specs

[*DirectX-Specs*](https://microsoft.github.io/DirectX-Specs/)

[*DirectX 12*](https://youtube.com/playlist?list=PLeHvwXyqearWT_NT7CiGm_kEiKabWNPKw) - D3D12 Programming Tutorial Series by Microsoft

## Optimisations
[*Performance Guide*](https://gpuopen.com/performance) - GPUOpen

[*The benefits of buffr packing*](https://developer.arm.com/solutions/graphics-and-gaming/developer-guides/learn-the-basics/the-benefits-of-buffer-packing/attribute-buffer-encoding) - ARM Developer

[*Geometry Caching Optimizations in Halo 5: Guardians*](https://youtu.be/uYAjUOlEgwI) - GDC 2017: Zabir Hoque and Ben Laidlaw

[*Visible Surface Algorithms*](https://youtu.be/hmlWFi1TdbI) - UC Davis Academics

[*Rendering the World of Far Cry 4*](https://youtu.be/rD6KcxcCl_8) - GDC 2015: Stephen McAuley

[*Temporal Reprojection Anti-Aliasing in INSIDE*](https://youtu.be/2XXS5UyNjjU) - GDC 2016: Lasse Jon Fuglsang Pedersen 

## Foliage
[*Between Tech and Art: The Vegetation of Horizon Zero Dawn*](https://youtu.be/wavnKZNSYqU) - GDC 2018: Gilbert Sanders

### Compressed Textures
[DirectX's Compressed Textures Resources](https://docs.microsoft.com/en-us/windows/win32/direct3d9/compressed-texture-resources)

[*DXT is NOT ENOUGH! Advanced texture compression for games*](https://youtu.be/7bJ-D1xXEeg) - GDC 2012: Colt McAnlis

[*Adaptive Virtual Texture Rendering in Far Cry 4*](https://youtu.be/SVPMhGteeuE) - GDC 2015: Ka Chen

[*Virtual Textures (aka Megatextures)*](https://youtu.be/MejJL87yNgI) - GDC 2008: Sean Barrett

### Occulusion Culling
[*Frustrum Calculation and Culling, Hopefully Demystified*](http://davidlively.com/programming/graphics/frustum-calculation-and-culling-hopefully-demystified/) - David Lively

[*Frustrum Culling tutorial*](https://www.rastertek.com/dx10tut16.html) - Rastertek

[*How Occlusion Culling Works*](https://youtube.com/playlist?list=PLEETnX-uPtBVszVeAIDl5jp5j9YT9EFae) - thebennybox

### Precomputed Lighting
[*Radiositiy*](http://web.archive.org/web/20160311085440/http://freespace.virgin.net/hugo.elias/radiosity/radiosity.htm) - Hugo Elias

[*Graphics Tech: Precomputed Lighting*](https://web.archive.org/web/20191231233409/http://the-witness.net/news/2010/03/graphics-tech-precomputed-lighting/) - Jonathan Blow

[*Lightmap Parameterization*](http://www.ludicon.com/castano/blog/articles/lightmap-parameterization/) - Ignacio Castano

[*Hemicube Rendering and Integration*](http://www.ludicon.com/castano/blog/articles/hemicube-rendering-and-integration/) - Ignacio Castano

[*Mesh Parameterization*](https://www.inf.usi.ch/hormann/parameterization/index.html) - full-day course given at SIGGRAPH Asia 2007

[*D-Charts: Quasi-Developable Mesh Segmentation*](http://www.cs.ubc.ca/labs/imager/tr/2005/Vlad_DCharts/) - Dan Julius, Vladislav Kraevoy, Alla Sheffer

[*Vector Texture Maps on the GPU*](https://www.researchgate.net/publication/248311661_Vector_texture_maps_on_the_GPU) - Nicolas Ray, Thibaut Neiger, Bruno Levy, Xavier Cavin

[*Lightmap*](https://en.wikipedia.org/wiki/Lightmap) - Wikipedia

[*Packing Lightmaps*](https://blackpawn.com/texts/lightmaps/) - blackspawn

# Physics
## Collision Detection
[*Physics for Game Programmers; Continous Collision*](https://youtu.be/7_nKOET6zwI) - GDC 2013: Erin Catto

[*Convx Polygon Collisions*](https://youtu.be/7Ik2vowGcU0) - javidx9

[*GJK Algorithm Explanation & Implementation*](https://youtu.be/MDusDn8oTSE) - Winterdev

[*Handmade Hero Day 050 - Basic Minkowski-based Collision Detection*](https://youtu.be/_g8DLrNyVsQ) - Molly Rocket

## Physics Engines
[*The Fast Fourier Transform (FFT): Most Ingenious Algorithm Ever?*](https://youtu.be/h7apO7q16V0) - Reducible

[*Physics for Game Programmers: Understanding Constraints*](https://youtu.be/SHinxAhv1ZE) - GDC 2014: Erin Catto

[*Valve's Physics for Game Programmers*](https://youtu.be/1RphLzpQiJY) - GDC 2014: Sergiy Migdalskiy

[*A/B Testing for Game Design Iteration: A Bayesian Approach*](https://youtu.be/-OfmPhYXrxY) - GDC 2014: Steven Collins 

[*Intro to Game Physics*](https://youtu.be/wPKzwSxyhTI) - 
DigiPen Game Engine Architecture Club

[*Supercharged! Vehicle Physics in Skylanders*](https://youtu.be/Db1AgGavL8E) - GDC 2016: Jan Erik Steel & Patrick Donnelly

[*Designing with Physics: Bend the Physics Engine to Your Will*](https://youtu.be/NwPIoVW65pE) - GDC 2015: Bennett Foddy

[*3D Physics Engine Tutorial* ](https://youtube.com/playlist?list=PLEETnX-uPtBXm1KEr_2zQ6K_0hoGH6JJ0) - thebennybox

[*Destructible Environments in Control: Lessons in Procedural Destruction*](https://youtu.be/kODJsQGXanU) - GDC 2020: Johannes Richter

[*Cloth Self Collision with Predictive Contacts*](https://youtu.be/XUsD3xrNJH0) - GDC 2018: Chris Lewin

# Game Logic
## AI
[*Nuts and Bolts: Modular AI From the Ground Up*](https://youtu.be/IvK0ZlNoxjw) - GDC 2016: Kevin Dill, Christopher Dragert & Troy Humphreys

[*Bringing Hell to Life: AI and Full Body Animation in DOOM*](https://youtu.be/3lO1q8mQrrg) - GDC 2017: Jake Campbell

[*Modular, Reusable Social Behavior In Video Game AI*](https://youtu.be/BSoB19aE9RM) - GDC 2014: Michael Mateas & Bill Ferguson 

[*Creating Complex AI Behavior in Stellaris Through Data-Driven Design*](https://youtu.be/Z5LMUbjyFQM) - GDC 2017: Mehranz Amanat Bari

## ECS
[*A Simple Entity Component System (ECS) [C++]*](https://austinmorlan.com/posts/entity_component_system/) - Austin Morlan

[*Implementation of a multithreaded compile-time ECS in C++14*](https://youtu.be/3N1pLtTV2Uc) - Vittorio Romeo
## Game Content
### Resource Management
[*Pak files - Virtual file system*](https://simoncoenen.com/blog/programming/PakFiles.html) - Simon Coenen

### Maps
[*Valve's BSP Map Format*](https://developer.valvesoftware.com/wiki/Source_BSP_File_Format) - VDC

[*Half-space (geometry)*](https://en.wikipedia.org/wiki/Half-space_(geometry)) - Wikipedia

[*Computational Geometry*](https://www.youtube.com/playlist?list=PLubYOWSl9mIuVdf6VnLIrtF9Y0Sa4Dvoq&pbjreload=102) - Phylip Kindermann

## Concurrency
### Multithreading
[*Using Synchronization*](https://docs.microsoft.com/en-us/windows/win32/sync/using-synchronization) - MSDN
### SIMD
[*SIMD and Vectorization: Parallelism in C++(multitasking on single core)*](https://youtu.be/Pc8DfEyAxzg) - Bisqwit

[*C++ SSE Optimization*](https://youtube.com/playlist?list=PLqCJpWy5FohfwOaELrhGqJlBF14xaSB_Y) - ChiliTomatoNoodle

## Procedural Generation
[*Practical Procedural Generation for Everyone*](https://youtu.be/WumyfLEa6bU) - GDC 2017: Kate Compton

[*Math for Game Programmers: Mixing Geodetic, Hand-crafted and Procedural Geometry*](https://youtu.be/0A4P6MaQxTs) - GDC 2015: Graham Rhodes

## Skeletal Animations
[*IK Rig: Procedural Pose Animation*](https://youtu.be/KLjTU0yKS00) - GDC 2016: Alexander Bereznyak

[*Skeletal Animation - From Theory and Math to Code*](https://youtu.be/ZzMnu3v_MOw) - FloatyMonkey

[*FABRIK (Inverse kinematics)*](https://youtu.be/UNoX65PRehA) - EgoMoose

[*Freeform Animation Rigging: Evolving the Animation Pipeline*](https://youtu.be/XjMKbElVNmg) - GDC 2020: Dave Hunt

[*Bringing Hell to Life: AI and Full Body Animation in DOOM*](https://youtu.be/3lO1q8mQrrg) - GDC 2017: Jake Campbell

# Networking
[*I Shot You First: Networking the Gameplay of Halo: Reach*](https://youtu.be/h47zZrqjgLc) - GDC 2011: David Aldridge

[*Networking for Physics Programmers by Glenn Fiedler*](https://youtu.be/Z9X4lysFr64) - GDC 2015: Glenn Fiedler

# Mathematics
[*The Blaze High Performance Math Library*](https://youtu.be/w-Y22KrMgFE) - Klaus Iglberger

[*Math for Game Programmers: Understanding Homogeneous Coordinates*](https://youtu.be/o1n02xKP138) - GDC 2015: Squirrel Eiserloh

[*Math for Game Programmers: Mixing Geodetic, Hand-crafted and Procedural Geometry*](https://youtu.be/0A4P6MaQxTs) - GDC 2015: Graham Rhodes

# Audio
[*An Interactive Sound Dystopia: Real-Time Audio Processing in NieR:Automata*](https://youtu.be/BrUQdd96qzk) - GDC 2018: Shuji Kohata

[*Performance Based Sound Design*](https://youtu.be/VCJJT4ZuqSg) - GDC 2017: Matt Piersall

[*Next-Gen Audio in Killer Instinct*](https://youtu.be/SPQjOT3gmPY) - GDC 2014: Mick Gordon & Jean-Edouard Miclot 

# Debugging and Developer Tools
[*Printing Call Stack*](https://stackoverflow.com/questions/3899870/print-call-stack-in-c-or-c) - Stack Overflow

[*Introspections*](https://github.com/TeamHypersomnia/Introspector-generator) - TeamHypersomnia

[Frostbite: Implementing a Scripting Solution for Your Editor](https://youtu.be/mxs_x5ne9JY) - GDC 2015: Matthew Doell
