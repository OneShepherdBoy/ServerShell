

## Include nlohmann/json
include(FetchContent)

FetchContent_Declare(json URL https://github.com/nlohmann/json/releases/download/v3.11.3/json.tar.xz)
FetchContent_MakeAvailable(json)

#
add_library(${SHELL_SERVER_TARGET_NAME} INTERFACE)
add_library(${PROJECT_NAME}::${SHELL_SERVER_TARGET_NAME} ALIAS ${SHELL_SERVER_TARGET_NAME})

#
target_link_libraries(foo PRIVATE nlohmann_json::nlohmann_json)