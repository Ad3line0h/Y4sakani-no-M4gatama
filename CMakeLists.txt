cmake_minimum_required(VERSION 3.13...3.31)

set(CMAKE_TOOLCHAIN_FILE "C:/Users/skanm/Desktop/Y4sakani-no-M4gatama/vcpkg/scripts/buildsystems/vcpkg.cmake")
set(VCPKG_TARGET_TRIPLET "x64-windows")
set(glfw3_DIR "C:/Users/skanm/Desktop/Y4sakani-no-M4gatama/vcpkg/installed/x64-windows/share/glfw3")

set(PROJECT_NAME Y4SAKANI_NO_M4GATAMA)
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(${PROJECT_NAME} src/main.cpp)

find_package(OpenGL REQUIRED)
find_package(glfw3 CONFIG REQUIRED)
find_package(glad CONFIG REQUIRED)

target_link_libraries(${PROJECT_NAME} 
    OpenGL::GL 
    glfw
    glad::glad
)