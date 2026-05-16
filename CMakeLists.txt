cmake_minimum_required(VERSION 3.21)

project(AI-Assistant LANGUAGES CXX RC)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(AI-Assistant SHARED
    src/AIAssistant.cpp
    src/AIAssistantResources.rc
    src/shared/HttpClient.cpp
    src/shared/LLMApiClient.cpp
    src/shared/SettingsStorage.cpp
    src/shared/SecureStorage.cpp
)

target_include_directories(AI-Assistant PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/src
    ${CMAKE_CURRENT_SOURCE_DIR}/src/shared
    ${CMAKE_CURRENT_SOURCE_DIR}/vendor/notepadpp/PluginsManager
    ${CMAKE_CURRENT_SOURCE_DIR}/vendor/notepadpp/DockingWnd
    ${CMAKE_CURRENT_SOURCE_DIR}/vendor/scintilla/include
)

target_compile_definitions(AI-Assistant PRIVATE
    UNICODE
    _UNICODE
    NOMINMAX
    WIN32_LEAN_AND_MEAN
)

target_link_libraries(AI-Assistant PRIVATE
    comctl32
    advapi32
    crypt32
    shell32
    shlwapi
    winhttp
    riched20
    -static-libgcc
    -static-libstdc++
)

set_target_properties(AI-Assistant PROPERTIES
    OUTPUT_NAME "AI-Assistant"
    PREFIX ""
    RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/plugins/AI-Assistant"
    LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/plugins/AI-Assistant"
)
