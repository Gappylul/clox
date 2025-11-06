cmake_minimum_required(VERSION 4.0)
project(clox C)

set(CMAKE_C_STANDARD 99)

add_executable(clox main.c
        include/common.h
        include/chunk.h
        chunk.c
        include/memory.h
        memory.c
        include/debug.h
        debug.c
        include/value.h
        value.c
        include/vm.h
        vm.c)

target_include_directories(clox PRIVATE include)