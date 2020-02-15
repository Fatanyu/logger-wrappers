cmake_minimum_required(VERSION 3.15)
project(logger_wrappers)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pedantic -Wall -Wextra")

include_directories(sources)

add_library(spdlog-wrapper STATIC sources/spdlog-wrapper/library.cpp sources/spdlog-wrapper/library.h)

add_subdirectory(external-libraries/google-tests)
include_directories(external-libraries/google-tests/googletest/googletest/include)
include_directories(external-libraries/google-tests/googletest/googlemock/include)