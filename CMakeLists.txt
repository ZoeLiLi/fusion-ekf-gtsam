cmake_minimum_required(VERSION 3.0)
set(CMAKE_CXX_STANDARD 11)
project(fusion-ekf-gtsam)

add_subdirectory(${PROJECT_SOURCE_DIR}/multi_sensor_fusion)

option(ENABLE_EXAMPLE_PROJECT       "enable example project or not"  OFF)

if(ENABLE_EXAMPLE_PROJECT)
    add_subdirectory(${PROJECT_SOURCE_DIR}/example)
endif()
