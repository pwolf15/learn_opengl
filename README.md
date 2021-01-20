# Overview

## Getting Started

* Create an OpenGL context and an application window.
* Both are OS-specific and OpenGL tries to abstract itself from these operations.

1. Create a window.
2. Define a context.
3. Handle user input.

Popular options
* GLUT
* SDL
* SFML
* GLFW

GLFW: Create context, define window parameters, handle user input.
OpenGL is just a specification; driver manufacturer must implement the specification for a given graphics card.

GLAD: Open source library that handles API calls for getting locations of functions at run-time.