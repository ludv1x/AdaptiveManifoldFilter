cmake_minimum_required(VERSION 2.8.3)

project(AdaptiveManifoldFilter)

find_package(OpenCV 3.0 REQUIRED)
include_directories(${OpenCV_INCLUDE_DIR})

file(GLOB hdrs "*.hpp" "*.h")
file(GLOB srcs "*.cpp")

add_executable(${PROJECT_NAME} ${hdrs} ${srcs})

include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS})
