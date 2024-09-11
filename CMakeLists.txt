cmake_minimum_required(VERSION 3.22)
project(learn_opengl)

set(CMAKE_CXX_STANDARD 20)

find_package(glfw3 3.3 REQUIRED)

file(GLOB_RECURSE SOURCES src/*.cpp src/*.c src/*.h)

# message(${SOURCES})
include_directories(${PROJECT_SOURCE_DIR}/include)
add_executable(learn_opengl ${SOURCES})

target_link_libraries(learn_opengl glfw)