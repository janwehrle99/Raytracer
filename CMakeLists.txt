cmake_minimum_required (VERSION 3.9)
project (raytracer)


set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)


add_compile_options(-g -Wall -Wextra -Wpedantic -Wl,--stack,16777216)


# Hinzufügen der ausführbaren Dateien
add_executable(math_test math_test.cc raytracer.cc)
add_executable(geometry_test geometry_test.cc raytracer.cc)


# Verlinken der Bibliotheken mit den Zielen
target_link_libraries(math_test gtest gtest_main)
target_link_libraries(geometry_test gtest gtest_main)