cmake_minimum_required (VERSION 3.10)
project (TestTravis VERSION 1.0.0 LANGUAGES CXX)

set(REDMONKEYLIB RedMonkeyLib)
add_library(${REDMONKEYLIB} SHARED lib.h lib.cpp)

add_executable(TestTravis main.cpp)
target_link_libraries (TestTravis PUBLIC ${REDMONKEYLIB})
