cmake_minimum_required(VERSION 3.24)
project(opengl_101 C)

set(CMAKE_C_STANDARD 11)

add_executable(opengl_101 main.c)

find_package(OpenGL REQUIRED COMPONENTS OpenGL)
find_package(GLUT REQUIRED)

add_dependencies(opengl_101 OpenGL::OpenGL)
include_directories(${GLUT_INCLUDE_DIRS} )
target_link_libraries(opengl_101 OpenGL::OpenGL ${GLUT_LIBRARIES} )
