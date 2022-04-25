cmake_minimum_required(VERSION 3.14)
project(Perlin)

add_compile_options(
	-Wall
	-Wextra
	-Werror
)

add_library(perlin
	perlin.c
)

target_link_libraries(perlin
	m
)

target_include_directories(perlin
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}
)

add_executable(perlintest perlintest.c)
target_link_libraries(perlintest perlin)
