if(WIN32)
        set(CMAKE_CXX_COMPILER "dpcpp-cl")
        set(CMAKE_C_COMPILER "dpcpp-cl")
else()
        set(CMAKE_CXX_COMPILER "dpcpp")
endif()
if(NOT DEFINED ${CMAKE_BUILD_TYPE})
	set(CMAKE_BUILD_TYPE "RELEASE")
endif()
if( CMAKE_BUILD_TYPE STREQUAL "DEBUG" )
	set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g")
endif()
cmake_minimum_required (VERSION 3.0)
project (NBODY)
add_subdirectory (src)
