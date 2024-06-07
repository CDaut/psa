cmake_minimum_required(VERSION 3.20)
project(psa CXX)

if (CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
    set(CMAKE_CXX_STANDARD 20)
endif ()

set(CMAKE_CXX_FLAGS "-O3 -Wall -Wall -g")

set(SOURCE_FILES
        src/main.cpp
        src/analysis.cpp
        src/config.cpp
        src/curve.cpp
        src/delaunay.cpp
        src/image.cpp
        src/param.cpp
        src/periodogram.cpp
        src/point.cpp
        src/result.cpp
        src/spectrum.cpp
        src/statistics.cpp
)

set(HEADER_FILES
        src/analysis.h
        src/config.h
        src/curve.h
        src/delaunay.h
        src/image.h
        src/param.h
        src/periodogram.h
        src/point.h
        src/result.h
        src/spectrum.h
        src/statistics.h
        src/util.h
)

add_executable(${PROJECT_NAME} ${SOURCE_FILES} ${HEADER_FILES})
target_link_libraries(${PROJECT_NAME} cairo)