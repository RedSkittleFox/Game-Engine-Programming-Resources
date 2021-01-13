# About This Document
This document should serve as a learning resource and a reference for aspiring game engine programmers. It's focus is game engine programming, not game programming. It's going to cover low level topics such as networking, renderers, entitiy systems and physics engines. The language of interest in this document is C++ thus expect most of the resources use it.

## Usage
This document is not fit for people with basic programming knowledge. Please acquire high level programming language knowledge before using this as a reference. If you are interested in learning C++ please check out [this](https://github.com/RedSkittleFox/Cpp-Learning-Resources) document.

## Contribution and suggestions
Please use issues and create branches to make suggestions and comments.

# Table of Contents
* Memory Management
  * GPU Memory Management
* Rendering
  * Ray Tracing
  * Rendering APIs
    * D3D12
  * Compressed Textures
  * Optimisations
    * Frustrum Culling
    * Precomputed Lighting
* Physics
* Game Logic
  * ECS
  * Concurrency
  * Game Content
    * Maps
* Networking
* Debugging and Developer Tools

# Memory Management
## GPU Memory Management
[*D3D12 Memory Allocator* - GPUOpen-LibrariesAndSDKs](https://github.com/GPUOpen-LibrariesAndSDKs/D3D12MemoryAllocator)

# Rendering
## Rendering
[*Variance Shadow Maps* - NVidia](https://http.download.nvidia.com/developer/presentations/2006/gdc/2006-GDC-Variance-Shadow-Maps.pdf)

## Ray Tracing
[*Ray Tracing - Soft Shadows* - Stack Overflow](https://stackoverflow.com/a/31822904/10266364)
## Rendering APIs
### D3D12
[*Mesh Shaders* - DirectX-Specs](https://microsoft.github.io/DirectX-Specs/d3d/MeshShader.html)

[*DirectX Raytracing* - DirectX-Specs](https://microsoft.github.io/DirectX-Specs/d3d/Raytracing.html)

[*DirectX-Specs*](https://microsoft.github.io/DirectX-Specs/)

## Compressed Textures
[DirectX's Compressed Textures Resources](https://docs.microsoft.com/en-us/windows/win32/direct3d9/compressed-texture-resources)

## Optimisations
[*Performance Guide* - GPUOpen](https://gpuopen.com/performance)

[*The benefits of buffr packing* - ARM Developer](https://developer.arm.com/solutions/graphics-and-gaming/developer-guides/learn-the-basics/the-benefits-of-buffer-packing/attribute-buffer-encoding)
### Frustrum Culling
[*Frustrum Calculation and Culling, Hopefully Demystified* - David Lively](http://davidlively.com/programming/graphics/frustum-calculation-and-culling-hopefully-demystified/)

[*Frustrum Culling tutorial* - Rastertek](https://www.rastertek.com/dx10tut16.html)

### Precomputed Lighting
[*Radiositiy* - Hugo Elias](http://web.archive.org/web/20160311085440/http://freespace.virgin.net/hugo.elias/radiosity/radiosity.htm)

[*Graphics Tech: Precomputed Lighting* - Jonathan Blow](https://web.archive.org/web/20191231233409/http://the-witness.net/news/2010/03/graphics-tech-precomputed-lighting/)

[*Lightmap Parameterization* - Ignacio Castano](http://www.ludicon.com/castano/blog/articles/lightmap-parameterization/)

[*Hemicube Rendering and Integration* - Ignacio Castano](http://www.ludicon.com/castano/blog/articles/hemicube-rendering-and-integration/)

[*Mesh Parameterization* - full-day course given at SIGGRAPH Asia 2007](https://www.inf.usi.ch/hormann/parameterization/index.html)

[*D-Charts: Quasi-Developable Mesh Segmentation* - Dan Julius, Vladislav Kraevoy, Alla Sheffer](http://www.cs.ubc.ca/labs/imager/tr/2005/Vlad_DCharts/)

[*Vector Texture Maps on the GPU* - Nicolas Ray, Thibaut Neiger, Bruno Levy, Xavier Cavin](https://www.researchgate.net/publication/248311661_Vector_texture_maps_on_the_GPU)

[*Lightmap* - Wikipedia](https://en.wikipedia.org/wiki/Lightmap)

[*Packing Lightmaps* - blackspawn](https://blackpawn.com/texts/lightmaps/)


# Physics
## Collision Detection
[*Physics for Game Programmers; Continous Collision* - GDC](https://youtu.be/7_nKOET6zwI)

[*Convx Polygon Collisions* - javidx9](https://youtu.be/7Ik2vowGcU0)

[*GJK Algorithm Explanation & Implementation* - Winterdev](https://youtu.be/MDusDn8oTSE)

[*Handmade Hero Day 050 - Basic Minkowski-based Collision Detection* - Molly Rocket](https://youtu.be/_g8DLrNyVsQ)

## Physics Engines
[*The Fast Fourier Transform (FFT): Most Ingenious Algorithm Ever?* - Reducible](https://youtu.be/h7apO7q16V0)

[*Physics for Game Programmers: Understanding Constraints* - GDC](https://youtu.be/SHinxAhv1ZE)

[*Valve's Physics for Game Programmers* - GDC](https://youtu.be/1RphLzpQiJY)

[*A/B Testing for Game Design Iteration: A Bayesian Approach* - GDC](https://youtu.be/-OfmPhYXrxY)

# Game Logic
## ECS
[*A Simple Entity Component System (ECS) [C++]* - Austin Morlan](https://austinmorlan.com/posts/entity_component_system/)
## Game Contnt
### Maps
[*Valve's BSP Map Format* - VDC](https://developer.valvesoftware.com/wiki/Source_BSP_File_Format)

[*Half-space (geometry)* - Wikipedia](https://en.wikipedia.org/wiki/Half-space_(geometry))

## Concurrency
[*Using Synchronization* - MSDN](https://docs.microsoft.com/en-us/windows/win32/sync/using-synchronization)

# Debugging and Developer Tools
[*Printing Call Stack* - Stack Overflow](https://stackoverflow.com/questions/3899870/print-call-stack-in-c-or-c)

[*Introspections* - TeamHypersomnia](https://github.com/TeamHypersomnia/Introspector-generator)

