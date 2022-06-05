cmake_minimum_required(VERSION 3.10)
project(ExampleProject)

set(CMAKE_CXX_STANDARD 17)

include_directories(include
                    lib/googletest/googletest)

add_subdirectory(src)
add_subdirectory(tst)
add_subdirectory(lib/googletest)
