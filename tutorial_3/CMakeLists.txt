cmake_minimum_required(VERSION 3.5)
project(HelloApp
        VERSION 1.0.0
        DESCRIPTION "The leading Hello World App"
        LANGUAGES CXX)

# Not recommended
# https://stackoverflow.com/questions/1027247/is-it-better-to-specify-source-files-with-glob-or-each-file-individually-in-cmak/1060061#1060061
# https://stackoverflow.com/a/1060061
# file(GLOB_RECURSE SRC_FILES src/*.cpp) # store source files in variable SRC_FILES
# add_executable(HelloBinary main.cpp ${SRC_FILES}) # use SRC_FILES to build the binary


#List your sources
add_executable(HelloBinary main.cpp
                src/dog.cpp
                src/operations.cpp)

target_compile_features(HelloBinary PRIVATE cxx_std_20)
target_include_directories(HelloBinary PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)