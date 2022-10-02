cmake_minimum_required(VERSION 2.8)
project(my_first_example)

find_package(qibuild)
#set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

#set(CMAKE_CXX_FLAGS "-D_GLIBCXX_USE_CXX11_ABI=0")

# Create a executable named my_first_example
# with the source file: main.cpp
qi_create_bin(my_first_example "main.cpp")

# Add a simple test:
qi_create_test(test_my_first_example "test.cpp")

qi_use_lib(my_first_example ALCOMMON)

qi_use_lib(my_first_example ALPROXIES)

qi_use_lib(my_first_example QI)

qi_use_lib(my_first_example ALVISION)

qi_use_lib(my_first_example ALERROR)

qi_use_lib(my_first_example OPENCV2_CORE OPENCV2_HIGHGUI)