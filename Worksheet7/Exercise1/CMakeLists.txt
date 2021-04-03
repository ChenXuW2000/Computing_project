# CMakeLists.txt 
cmake_minimum_required(VERSION 2.8.0)
project(MathsLib)
include(CTest)
add_library( maths adder.cpp )
if( NOT BUILD_SHARED_LIBS )
add_definitions( -Dmaths_STATIC )
endif()
add_executable(test1 test1.cpp)
target_link_libraries(test1 maths)
add_test(test1 test1)
# end 