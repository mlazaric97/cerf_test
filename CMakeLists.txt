cmake_minimum_required(VERSION 3.17)

project(cerf_test LANGUAGES CXX C)

set (CMAKE_CXX_STANDARD 17)
set (CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(cerf REQUIRED ON) #can't get it working :/ 



include_directories(${cerf_DIR}
		    ${CMAKE_SOURCE_DIR}/src/) #cerf_DIR

add_compile_options(-O3 -Wall)

add_executable(cerf_test cerf_test.cpp)

target_link_libraries(cerf_test
			cerf::cerfcpp)
