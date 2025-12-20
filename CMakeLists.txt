cmake_minimum_required(VERSION 3.20)
project(Gearwave LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(Gearwave
    src/main.cpp
)

add_subdirectory(external/glfw)

target_link_libraries(Gearwave
    glfw
)