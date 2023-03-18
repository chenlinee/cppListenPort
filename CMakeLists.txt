# CMake 最低版本号要求
cmake_minimum_required (VERSION 2.8)

# generate compile_commands.json
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# set compiler
SET (CMAKE_C_COMPILER               "clang")
SET (CMAKE_C_FLAGS                  "-Wall -std=c11")
SET (CMAKE_C_FLAGS_DEBUG            "-g")
SET (CMAKE_C_FLAGS_MINSIZEREL       "-Os -DNDEBUG")
SET (CMAKE_C_FLAGS_RELEASE          "-O4 -DNDEBUG")
SET (CMAKE_C_FLAGS_RELWITHDEBINFO   "-O2 -g")

SET (CMAKE_CXX_COMPILER             "clang++")
SET (CMAKE_CXX_FLAGS                "-Wall -std=c++17")
SET (CMAKE_CXX_FLAGS_DEBUG          "-g")
SET (CMAKE_CXX_FLAGS_MINSIZEREL     "-Os -DNDEBUG")
SET (CMAKE_CXX_FLAGS_RELEASE        "-O4 -DNDEBUG")
SET (CMAKE_CXX_FLAGS_RELWITHDEBINFO "-O2 -g")

# 项目信息
project (NetworkDemo)

# 指定生成目标
add_executable(server server.cpp)
add_executable(client client.cpp)
