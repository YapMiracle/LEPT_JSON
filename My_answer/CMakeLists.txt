cmake_minimum_required (VERSION 2.6)
project (leptjson_test C)

if (CMAKE_C_COMPILER_ID MATCHES "GNU|Clang")
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -ansi -pedantic -Wall")
endif()
#生成链接库
add_library(leptjson leptjson.c)
#指定生成目标为leptjson_test
add_executable(leptjson_test test.c)
#
target_link_libraries(leptjson_test leptjson)
