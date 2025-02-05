cmake_minimum_required(VERSION 3.16.3)
project(ProgrammingQuiz4)

set(CMAKE_CXX_STANDARD 14)

# Set the include and link directories for Bridges
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/libraries/bridges/include)
link_directories(${CMAKE_CURRENT_SOURCE_DIR}/libraries/bridges/lib)

# Use the system-installed cURL library
find_package(CURL REQUIRED)
include_directories(${CURL_INCLUDE_DIRS})

add_executable(ProgrammingQuiz4 ImdbTree.cpp)
target_link_libraries(ProgrammingQuiz4 ${CURL_LIBRARIES})