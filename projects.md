---
layout: page
title:  "Projects"
categories: projects
---

## [Sirius](https://github.com/Epsylene/Sirius)
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

## [Ilya](https://github.com/Epsylene/Ilya)
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

## [caliban](https://github.com/Epsylene/caliban)
![caliban](/assets/images/caliban.png)

Implementation of the [Rust Vulkan tutorial](https://kylemayes.github.io/vulkanalia/introduction.html), to learn Vulkan. In time, I hope to expand this to some sort of engine-playground for experimenting with graphics programming. For now, there is:

- A Vulkan instance provided by the vulkanalia crate
- Error checking with validation layers
- Physical and logical devices selection
- A window surface and swapchain, with image views and framebuffers as needed
- A render pass and pipeline
- Shader modules
- Vertex buffers, index buffers, staging buffers, uniform buffers
- The Vulkan Triangle
- Samplers and textures
- A depth buffer

## [CHIP-8](https://github.com/Epsylene/CHIP-8)
![CHIP-8](/assets/images/chip8.png)

An implementation of Austin Morlan's [CHIP-8 emulator](https://austinmorlan.com/posts/chip8_emulator/) in C++, using SDL2 for input and rendering. 

It runs the fetch-decode-execute cycle of the virtual CPU,
using a function pointer table to get each opcode method, and
displaying the result on a (scaled) 64x32 screen.

## [AxolotlOS](https://github.com/Epsylene/AxolotlOS)
![AxolotlOS](/assets/images/axolotlos.png)

A (very early-stage) 64-bit OS, for fun.

Comprised for now almost exclusively of a bootloader written in assembly, which:
- Sets up the MBR
- Sets up a basic flat-model GDT
- Elevates from real mode to protected mode
- Sets up identity paging
- Elevates from protected mode to long mode
- Calls the main() function in the kernel