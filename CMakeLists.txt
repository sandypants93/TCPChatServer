#=========================================================
# top level CMakeLists.txt for the TcpChatServer project
# 
# Dependencies:
#     o Queue
#     +----o list
#=========================================================


# project setup
cmake_minimum_required (VERSION 3.12)
project(TcpChatServer)

# dependency setup
add_subdirectory(LinkedList)
set(DEPENDENCIES 
    LinkedList
)

# executable setup
set(SOURCES 
    src/server.c
)
add_executable(server ${SOURCES})
target_link_libraries(server 
    PRIVATE
    ${DEPENDENCIES})