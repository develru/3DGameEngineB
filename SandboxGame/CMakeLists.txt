cmake_minimum_required(VERSION 2.8.10)

project(SandboxGame)

file(GLOB CPP_FILES src/*.cpp)

include_directories(${Engine_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} ${CPP_FILES})

target_link_libraries(${PROJECT_NAME} Engine)


#------------
#project(3DGameEngineB)
#cmake_minimum_required(VERSION 2.8)


# Lets LOAD app our headers!
#file(GLOB_RECURSE HDRS ${3DGameEngine_SOURCE_DIR}/src/*.h)

# Lets LOAD app our sources!
#file(GLOB_RECURSE SRCS ${3DGameEngine_SOURCE_DIR}/src/*.cpp)

#find_package(PkgConfig REQUIRED)

#pkg_search_module(GLFW REQUIRED glfw3)
#include_directories(${GLFW_INCLUDE_DIRS})

#find_package(OpenGL)
#include_directories(${OPENGL_INCLUDE_DIR})

#aux_source_directory(. SRC_LIST)
#add_executable(${PROJECT_NAME} ${SRC_LIST} ${HDRS} ${SRCS})

#link_libraries(${OPENGL_gl_LIBRARY} ${MATH_LIBRARY})
#target_link_libraries(${PROJECT_NAME} ${GLFW_STATIC_LIBRARIES} ${OPENGL_LIBRARIES})


