cmake_minimum_required(VERSION 3.4)
if("${CMAKE_CXX_COMPILER}" STREQUAL "")
       set(CMAKE_C_COMPILER "icx")
       set(CMAKE_CXX_COMPILER "icpx")
endif()
project (oneCCL)
if("$ENV{EXAMPLE_ROOT}" STREQUAL "")
        message(" - use default examples")
        add_subdirectory ($ENV{CCL_ROOT}/share/doc/ccl/examples out)
else()
        add_subdirectory ($ENV{EXAMPLE_ROOT} out)
endif()
