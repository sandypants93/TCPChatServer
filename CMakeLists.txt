#=========================================================
# top level CMakeLists.txt for the TcpChatServer project
# 
# Dependencies:
#     o Queue
#     +----o list
#=========================================================


# project setup
cmake_minimum_required (VERSION 2.8.12)
project(TcpChatServer)

# dependency setup
add_subdirectory (queue)

# executable setup
set(SOURCES src/server.c)
add_executable(server ${SOURCES})