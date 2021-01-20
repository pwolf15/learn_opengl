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

Be sure to include GLAD before GLFW header.

GLAD manages function pointers for OpenGL functions, so initalize it pefore calling any OpenGL functions.

glViewport: size of rendering window. Instruction to OpenGL how we want to display the data and coordinates with respect to the window. How to transform 2D coordinates it processed to coordinates on your screen. -0.5,0.5 to 200, 450

render loop: keeps on drawing images and handling user input until program told to stop

glfwPollEvents: check if any events are triggered
glfwSwapBuffers: swap the color buffer (a large 2D buffer that contains the color values for each pixel in GLFW's window) that is used to render to during this render iteration and show it as output to the screen

double buffer: front buffer contains output image, while all the rendering commands draw to the back buffer
As soon as rendering commands are finished, we swap buffers.
Without double buffering, we get flickering issues in display.

Iteration of render loop: frame

glClearColor vs. glClear (state-setting vs. state-using function)