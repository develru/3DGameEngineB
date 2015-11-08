cmake_minimum_required(VERSION 2.8.10)

project(Engine)

set(CMAKE_CXX_FLAGS "-std=c++0x")

#find_package(Boost
#             1.50.0
#             REQUIRED)

file(GLOB CPP_FILES src/*.cpp)

#include_directories(${Boost_INCLUDE_DIRS})

add_library(${PROJECT_NAME} STATIC ${CPP_FILES})

# Required on Unix OS family to be able to be linked into shared libraries.
set_target_properties(${PROJECT_NAME}
                      PROPERTIES POSITION_INDEPENDENT_CODE ON)

target_link_libraries(${PROJECT_NAME})

# Expose B's public includes (including Boost transitively) to other
# subprojects through cache variable.
set(${PROJECT_NAME}_INCLUDE_DIRS ${PROJECT_SOURCE_DIR}/include
    CACHE INTERNAL "${PROJECT_NAME}: Include Directories" FORCE)





#-----------------
#project(Engine)
#cmake_minimum_required(VERSION 2.8)


# Lets LOAD app our headers!
#file(GLOB_RECURSE HDRS ${3DGameEngine_SOURCE_DIR}/src/*.h)

# Lets LOAD app our sources!
#file(GLOB_RECURSE SRCS ${3DGameEngine_SOURCE_DIR}/src/*.cpp)

#find_package(PkgConfig REQUIRED)

#pkg_search_module(GLFW REQUIRED glfw3)
#include_directories(${GLFW_INCLUDE_DIRS})
#
#find_package(OpenGL)
#include_directories(${OPENGL_INCLUDE_DIR})

#aux_source_directory(. SRC_LIST)
#add_executable(${PROJECT_NAME} ${SRC_LIST} ${HDRS} ${SRCS})

#link_libraries(${OPENGL_gl_LIBRARY} ${MATH_LIBRARY})
#target_link_libraries(${PROJECT_NAME} ${GLFW_STATIC_LIBRARIES} ${OPENGL_LIBRARIES})


