cmake_minimum_required(VERSION 3.10)
project(cpp_project_in_github_4)

add_executable(main src/main.cpp)

enable_testing()
set(gtest_force_shared_crt ON CACHE BOOL "Use shared (DLL) run-time lib by default")
add_subdirectory(test)

