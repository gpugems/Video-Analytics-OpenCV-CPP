cmake_minimum_required(VERSION 2.8)
project( sample_03_image_test )
# Set the output folder where your program will be created
set(CMAKE_BINARY_DIR ${CMAKE_SOURCE_DIR}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})
file(GLOB SOURCES "src/*.cpp")
find_package( OpenCV REQUIRED )
add_executable( ocv_image_test ${SOURCES} )
target_link_libraries( ocv_image_test ${OpenCV_LIBS} )