cmake_minimum_required(VERSION 2.8...3.5)

project(SoftwareRender VERSION 0.1 LANGUAGES CXX)

set(SFML_DIR ${CMAKE_CURRENT_SOURCE_DIR}/dependencies/SFML/lib/cmake/SFML)
set(SFML_STATIC_LIBRARIES TRUE)

find_package(SFML COMPONENTS graphics REQUIRED)

add_executable(main  src/main.cpp)

target_link_libraries(main sfml-graphics)