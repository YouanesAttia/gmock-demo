cmake_minimum_required(VERSION 3.10)
project(registration_service_project)

find_package(GTest REQUIRED)
include(GoogleTest)
enable_testing()

add_executable(registration_test 
    registration_service_test.cpp 
    registration_service.cpp
)

target_link_libraries(registration_test PRIVATE GTest::gmock_main)

gtest_discover_tests(registration_test)

