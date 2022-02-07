cmake_minimum_required(VERSION 3.01)

project(example)

set(CMAKE_CXX_STANDARD 14)

add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME}  PUBLIC
        prim
        /usr/local/lib/libcapd.so
        )

target_compile_options(${PROJECT_NAME}
        PUBLIC
        -D__USE_FILIB__)
        
target_compile_definitions(${PROJECT_NAME}
        PUBLIC
        _USE_MATH_DEFINES)