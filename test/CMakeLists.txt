cmake_minimum_required(VERSION 3.16)
project(test)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(test
    src/main.cpp
)

target_compile_options(test PRIVATE
    -Wall
    -Wextra
    -Wpedantic
)
