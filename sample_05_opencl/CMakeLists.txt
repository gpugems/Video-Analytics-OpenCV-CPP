cmake_minimum_required(VERSION 2.8)
project( sample_05_opencl )
# Set the output folder where your program will be created
set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})
file(GLOB SOURCES "src/*.cpp")
find_package( OpenCV REQUIRED )
add_executable( ocv_ocl_info ${SOURCES} )
target_link_libraries( ocv_ocl_info ${OpenCV_LIBS} )