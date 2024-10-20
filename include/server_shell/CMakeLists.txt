

## Include nlohmann/json
include(FetchContent)
FetchContent_Declare(
        json
        GIT_REPOSITORY https://github.com/nlohmann/json.git
        GIT_TAG master
)

FetchContent_MakeAvailable(json)

#
add_library(${SERVER_SHELL_TARGET_NAME} INTERFACE)
add_library(${PROJECT_NAME}::${SERVER_SHELL_TARGET_NAME} ALIAS ${SERVER_SHELL_TARGET_NAME})