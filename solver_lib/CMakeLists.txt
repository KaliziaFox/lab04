cmake_minimum_required(VERSION 3.10) 
project(formatter_ex)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/solver.cpp)
set(HEADERS ${CMAKE_CURRENT_SOURCE_DIR}/solver.h)

add_library(solver_lib STATIC ${SOURCES} ${HEADERS})
target_include_directories(solver_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(solver_lib formatter)
target_link_libraries(solver_lib formatter_ex)

