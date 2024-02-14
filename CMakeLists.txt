cmake_minimum_required(VERSION 3.10)
project(checkbitbalance)

set(CMAKE_CXX_STANDARD 17)
add_subdirectory(generateAddress)

include_directories(generateAddress/include)
include_directories(nlohmann)

add_executable(checkbitbalance main.cpp)
target_link_libraries(checkbitbalance pthread curl bitaddress)
