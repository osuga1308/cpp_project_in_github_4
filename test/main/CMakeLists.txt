cmake_minimum_required(VERSION 3.10)

add_executable(TestMain test_main.cpp)

target_link_libraries(TestMain gtest gtest_main pthread)

add_test(NAME TestMain COMMAND TestMain)
