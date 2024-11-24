# BasicVertexShader

This project demonstrates a simple vertex shader that colors a triangle based on vertex positions. It is meant to showcase the basic usage of vertex shaders in OpenGL and how they interact with the rest of the pipeline.

## Dependencies:
- C++ Compiler
- OpenGL
- GLM (for matrix math)
- GLFW (for window creation)
- GLEW (for managing OpenGL extensions)

## Setup:
1. Clone the repository:
git clone https://github.com/CozartKevin/ShaderPlayground.git

2. Navigate to the `BasicVertexShader` directory:
cd ShaderPlayground/projects/ShaderDemos/BasicVertexShader 

3. Build the project using CMake:
mkdir build cd build cmake .. make

4. Run the project:
./basic_vertex_shader


## How It Works:
- **Vertex Shader**: The vertex shader computes the position and color of each vertex in the triangle. It transforms the coordinates from object space to clip space.
- **Fragment Shader**: The fragment shader applies color interpolation to smooth out the color transitions between the vertices.

## Assets:
- `triangle.obj`: A simple 3D model of a triangle (can be replaced with your own models).
