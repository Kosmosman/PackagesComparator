CMAKE_MINIMUM_REQUIRED(VERSION 3.15)
PROJECT(PackageComparator)

SET(CMAKE_CXX_STANDARD 20)

SET(LIB_NAME package_comparator_lib)
FILE(GLOB_RECURSE ${LIB_NAME}_SRCS
        lib/*.cc
)
FILE(GLOB_RECURSE ${LIB_NAME}_HDRS
        lib/*.h
)

add_library(${LIB_NAME} SHARED
        ${${LIB_NAME}_SRCS}
        ${${LIB_NAME}_HDRS}
)

install(TARGETS ${LIB_NAME} DESTINATION /usr/local/lib)
