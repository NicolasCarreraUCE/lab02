cmake_minimum_required(VERSION 3.25)
project(lab02)

set(CMAKE_CXX_STANDARD 17)

include(cmake/CPM.cmake)

CPMAddPackage("gh:fmtlib/fmt#10.0.0")

CPMAddPackage("gh:abdes/cryptopp-cmake#v8.8.0")

add_executable(lab02 main_omp.cpp)

target_link_libraries(lab02 fmt::fmt cryptopp::cryptopp)
