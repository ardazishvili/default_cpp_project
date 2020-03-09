cmake_minimum_required(VERSION 3.10)
set (CMAKE_CXX_STANDARD 17)
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g")
project(proj_name)

add_subdirectory("${CMAKE_SOURCE_DIR}/tests")
add_executable(proj_name
  main.cpp
  )

add_executable(unit_tests tests/unit_main.cpp
  )
target_link_libraries(unit_tests gtest gmock)
