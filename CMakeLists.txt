cmake_minimum_required(VERSION 3.20)
project(Gearwave LANGUAGES CXX C)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(external/glfw)

add_library(glad
    external/glad/src/glad.c
)

target_include_directories(glad PUBLIC external/glad/include)

add_executable(Gearwave
    src/main.cpp
)

target_link_libraries(Gearwave PRIVATE glfw glad)

target_include_directories(Gearwave PRIVATE
    external/glfw/include
    external/glad/include
)