cmake_minimum_required(VERSION 3.1)
project(test_package LANGUAGES C)

find_package(xmlsec REQUIRED CONFIG)

add_executable(${PROJECT_NAME} sign1.c)
target_link_libraries(${PROJECT_NAME} PRIVATE xmlsec::xmlsec)
