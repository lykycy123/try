cmake_minimum_required(VERSION 3.7)
project(TRY)

set(CMAKE_CXX_STANDARD 14)
add_compile_options(-O3)
set(SOURCE_FILES main.cpp)

add_executable(TRY ${SOURCE_FILES})
find_package(OpenCV 4 REQUIRED)

link_directories(${OpenCV_LIBRARY_DIRS})
target_link_libraries(TRY ${OpenCV_LIBS} -lpthread)