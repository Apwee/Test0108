cmake_minimum_required(VERSION 4.1)

project(0108TEST)

file(GLOB SOURCES "${CMAKE_SOURCE_DIR}/src/*.c*")
file(GLOB LIB_DIR "${CMAKE_SOURCE_DIR}/lib/*.a")

add_executable(
    ${PROJECT_NAME}
    ${SOURCES}
)

target_include_directories(
    ${PROJECT_NAME}
    PRIVATE
    include
)

target_link_libraries(
    ${PROJECT_NAME}
    PRIVATE
    ${LIB_DIR}
    opengl32
)