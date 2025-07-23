cmake_minimum_required(VERSION 3.10)
project(cpp-search-server)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCES
    main.cpp
    document.cpp
    read_input_functions.cpp
    request_queue.cpp
    search_server.cpp
    string_processing.cpp
)

add_executable(search_server ${SOURCES})
