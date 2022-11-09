cmake_minimum_required(VERSION 3.17)
project(lrenderer)

set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD 17)
include_directories(include obj)
aux_source_directory(src DIR_SRCS)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/obj)
#set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/obj)
add_executable(${PROJECT_NAME} ${DIR_SRCS})

#install(TARGETS MyLib
#        EXPORT MyLibTargets
#        LIBRARY DESTINATION lib  # 动态库安装路径
#        ARCHIVE DESTINATION lib  # 静态库安装路径
#        RUNTIME DESTINATION bin  # 可执行文件安装路径
#        PUBLIC_HEADER DESTINATION include  # 头文件安装路径
#        )