cmake_minimum_required(VERSION 3.10)

project(Game)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

set(CMAKE_TOOLCHAIN_FILE "C:/Users/flaim/Desktop/vcpkg/scripts/buildsystems/vcpkg.cmake" CACHE STRING "")
set(CMAKE_PREFIX_PATH "C:/Users/flaim/Desktop/vcpkg/installed/x64-windows")

set(SOURCES
    main.cpp 
)

add_executable(Game ${SOURCES})

find_package(glfw3 CONFIG REQUIRED)
find_package(GLEW REQUIRED)

target_link_libraries(Game PRIVATE glfw GLEW::GLEW)
