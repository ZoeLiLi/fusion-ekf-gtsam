cmake_minimum_required(Version 3.0)
set(CXX_FLAGS_STANDARD 11)
project(fusion)
set(TARGET_LIB ${PROJECT_NAME})

file(GLOB_RECURSE SRC_FILES ${PROJECT_SOURCE_DIR}/src/*.cpp
			    ${PROJECT_SOURCE_DIR}/include/*.h)
include_directories(${PROJECT_SOURCE_DIR}/include)

add_library(${TARGET_NAME} static ${SRC_FILES})

option(ENABLE_TEST_PROJECT "build test project" ON)

if(ENABLE_TEST_PROJECT)
  add_subdirectory(test)
endif()
