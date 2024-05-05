cmake_minimum_required(VERSION 3.28)
project(cpp_opengl)
set(CMAKE_CXX_STANDARD 17)

# Find packages
find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

include_directories(${GLEW_INCLUDE_DIRS} ${GLFW_INCLUDE_DIRS} ${OPENGL_INCLUDE_DIRS})

add_executable(cpp_opengl main.cpp)
target_link_libraries(cpp_opengl ${GLEW_LIBRARIES} glfw OpenGL::GL)