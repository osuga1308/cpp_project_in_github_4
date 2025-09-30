cmake_minimum_required(VERSION 3.10)

add_executable(TestMain test_main.cpp)

target_link_libraries(TestMain gtest gtest_main)

# Linux / macOS では pthread が必要
if(UNIX AND NOT APPLE)
    target_link_libraries(TestMain pthread)
endif()

add_test(NAME TestMain COMMAND TestMain)

