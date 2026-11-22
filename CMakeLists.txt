cmake_minimum_required(VERSION 3.20)
set(CMAKE_CXX_STANDARD 20)

project(main)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)
set(BUILD_SHARED_LIBS OFF CACHE BOOL "" FORCE)

add_subdirectory(libraries/glfw-3.3.2)
add_subdirectory(libraries/glad)

add_executable(main src/main.cpp)

target_link_libraries("${CMAKE_PROJECT_NAME}" PRIVATE glfw glad)