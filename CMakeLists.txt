cmake_minimum_required(VERSION 3.0.0)
project(cpp_tutorial VERSION 0.1.0)

include(CTest)
enable_testing()

add_executable(cpp_tutorial main.cpp)
target_link_libraries(cpp_tutorial mylib)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

add_subdirectory(mylib)
