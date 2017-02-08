#
# This is a CMake makefile.  You can find the cmake utility and
# information about it at http://www.cmake.org
#


cmake_minimum_required(VERSION 2.8.4)

PROJECT(dlib-ext)

include(../dlib/dlib/cmake)



# Since there are a lot of examples I'm going to use a macro to simply this
# CMakeLists.txt file.  However, usually you will create only one executable in
# your cmake projects and use the syntax shown above.
MACRO(add_src name)
   ADD_EXECUTABLE(${name} ${name}.cpp)
   TARGET_LINK_LIBRARIES(${name} dlib )
ENDMACRO()

add_src(test)



