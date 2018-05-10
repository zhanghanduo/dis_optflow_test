cmake_minimum_required(VERSION 3.0)
project(opt_flow_test)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_BUILD_TYPE Release)

set(OpenCV_DIR /home/hd/softwares/opencv-3.3.0/release)

find_package(OpenCV 3.1 REQUIRED)

include_directories(
#        include
        ${OpenCV_INCLUDE_DIRS}
)



add_executable(opt_flow_test main.cpp)
target_link_libraries(opt_flow_test
        ${OpenCV_LIBS}
        -lopencv_optflow
        )