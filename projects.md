---
layout: page
title:  "Projects"
categories: projects
---

* TOC
{:toc}

## Current
### [Ilya](https://github.com/Epsylene/Ilya)
![Ilya](/assets/images/ilya.png)

Simple raytracer based on the [Ray Tracing in One Weekend](https://raytracing.github.io/) series, written in C++. 

Features include:
- Ray-sphere, ray-quad intersection
- Lambertian diffusion
- Specular reflections
- Transparent materials
- Emissive materials
- Isotropic media
- Color/image textures
- Perlin noise textures
- BVH acceleration structure
- Instancing
- Importance sampling
- Next-neighbour resampling
- Defocus blur

### [caliban](https://github.com/Epsylene/caliban)
![caliban](/assets/images/caliban.png)

Implementation of the [Rust Vulkan tutorial](https://kylemayes.github.io/vulkanalia/introduction.html), to learn Vulkan. In time, I hope to expand this to some sort of engine-playground for experimenting with graphics programming. For now, there is:

- A Vulkan instance provided by the `vulkanalia` crate
- Error checking with validation layers
- Physical and logical devices selection
- A window surface and swapchain, with image views and framebuffers as needed
- A render pass and pipeline
- Shader modules
- Vertex buffers, index buffers, staging buffers, uniform buffers
- The Vulkan Triangle
- Samplers and textures
- A depth buffer
- OBJ model loading
- Mipmaps
- Multisample antialiasing (MSAA)
- Push constants
- Primary and secondary command buffers

The code is being heavily commented as I go through the
tutorial, so it can be useful as a learning reference.

### [minigl](https://github.com/Epsylene/minigl)
![minigl](/assets/images/minigl.png){:width="70%"}

OpenGL library to provide common functionality for my 3D school projects. There are 3 parts:

* A C++ wrapper over the OpenGL API, to provide abstractions and a more suitable interface for my needs;
* An application framework, to handle window creation, events, input, etc.;
* Utility functions, to load shaders, models, do math, etc.

### [nessie](https://github.com/Epsylene/nessie)
![nessie](/assets/images/nessie.png)

NES emulator in Rust, based on the tutorial at [https://bugzmanov.github.io/nes_ebook/](https://bugzmanov.github.io/nes_ebook/). For now, it only implements the CPU, with:

- Memory map and registers
- Status flags
- Full 6502 instruction set
- Addressing modes

Programs are loaded from an array of bytes and then run with a callback to a function on each CPU cycle; this is used for rendering to a window with SDL2.

### [axolotl-os](https://github.com/Epsylene/axolotl-os)
![axolotl-os](/assets/images/axolotlos.png)

A (very early-stage) 64-bit OS, for fun.

Comprised for now almost exclusively of a bootloader written in x86-64 assembly, which:
- Sets up the MBR
- Sets up a basic flat-model GDT
- Elevates from real mode to protected mode
- Sets up identity paging
- Elevates from protected mode to long mode
- Calls the _start() function in the kernel

### [trout](https://github.com/Epsylene/trout)
<!-- ![trout](/assets/images/trout.png) -->

Interpreter for a simple dynamically-typed programming language, from the book [*Crafting Interpreters*](https://craftinginterpreters.com/) by Robert Nystrom, implemented in Rust. The program consists of four main components:

1. A scanner that reads the source code, either from a file or a REPL, and produces a sequence of tokens.
2. A parser that produces an abstract sintax tree from the sequence of tokens.
3. A resolver that performs static analysis on the AST, checking for undeclared variables and other errors.
4. An interpreter that traverses the AST and executes the code.

The language is expression-based, with dynamic typing, lexical
scoping, local functions, closures and some built-in functions.

## Archive
### [Sirius](https://github.com/Epsylene/Sirius)
![Sirius](/assets/images/sirius.png)

Educational 3D graphics engine written in C++ and OpenGL. Features include:
- OpenGL rendering with a free camera
- 3D models with OBJ loading
- Materials and textures
- Phong shading, multiple lights
- Skyboxes with environment mapping
- Post-processing effects
- Custom logger and math library
- ImGui-based editor

Mainly based on the [LearnOpenGL](https://learnopengl.com/) tutorials.

### [CHIP-8](https://github.com/Epsylene/CHIP-8)
![CHIP-8](/assets/images/chip8.png)

An implementation of Austin Morlan's [CHIP-8 emulator](https://austinmorlan.com/posts/chip8_emulator/) in C++, using SDL2 for input and rendering. 

It runs the fetch-decode-execute cycle of the virtual CPU, using a function pointer table to get each opcode method, and displaying the result on a (scaled) 64x32 screen.