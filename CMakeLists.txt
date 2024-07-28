cmake_minimum_required(VERSION 3.10)

# Set the project name
project(OpenGLTriangle)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the source directory to the include path
include_directories(include)

# Add the executable
add_executable(OpenGLTriangle src/main.cpp)

# Find and link GLFW
find_package(glfw3 3.3 REQUIRED)
target_link_libraries(OpenGLTriangle glfw)

# Find and link GLEW
find_package(GLEW REQUIRED)
target_link_libraries(OpenGLTriangle GLEW::GLEW)

# Find and link OpenGL
find_package(OpenGL REQUIRED)
target_link_libraries(OpenGLTriangle OpenGL::GL)