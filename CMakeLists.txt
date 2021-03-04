cmake_minimum_required(VERSION 3.9)
set(target "linter_example")

# find_package(Python3 REQUIRED)
if( NOT WIN32 )
    include(cmake/Cpplint.cmake)
    cpplint_add_subdirectory(example)
endif( NOT WIN32 )

add_executable(${target} example/main.cpp)
