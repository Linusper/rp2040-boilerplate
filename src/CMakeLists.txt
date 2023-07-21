cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

add_executable(boilerplate
	main.c
	sum.c
)
pico_enable_stdio_usb(boilerplate 1)
pico_enable_stdio_uart(boilerplate 1)

pico_add_extra_outputs(boilerplate)

target_link_libraries(boilerplate pico_stdlib)

include_directories(../inc)
