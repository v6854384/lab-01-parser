make_minimum_required(VERSION 2.8)

project(CH CXX)

if (MSVC)
    add_definitions(/W4)
else()
    add_definitions(-Wall)
    add_definitions(-std=c++17)
endif()

include_directories(include)

enable_testing()

add_executable(test_json main.cpp)

add_test(NAME ${PROJECT_NAME} COMMAND test_json)
