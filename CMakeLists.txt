cmake_minimum_required(VERSION 3.5)

project(08.homework)

add_executable(topk_words topk_words.cpp)

if (CMAKE_CXX_COMPILER_ID MATCHES "Clang" OR
    CMAKE_CXX_COMPILER_ID STREQUAL "GNU")
    target_compile_options(topk_words PRIVATE 
        -g
        -Wall
        -Wextra
        -Werror
        -pedantic
    )
elseif (CMAKE_CXX_COMPILER_ID STREQUAL "MSVC")
    target_compile_options(topk_words PRIVATE
        /EHsc
        /W4
        /WX
    )
endif()