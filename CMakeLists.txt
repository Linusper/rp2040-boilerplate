cmake_minimum_required(VERSION 3.13)
include(pico_sdk_import.cmake)
set(PROJECT_NAME "boilerplate")
project(${PROJECT_NAME}
        LANGUAGES C CXX ASM
        DESCRIPTION "RP2040 Boilerplate project"
)
pico_sdk_init()
add_subdirectory(src)
