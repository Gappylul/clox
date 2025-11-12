cmake_minimum_required(VERSION 4.0)
project(clox C)

set(CMAKE_C_STANDARD 99)

set(SOURCES
        src/main.c
        src/chunk.c
        src/memory.c
        src/debug.c
        src/value.c
        src/vm.c
        src/scanner.c
        src/compiler.c
        src/object.c
)

set(HEADERS
        include/common.h
        include/chunk.h
        include/memory.h
        include/debug.h
        include/value.h
        include/vm.h
        include/compiler.h
        include/scanner.h
        include/object.h
)

add_executable(clox ${SOURCES} ${HEADERS})

target_include_directories(clox PRIVATE src include)