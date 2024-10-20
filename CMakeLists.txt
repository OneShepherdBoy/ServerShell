cmake_minimum_required(VERSION 3.20)

# Project settings
project(ServerShell
        VERSION 0.0.1
        LANGUAGES CXX
        DESCRIPTION "Library to bootstrap your server's shell creation.")

## Require C++14
set(CMAKE_CXX_STANDARD 14)

## Require the C++ standard and nothing else
set(CMAKE_CXX_STANDARD_REQUIRED ON)

## Turn off vendor specific compiler extensions
set(CMAKE_CXX_EXTENSIONS OFF)

## Prevents In-source builds
if(PROJECT_SOURCE_DIR STREQUAL PROJECT_BINARY_DIR)
    message(FATAL_ERROR "In-source builds are not allowed.")
endif()

## Library name
set(SERVER_SHELL_TARGET_NAME server_shell)

# Project components
add_subdirectory(include/server_shell)
## add_subdirectory(examples)
## add_subdirectory(tests)