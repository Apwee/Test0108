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
    opengl32
)

message(STATUS "Dentro de SOURCES:")
foreach(ITEM IN LISTS SOURCES)
    message(STATUS "Item actual dentro de SOURCES: ${ITEM}")
endforeach(ITEM IN LISTS SOURCES)

message(STATUS "Dentro de LIB_DIR:")
foreach(ITEM IN LISTS LIB_DIR)
    message(STATUS "Item actual dentro de LIB_DIR: ${ITEM}")
endforeach()